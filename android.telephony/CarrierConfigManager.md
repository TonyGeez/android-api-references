Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CarrierConfigManager

```
open class CarrierConfigManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.CarrierConfigManager](CarrierConfigManager.md) |

Provides access to telephony configuration values that are carrier-specific. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)`.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.Apn` Configs used for APN setup. |
| | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.Bsf` This groups the BSF (BootStrapping Function) related configs. |
| abstract | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.CarrierConfigChangeListener` Listener interface to get a notification when the carrier configurations have changed. |
| --- | --- |
| | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.Gps` GPS configs. |
| | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.Ims` Configs used by the IMS stack. |
| | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.ImsEmergency` Emergency Call/E911. |
| --- | --- |
| | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.ImsRtt` IMS RTT configs. |
| | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.ImsServiceEntitlement` Configs used by ImsServiceEntitlement. |
| | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.ImsSms` IMS SMS configs. |
| --- | --- |
| | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.ImsSs` IMS supplementary services configs. |
| | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.ImsVoice` IMS Voice configs. |
| | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.ImsVt` IMS Video Telephony configs. |
| --- | --- |
| | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.ImsWfc` WiFi Calling. |
| | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.Iwlan` Configs used for epdg tunnel bring up. |
| | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.OpportunisticNetwork` Carrier configuration keys for opportunistic networks. |
| --- | --- |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#ACTION_CARRIER_CONFIG_CHANGED:kotlin.String` This intent is broadcast by the system when carrier config changes. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#CARRIER_NR_AVAILABILITY_NSA:kotlin.Int` Indicates CARRIER_NR_AVAILABILITY_NSA determine that the carrier enable the non-standalone (NSA) mode of 5G NR. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#CARRIER_NR_AVAILABILITY_SA:kotlin.Int` Indicates CARRIER_NR_AVAILABILITY_SA determine that the carrier enable the standalone (SA) mode of 5G NR. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#CARRIER_ROAMING_NTN_CONNECT_AUTOMATIC:kotlin.Int` Device can connect to carrier roaming non-terrestrial network automatically. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#CARRIER_ROAMING_NTN_CONNECT_HYBRID:kotlin.Int` Device can connect to carrier roaming non-terrestrial network both automatically and manually i. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#CARRIER_ROAMING_NTN_CONNECT_MANUAL:kotlin.Int` Device can connect to carrier roaming non-terrestrial network only if user manually triggers satellite connection. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#CROSS_SIM_SPN_FORMAT_CARRIER_NAME_ONLY:kotlin.Int` Specifies SPN format of displaying carrier name only. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#CROSS_SIM_SPN_FORMAT_CARRIER_NAME_WITH_BRANDING:kotlin.Int` Specifies SPN format of displaying carrier name along with "Cross-SIM calling". |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#DATA_CYCLE_THRESHOLD_DISABLED:kotlin.Int` Flag indicating that a data cycle threshold should be disabled. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#DATA_CYCLE_USE_PLATFORM_DEFAULT:kotlin.Int` When `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MONTHLY_DATA_CYCLE_DAY_INT:kotlin.String`, `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_DATA_LIMIT_THRESHOLD_BYTES_LONG:kotlin.String`, or `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_DATA_WARNING_THRESHOLD_BYTES_LONG:kotlin.String` are set to this value, the platform default value will be used for that key. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#ENABLE_EAP_METHOD_PREFIX_BOOL:kotlin.String` Specifies whether the system should prefix the EAP method to the anonymous identity. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#EXTRA_REBROADCAST_ON_UNLOCK:kotlin.String` `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#ACTION_CARRIER_CONFIG_CHANGED:kotlin.String` is broadcast once on device bootup and then again when the device is unlocked. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#EXTRA_SLOT_INDEX:kotlin.String` Extra included in `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#ACTION_CARRIER_CONFIG_CHANGED:kotlin.String` to indicate the slot index that the broadcast is for. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#EXTRA_SUBSCRIPTION_INDEX:kotlin.String` Optional extra included in `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#ACTION_CARRIER_CONFIG_CHANGED:kotlin.String` to indicate the subscription index that the broadcast is for, if a valid one is available. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#IMSI_KEY_AVAILABILITY_INT:kotlin.String` Identifies if the key is available for WLAN or EPDG or both. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_5G_NR_SSRSRP_THRESHOLDS_INT_ARRAY:kotlin.String` List of 4 customized 5G SS reference signal received power (SSRSRP) thresholds. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_5G_NR_SSRSRQ_THRESHOLDS_INT_ARRAY:kotlin.String` List of 4 customized 5G SS reference signal received quality (SSRSRQ) thresholds. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_5G_NR_SSSINR_THRESHOLDS_INT_ARRAY:kotlin.String` List of 4 customized 5G SS signal-to-noise and interference ratio (SSSINR) thresholds. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_ADDITIONAL_CALL_SETTING_BOOL:kotlin.String` Does not display additional call setting for IMS phone based on GSM Phone |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_ADDITIONAL_SETTINGS_CALLER_ID_VISIBILITY_BOOL:kotlin.String` Boolean indicating if the "Caller ID" item is visible in the Additional Settings menu. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_ADDITIONAL_SETTINGS_CALL_WAITING_VISIBILITY_BOOL:kotlin.String` Boolean indicating if the "Call Waiting" item is visible in the Additional Settings menu. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_ALLOW_ADDING_APNS_BOOL:kotlin.String` Allow user to add APNs |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_ALLOW_ADD_CALL_DURING_VIDEO_CALL_BOOL:kotlin.String` When `false`, indicates that adding a call is disabled when there is an ongoing video call or when there is an ongoing call on wifi which was downgraded from video and VoWifi is turned off. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_ALLOW_EMERGENCY_NUMBERS_IN_CALL_LOG_BOOL:kotlin.String` Determines if the current device should allow emergency numbers to be logged in the Call Log. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_ALLOW_EMERGENCY_VIDEO_CALLS_BOOL:kotlin.String` Flag indicating whether to allow carrier video calls to emergency numbers. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_ALLOW_HOLD_CALL_DURING_EMERGENCY_BOOL:kotlin.String` Flag indicating whether or not an ongoing call will be held when an outgoing emergency call is placed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_ALLOW_HOLD_IN_RTT_CALL_BOOL:kotlin.String` Flag indicating whether RTT (Real-Time Text) calls support the hold/unhold capability. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_ALLOW_HOLD_VIDEO_CALL_BOOL:kotlin.String` When `true`, indicates that video calls can be put on hold in order to swap to another call (e.g. a new outgoing call). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_ALLOW_LOCAL_DTMF_TONES_BOOL:kotlin.String` Determine whether we want to play local DTMF tones in a call, or just let the radio/BP handle playing of the tones. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_ALLOW_MERGE_WIFI_CALLS_WHEN_VOWIFI_OFF_BOOL:kotlin.String` Flag indicating whether the carrier supports merging wifi calls when VoWIFI is disabled. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_ALLOW_NON_EMERGENCY_CALLS_IN_ECM_BOOL:kotlin.String` Determines whether the carrier supports making non-emergency phone calls while the phone is in emergency callback mode. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_ALLOW_VIDEO_CALLING_FALLBACK_BOOL:kotlin.String` Whether system apps are allowed to use fallback if carrier video call is not available. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_ALLOW_VIDEO_CALL_IN_LOW_BATTERY_BOOL:kotlin.String` Flag indicating whether or not an incoming video call will be auto rejected and logged since device is in low battery. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_ALWAYS_SHOW_DATA_RAT_ICON_BOOL:kotlin.String` Boolean indicating if show data RAT icon on status bar even when data is disabled. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_ALWAYS_SHOW_EMERGENCY_ALERT_ONOFF_BOOL:kotlin.String` The default flag specifying whether "Allow alerts" option will be always shown in emergency alerts settings regardless developer options is turned on or not. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_ALWAYS_SHOW_PRIMARY_SIGNAL_BAR_IN_OPPORTUNISTIC_NETWORK_BOOLEAN:kotlin.String` Indicates when a carrier has a primary subscription and an opportunistic subscription active, and when Internet data is switched to opportunistic network, whether to still show signal bar of primary network. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_APN_EXPAND_BOOL:kotlin.String` Control whether users can edit APNs in Settings. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_APN_SETTINGS_DEFAULT_APN_TYPES_STRING_ARRAY:kotlin.String` Default value of APN types field if not specified by user when adding/modifying an APN. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_AUTO_RETRY_ENABLED_BOOL:kotlin.String` Flag indicating if auto retry is enabled |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_AUTO_UNHOLD_ON_REMOTE_DISCONNECT_BOOL:kotlin.String` Flag indicating whether the carrier supports auto-unholding the background call on remotely disconnected calls. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_AVOID_BAD_WIFI_BOOL:kotlin.String` Used in reading the 'avoid bad Wi-Fi' setting from the carrier config. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CALL_BARRING_DEFAULT_SERVICE_CLASS_INT:kotlin.String` Specifies the service class for call barring service. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CALL_BARRING_SUPPORTS_DEACTIVATE_ALL_BOOL:kotlin.String` Flag indicating whether or not deactivating all call barring features via the "Call Barring" settings menu is supported. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CALL_BARRING_SUPPORTS_PASSWORD_CHANGE_BOOL:kotlin.String` Flag indicating whether or not changing the call barring password via the "Call Barring" settings menu is supported. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CALL_BARRING_VISIBILITY_BOOL:kotlin.String` Boolean indicating if the "Call barring" item is visible in the Call Settings menu. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CALL_COMPOSER_PICTURE_SERVER_URL_STRING:kotlin.String` Indicates the carrier server url that serves the call composer picture. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CALL_FORWARDING_BLOCKS_WHILE_ROAMING_STRING_ARRAY:kotlin.String` An array containing custom call forwarding number prefixes that will be blocked while the device is reporting that it is roaming. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CALL_REDIRECTION_SERVICE_COMPONENT_NAME_STRING:kotlin.String` Specifies a carrier-defined `https://developer.android.com/reference/kotlin/android/telecom/CallRedirectionService.html#` which Telecom will bind to for outgoing calls. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CAPABILITIES_EXEMPT_FROM_SINGLE_DC_CHECK_INT_ARRAY:kotlin.String` Only apply if `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_ONLY_SINGLE_DC_ALLOWED_INT_ARRAY:kotlin.String` specifies the network types that support a single data connection at a time. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_ALLOW_DEFLECT_IMS_CALL_BOOL:kotlin.String` Flag indicating whether the carrier supports call deflection for an incoming IMS call. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_ALLOW_TURNOFF_IMS_BOOL:kotlin.String` Flag specifying whether IMS service can be turned off. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_APP_REQUIRED_DURING_SIM_SETUP_BOOL:kotlin.String` Determines whether the carrier app needed to be involved when users try to finish setting up the SIM card to get network service. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_CALL_SCREENING_APP_STRING:kotlin.String` The Component Name of a carrier-provided CallScreeningService implementation. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_CERTIFICATE_STRING_ARRAY:kotlin.String` Holds the list of carrier certificate hashes, followed by optional package names. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_CONFIG_APPLIED_BOOL:kotlin.String` Determines whether any carrier has been identified and its specific config has been applied, default to false. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_CONFIG_VERSION_STRING:kotlin.String` Specifies a value that identifies the version of the carrier configuration that is currently in use. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_CROSS_SIM_IMS_AVAILABLE_BOOL:kotlin.String` Flag specifying whether Cross SIM over IMS should be available for carrier. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_DATA_CALL_PERMANENT_FAILURE_STRINGS:kotlin.String` Data call setup permanent failure causes by the carrier. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_DEFAULT_ACTIONS_ON_DCFAILURE_STRING_ARRAY:kotlin.String` Defines carrier-specific actions which act upon CARRIER_SIGNAL_REQUEST_NETWORK_FAILED and configured signal args: android. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_DEFAULT_ACTIONS_ON_DEFAULT_NETWORK_AVAILABLE:kotlin.String` Defines carrier-specific actions which act upon com. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_DEFAULT_ACTIONS_ON_REDIRECTION_STRING_ARRAY:kotlin.String` Defines carrier-specific actions which act upon com. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_DEFAULT_ACTIONS_ON_RESET:kotlin.String` Defines carrier-specific actions which act upon CARRIER_SIGNAL_RESET, used for customization of the default carrier app. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_DEFAULT_REDIRECTION_URL_STRING_ARRAY:kotlin.String` Defines a list of acceptable redirection url for default carrier app. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_DEFAULT_WFC_IMS_ENABLED_BOOL:kotlin.String` Default WFC_IMS_enabled: true VoWiFi by default is on false VoWiFi by default is off |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_DEFAULT_WFC_IMS_MODE_INT:kotlin.String` Default mode for WFC over IMS on home network: - 0: Wi-Fi only - 1: prefer mobile network - 2: prefer Wi-Fi <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_DEFAULT_WFC_IMS_ROAMING_MODE_INT:kotlin.String` Default mode for WFC over IMS on roaming network. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_FORCE_DISABLE_ETWS_CMAS_TEST_BOOL:kotlin.String` The default flag specifying whether ETWS/CMAS test setting is forcibly disabled in Settings-\>More-\>Emergency broadcasts menu even though developer options is turned on. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_IMS_GBA_REQUIRED_BOOL:kotlin.String` Flag specifying whether Generic Bootstrapping Architecture capable SIM is required for IMS. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_INSTANT_LETTERING_AVAILABLE_BOOL:kotlin.String` Flag specifying whether IMS instant lettering is available for the carrier. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_INSTANT_LETTERING_ENCODING_STRING:kotlin.String` When IMS instant lettering is available for a carrier (see `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_INSTANT_LETTERING_AVAILABLE_BOOL:kotlin.String`), determines the character encoding which will be used when determining the length of messages. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_INSTANT_LETTERING_ESCAPED_CHARS_STRING:kotlin.String` When IMS instant lettering is available for a carrier (see `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_INSTANT_LETTERING_AVAILABLE_BOOL:kotlin.String`), determines a list of characters which must be escaped with a backslash '\\' character. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_INSTANT_LETTERING_INVALID_CHARS_STRING:kotlin.String` When IMS instant lettering is available for a carrier (see `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_INSTANT_LETTERING_AVAILABLE_BOOL:kotlin.String`), determines the list of characters which may not be contained in messages. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_INSTANT_LETTERING_LENGTH_LIMIT_INT:kotlin.String` When IMS instant lettering is available for a carrier (see `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_INSTANT_LETTERING_AVAILABLE_BOOL:kotlin.String`), the length limit for messages. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_METERED_APN_TYPES_STRINGS:kotlin.String` A string array indicating the default APN types that are metered by the carrier. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_METERED_ROAMING_APN_TYPES_STRINGS:kotlin.String` A string array indicating the default APN types that are roaming-metered by the carrier. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_NAME_OVERRIDE_BOOL:kotlin.String` Unconditionally override the carrier name string using #KEY_CARRIER_NAME_STRING. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_NAME_STRING:kotlin.String` String to identify carrier name in CarrierConfig app. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_NR_AVAILABILITIES_INT_ARRAY:kotlin.String` A list of carrier nr availability is used to determine whether the carrier enable the non-standalone (NSA) mode of 5G NR, standalone (SA) mode of 5G NR |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_PROVISIONS_WIFI_MERGED_NETWORKS_BOOL:kotlin.String` Indicates whether or not the carrier will provision merged carrier Wi-Fi offload networks. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_RCS_PROVISIONING_REQUIRED_BOOL:kotlin.String` Flag specifying whether provisioning is required for RCS. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_ROAMING_NTN_CONNECT_TYPE_INT:kotlin.String` Indicates carrier roaming non-terrestrial network SatelliteManager. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_ROAMING_NTN_EMERGENCY_CALL_TO_SATELLITE_HANDOVER_TYPE_INT:kotlin.String` Indicates carrier roaming non-terrestrial network emergency call handover type that the device will use to perform a handover between ESOS or T911. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_ROAMING_SATELLITE_DEFAULT_SERVICES_INT_ARRAY:kotlin.String` An int array that contains default capabilities for carrier enabled satellite roaming. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_ROAMING_SATELLITE_T911_TO_ESOS_HANDOVER_SUPPORTED_BOOL:kotlin.String` Indicate whether carrier roaming satellite supports handover from T911 to ESOS. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_SERVICE_NAME_STRING_ARRAY:kotlin.String` String array containing the list of names for service numbers provided by carriers. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_SERVICE_NUMBER_STRING_ARRAY:kotlin.String` String array containing the list of service numbers provided by carriers. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_SETTINGS_ACTIVITY_COMPONENT_NAME_STRING:kotlin.String` Flatten `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` of the carrier's settings activity. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_SETTINGS_ENABLE_BOOL:kotlin.String` Display carrier settings menu if true |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_SUPPORTED_SATELLITE_NOTIFICATION_HYSTERESIS_SEC_INT:kotlin.String` The carrier roaming non-terrestrial network hysteresis time in seconds. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_SUPPORTED_SATELLITE_SERVICES_PER_PROVIDER_BUNDLE:kotlin.String` A PersistableBundle that contains a list of key-value pairs, where the values are integer arrays. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_SUPPORTS_OPP_DATA_AUTO_PROVISIONING_BOOL:kotlin.String` Configuration to indicate that the carrier supports opportunistic data auto provisioning. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_SUPPORTS_SS_OVER_UT_BOOL:kotlin.String` Flag indicating whether or not the carrier supports Supplementary Services over the UT interface for this subscription. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_SUPPORTS_TETHERING_BOOL:kotlin.String` Flag indicating if the carrier supports tethering of mobile data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_USE_IMS_FIRST_FOR_EMERGENCY_BOOL:kotlin.String` Flag specifying whether IMS should be the first phone attempted for E911 even if the phone is not in service. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_USSD_METHOD_INT:kotlin.String` Specify the method of selection for UE sending USSD requests. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_UT_PROVISIONING_REQUIRED_BOOL:kotlin.String` Flag indicating whether or not the IMS MmTel UT capability requires carrier provisioning before it can be set as enabled. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_VOLTE_AVAILABLE_BOOL:kotlin.String` Flag specifying whether VoLTE should be available for carrier, independent of carrier provisioning. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_VOLTE_OVERRIDE_WFC_PROVISIONING_BOOL:kotlin.String` Flag specifying if WFC provisioning depends on VoLTE provisioning. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_VOLTE_PROVISIONED_BOOL:kotlin.String` This flag specifies whether VoLTE availability is based on provisioning. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_VOLTE_PROVISIONING_REQUIRED_BOOL:kotlin.String` Flag specifying whether provisioning is required for VoLTE, Video Telephony, and WiFi Calling. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_VOLTE_TTY_SUPPORTED_BOOL:kotlin.String` Flag specifying whether VoLTE TTY is supported. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_VT_AVAILABLE_BOOL:kotlin.String` Flag specifying whether video telephony is available for carrier. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_VVM_PACKAGE_NAME_STRING:kotlin.String` The package name of the carrier's visual voicemail app to ensure that dialer visual voicemail and carrier visual voicemail are not active at the same time. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_VVM_PACKAGE_NAME_STRING_ARRAY:kotlin.String` A list of the carrier's visual voicemail app package names to ensure that dialer visual voicemail and carrier visual voicemail are not active at the same time. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_WFC_IMS_AVAILABLE_BOOL:kotlin.String` Flag specifying whether WFC over IMS should be available for carrier: independent of carrier provisioning. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_WFC_SUPPORTS_WIFI_ONLY_BOOL:kotlin.String` Flag specifying whether WFC over IMS supports the "wifi only" option. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CDMA_3WAYCALL_FLASH_DELAY_INT:kotlin.String` For carriers which require an empty flash to be sent before sending the normal 3-way calling flash, the duration in milliseconds of the empty flash to send. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CDMA_DTMF_TONE_DELAY_INT:kotlin.String` Specifies the amount of gap to be added in millis between postdial DTMF tones. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CDMA_NONROAMING_NETWORKS_STRING_ARRAY:kotlin.String` Override the platform's notion of a network operator being considered non roaming. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CDMA_ROAMING_MODE_INT:kotlin.String` The CDMA roaming mode (aka CDMA system select). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CDMA_ROAMING_NETWORKS_STRING_ARRAY:kotlin.String` Override the platform's notion of a network operator being considered roaming. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CELLULAR_SERVICE_CAPABILITIES_INT_ARRAY:kotlin.String` An array of cellular services supported by a subscription. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CELLULAR_USAGE_SETTING_INT:kotlin.String` Controls the cellular usage setting. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CHECK_PRICING_WITH_CARRIER_FOR_DATA_ROAMING_BOOL:kotlin.String` Determines whether we should show a warning asking the user to check with their carrier on pricing when the user enabled data roaming, default to false. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CI_ACTION_ON_SYS_UPDATE_BOOL:kotlin.String` Flag specifying whether an additional (client initiated) intent needs to be sent on System update |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CI_ACTION_ON_SYS_UPDATE_EXTRA_STRING:kotlin.String` Extra to be included in the intent sent for additional action on System update |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CI_ACTION_ON_SYS_UPDATE_EXTRA_VAL_STRING:kotlin.String` Value of extra included in intent sent for additional action on System update |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CI_ACTION_ON_SYS_UPDATE_INTENT_STRING:kotlin.String` Intent to be sent for the additional action on System update |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CONFIG_IMS_MMTEL_PACKAGE_OVERRIDE_STRING:kotlin.String` The package name containing the ImsService that will be bound to the telephony framework to support IMS MMTEL feature functionality instead of the device default ImsService for this subscription. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CONFIG_IMS_PACKAGE_OVERRIDE_STRING:kotlin.String` The package name containing the ImsService that will be bound to the telephony framework to support both IMS MMTEL and RCS feature functionality instead of the device default ImsService for this subscription. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CONFIG_IMS_RCS_PACKAGE_OVERRIDE_STRING:kotlin.String` The package name containing the ImsService that will be bound to the telephony framework to support IMS RCS feature functionality instead of the device default ImsService for this subscription. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CONFIG_PLANS_PACKAGE_OVERRIDE_STRING:kotlin.String` Override the package that will manage `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan` information instead of the `https://developer.android.com/reference/kotlin/android/service/carrier/CarrierService.html#` that defines this value. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CONFIG_TELEPHONY_USE_OWN_NUMBER_FOR_VOICEMAIL_BOOL:kotlin.String` Flag that specifies to use the user's own phone number as the voicemail number when there is no pre-loaded voicemail number on the SIM card. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CONFIG_WIFI_DISABLE_IN_ECBM:kotlin.String` Flag to indicate if Wi-Fi needs to be disabled in ECBM. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CROSS_SIM_SPN_FORMAT_INT:kotlin.String` Indexes of SPN format strings in crossSimSpnFormats. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CSP_ENABLED_BOOL:kotlin.String` If this is true, the SIM card (through Customer Service Profile EF file) will be able to prevent manual operator selection. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_DATA_LIMIT_NOTIFICATION_BOOL:kotlin.String` Controls if the device should automatically notify the user as they reach their cellular data limit. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_DATA_LIMIT_THRESHOLD_BYTES_LONG:kotlin.String` Controls the cellular data limit. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_DATA_RAPID_NOTIFICATION_BOOL:kotlin.String` Controls if the device should automatically notify the user when rapid cellular data usage is observed. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_DATA_SWITCH_VALIDATION_MIN_INTERVAL_MILLIS_LONG:kotlin.String` Data switch validation minimal interval, in milliseconds. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_DATA_SWITCH_VALIDATION_TIMEOUT_LONG:kotlin.String` Upon data switching between subscriptions within a carrier group, if switch depends on validation result, this value defines customized value of how long we wait for validation success before we fail and revoke the switch. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_DATA_WARNING_NOTIFICATION_BOOL:kotlin.String` Controls if the device should automatically notify the user as they reach their cellular data warning. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_DATA_WARNING_THRESHOLD_BYTES_LONG:kotlin.String` Controls the data usage warning. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_DEFAULT_SIM_CALL_MANAGER_STRING:kotlin.String` The default sim call manager to use when the default dialer doesn't implement one. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_DEFAULT_VM_NUMBER_ROAMING_AND_IMS_UNREGISTERED_STRING:kotlin.String` Where there is no preloaded voicemail number on a SIM card, specifies the carrier's default voicemail number while the device is both roaming and not registered for IMS. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_DEFAULT_VM_NUMBER_STRING:kotlin.String` Where there is no preloaded voicemail number on a SIM card, specifies the carrier's default voicemail number. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_DIAL_STRING_REPLACE_STRING_ARRAY:kotlin.String` Specifies a map from dialstrings to replacements for roaming network service numbers which cannot be replaced on the carrier side. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_DISABLE_CDMA_ACTIVATION_CODE_BOOL:kotlin.String` Disables dialing "\*228" (OTASP provisioning) on CDMA carriers where it is not supported or is potentially harmful by locking the SIM to 3G. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_DISABLE_CHARGE_INDICATION_BOOL:kotlin.String` The flag to disable the popup dialog which warns the user of data charges. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_DISABLE_DUN_APN_WHILE_ROAMING_WITH_PRESET_APN_BOOL:kotlin.String` Indicating whether DUN APN should be disabled when the device is roaming. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_DISABLE_SUPPLEMENTARY_SERVICES_IN_AIRPLANE_MODE_BOOL:kotlin.String` Boolean indicating the Supplementary Services(SS) is disable when airplane mode on in the Call Settings menu. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_DISALLOW_ADDING_APN_STRING_ARRAY:kotlin.String` Specifies disallowed substrings for the `https://developer.android.com/reference/kotlin/android/provider/Telephony.Carriers.html#APN:kotlin.String`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_DISCONNECT_CAUSE_PLAY_BUSYTONE_INT_ARRAY:kotlin.String` DisconnectCause array to play busy tone. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_DISPLAY_CALL_STRENGTH_INDICATOR_BOOL:kotlin.String` Determine whether or not to display a call strength indicator for this carrier in the System UI. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_DISPLAY_HD_AUDIO_PROPERTY_BOOL:kotlin.String` Determines whether High Definition audio property is displayed in the dialer UI. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_DROP_VIDEO_CALL_WHEN_ANSWERING_AUDIO_CALL_BOOL:kotlin.String` When `true`, if the user is in an ongoing video call over WIFI and answers an incoming audio call, the video call will be disconnected before the audio call is answered. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_DTMF_TYPE_ENABLED_BOOL:kotlin.String` Flag indicating if dtmf tone type is enabled |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_DURATION_BLOCKING_DISABLED_AFTER_EMERGENCY_INT:kotlin.String` The duration in seconds that platform call and message blocking is disabled after the user contacts emergency services. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_EDITABLE_ENHANCED_4G_LTE_BOOL:kotlin.String` Determine whether user can toggle Enhanced 4G LTE Mode in Settings. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_EDITABLE_VOICEMAIL_NUMBER_BOOL:kotlin.String` Since the default voicemail number is empty, if a SIM card does not have a voicemail number available the user cannot use voicemail. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_EDITABLE_VOICEMAIL_NUMBER_SETTING_BOOL:kotlin.String` Determine whether user can edit voicemail number in Settings. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_EDITABLE_WFC_MODE_BOOL:kotlin.String` Determine whether user can switch Wi-Fi preferred or Cellular preferred in calling preference. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_EDITABLE_WFC_ROAMING_MODE_BOOL:kotlin.String` Determine whether user can change Wi-Fi Calling preference in roaming. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_EMERGENCY_CALL_TO_SATELLITE_T911_HANDOVER_TIMEOUT_MILLIS_INT:kotlin.String` An integer key holds the timeout duration in milliseconds used to determine whether to hand over an emergency call to satellite T911. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_EMERGENCY_MESSAGING_SUPPORTED_BOOL:kotlin.String` Indicate whether a carrier supports emergency messaging. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_EMERGENCY_NOTIFICATION_DELAY_INT:kotlin.String` Time delay (in ms) after which we show the notification for emergency calls, while the device is registered over WFC. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_EMERGENCY_NUMBER_PREFIX_STRING_ARRAY:kotlin.String` Indicates zero or more emergency number prefix(es), because some carrier requires if users dial an emergency number address with a specific prefix, the combination of the prefix and the address is also a valid emergency number to dial. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_ENABLE_4G_OPPORTUNISTIC_NETWORK_SCAN_BOOL:kotlin.String` Controls whether 4G opportunistic networks should be scanned for possible data switch. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_ENABLE_CROSS_SIM_CALLING_ON_OPPORTUNISTIC_DATA_BOOL:kotlin.String` Flag specifying whether cross sim calling on opportunistic data is supported for carrier. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_ENABLE_DIALER_KEY_VIBRATION_BOOL:kotlin.String` If true, enable vibration (haptic feedback) for key presses in the EmergencyDialer activity. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_ENHANCED_4G_LTE_ON_BY_DEFAULT_BOOL:kotlin.String` Sets the default state for the "Enhanced 4G LTE" or "Advanced Calling" mode toggle set by the user. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_ENHANCED_4G_LTE_TITLE_VARIANT_INT:kotlin.String` The index indicates the carrier specified title string of Enhanced 4G LTE Mode settings. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_ESIM_DOWNLOAD_RETRY_BACKOFF_TIMER_SEC_INT:kotlin.String` This timer value is used in the eSIM Exponential Backoff download retry algorithm. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_ESIM_MAX_DOWNLOAD_RETRY_ATTEMPTS_INT:kotlin.String` If eSIM profile download fails then, the number of retry attempts by UE will be based on this configuration. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_FORCE_HOME_NETWORK_BOOL:kotlin.String` Override the platform's notion of a network operator being considered non roaming. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_GSM_DTMF_TONE_DELAY_INT:kotlin.String` Specifies the amount of gap to be added in millis between postdial DTMF tones. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_GSM_NONROAMING_NETWORKS_STRING_ARRAY:kotlin.String` Override the platform's notion of a network operator being considered not roaming. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_GSM_ROAMING_NETWORKS_STRING_ARRAY:kotlin.String` Override the platform's notion of a network operator being considered roaming. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_HAS_IN_CALL_NOISE_SUPPRESSION_BOOL:kotlin.String` Determines if device implements a noise suppression device for in call audio. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_HIDE_CARRIER_NETWORK_SETTINGS_BOOL:kotlin.String` Control whether users can reach the carrier portions of Cellular Network Settings. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_HIDE_ENHANCED_4G_LTE_BOOL:kotlin.String` Determines whether the Enhanced 4G LTE toggle will be shown in the settings. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_HIDE_IMS_APN_BOOL:kotlin.String` Determine whether IMS apn can be shown. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_HIDE_LTE_PLUS_DATA_ICON_BOOL:kotlin.String` Boolean indicating if LTE+ icon should be shown if available. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_HIDE_PREFERRED_NETWORK_TYPE_BOOL:kotlin.String` Determine whether preferred network type can be shown. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_HIDE_PRESET_APN_DETAILS_BOOL:kotlin.String` Flag to hide Preset APN details. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_HIDE_SIM_LOCK_SETTINGS_BOOL:kotlin.String` Control whether users can reach the SIM lock settings. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_HIDE_TTY_HCO_VCO_WITH_RTT_BOOL:kotlin.String` Indicates if the TTY HCO and VCO options should be hidden in the accessibility menu if the device is capable of RTT. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_IGNORE_DATA_ENABLED_CHANGED_FOR_VIDEO_CALLS:kotlin.String` When `true`, changes to the mobile data enabled switch will not cause the VT registration state to change. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_IGNORE_RTT_MODE_SETTING_BOOL:kotlin.String` When `true`, the phone will always tell the IMS stack to keep RTT enabled and determine on a per-call basis (based on extras from the dialer app) whether a call should be an RTT call or not. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_IGNORE_SIM_NETWORK_LOCKED_EVENTS_BOOL:kotlin.String` Flag indicating whether the Phone app should ignore EVENT_SIM_NETWORK_LOCKED events from the Sim. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_IMS_CONFERENCE_SIZE_LIMIT_INT:kotlin.String` Determines the maximum number of participants the carrier supports for a conference call. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_IMS_DTMF_TONE_DELAY_INT:kotlin.String` Specifies the amount of gap to be added in millis between DTMF tones. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_INCLUDE_LTE_FOR_NR_ADVANCED_THRESHOLD_BANDWIDTH_BOOL:kotlin.String` Indicating whether to include LTE cell bandwidths when determining whether the aggregated cell bandwidth meets the required threshold for NR advanced. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_IS_IMS_CONFERENCE_SIZE_ENFORCED_BOOL:kotlin.String` Determines whether a maximum size limit for IMS conference calls is enforced on the device. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_IS_OPPORTUNISTIC_SUBSCRIPTION_BOOL:kotlin.String` A boolean property indicating whether this subscription should be managed as an opportunistic subscription. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_IS_PRIVATE_NETWORK_BOOL:kotlin.String` Controls whether the subscription is used exclusively for private networks. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_LOG_CALLS_ANSWERED_ELSEWHERE_BOOL:kotlin.String` Flag indicating whether to log calls which were answered on another device. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_LOW_BATTERY_ALERT_INTERVAL_INT:kotlin.String` Interval between consecutive battery alert tones, in seconds. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_LOW_BATTERY_ALERT_THRESHOLD_INT:kotlin.String` Battery level threshold (in percentage) to trigger an audio alert. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_LTE_ENABLED_BOOL:kotlin.String` Boolean to decide whether LTE is enabled. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_LTE_RSRQ_THRESHOLDS_INT_ARRAY:kotlin.String` A list of 4 customized LTE Reference Signal Received Quality (RSRQ) thresholds. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_LTE_RSSNR_THRESHOLDS_INT_ARRAY:kotlin.String` A list of 4 customized LTE Reference Signal Signal to Noise Ratio (RSSNR) thresholds. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MDN_IS_ADDITIONAL_VOICEMAIL_NUMBER_BOOL:kotlin.String` When checking if a given number is the voicemail number, if this flag is true then in addition to comparing the given number to the voicemail number, we also compare it to the mdn. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MMS_ALIAS_ENABLED_BOOL:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MMS_ALIAS_MAX_CHARS_INT:kotlin.String` <br /> |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MMS_ALIAS_MIN_CHARS_INT:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MMS_ALLOW_ATTACH_AUDIO_BOOL:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MMS_APPEND_TRANSACTION_ID_BOOL:kotlin.String` <br /> |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MMS_CLOSE_CONNECTION_BOOL:kotlin.String` If true, add "Connection: close" header to MMS HTTP requests so the connection is immediately closed (disabling keep-alive). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MMS_EMAIL_GATEWAY_NUMBER_STRING:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MMS_GROUP_MMS_ENABLED_BOOL:kotlin.String` <br /> |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MMS_HTTP_PARAMS_STRING:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MMS_HTTP_SOCKET_TIMEOUT_INT:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MMS_MAX_IMAGE_HEIGHT_INT:kotlin.String` <br /> |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MMS_MAX_IMAGE_WIDTH_INT:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MMS_MAX_MESSAGE_SIZE_INT:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MMS_MAX_NTN_PAYLOAD_SIZE_BYTES_INT:kotlin.String` Maximum size in bytes of the PDU to send or download when connected to a non-terrestrial network. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MMS_MESSAGE_TEXT_MAX_SIZE_INT:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MMS_MMS_DELIVERY_REPORT_ENABLED_BOOL:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MMS_MMS_ENABLED_BOOL:kotlin.String` <br /> |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MMS_MMS_READ_REPORT_ENABLED_BOOL:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MMS_MULTIPART_SMS_ENABLED_BOOL:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MMS_NAI_SUFFIX_STRING:kotlin.String` <br /> |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MMS_NETWORK_RELEASE_TIMEOUT_MILLIS_INT:kotlin.String` Waiting time in milliseconds used before releasing an MMS data call. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MMS_NOTIFY_WAP_MMSC_ENABLED_BOOL:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MMS_RECIPIENT_LIMIT_INT:kotlin.String` <br /> |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MMS_SEND_MULTIPART_SMS_AS_SEPARATE_MESSAGES_BOOL:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MMS_SHOW_CELL_BROADCAST_APP_LINKS_BOOL:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MMS_SMS_DELIVERY_REPORT_ENABLED_BOOL:kotlin.String` <br /> |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MMS_SMS_TO_MMS_TEXT_LENGTH_THRESHOLD_INT:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MMS_SMS_TO_MMS_TEXT_THRESHOLD_INT:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MMS_SUBJECT_MAX_LENGTH_INT:kotlin.String` <br /> |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MMS_SUPPORT_HTTP_CHARSET_HEADER_BOOL:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MMS_SUPPORT_MMS_CONTENT_DISPOSITION_BOOL:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MMS_UA_PROF_TAG_NAME_STRING:kotlin.String` <br /> |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MMS_UA_PROF_URL_STRING:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MMS_USER_AGENT_STRING:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MONTHLY_DATA_CYCLE_DAY_INT:kotlin.String` The day of the month (1-31) on which the data cycle rolls over. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_NTN_5G_NR_SSRSRP_THRESHOLDS_INT_ARRAY:kotlin.String` This threshold is used when connected to a non-terrestrial NR network. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_NTN_5G_NR_SSRSRQ_THRESHOLDS_INT_ARRAY:kotlin.String` This threshold is used when connected to a non-terrestrial NR network. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_NTN_5G_NR_SSSINR_THRESHOLDS_INT_ARRAY:kotlin.String` This threshold is used when connected to a non-terrestrial NR network. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_NTN_EUTRAN_RSRP_HYSTERESIS_DB_INT:kotlin.String` An interval in dB for E-UTRAN reference signal received power (RSRP) measurement type defining the required magnitude change between reports when connected to a non-terrestrial LTE network. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_NTN_EUTRAN_RSRQ_HYSTERESIS_DB_INT:kotlin.String` An interval in dB for E-UTRAN reference signal received quality (RSRQ) measurement type defining the required magnitude change between reports when connected to a non-terrestrial LTE network. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_NTN_EUTRAN_RSSNR_HYSTERESIS_DB_INT:kotlin.String` An interval in dB for E-UTRAN reference signal to noise and interference ratio (RSSNR) measurement type defining the required magnitude change between reports when connected to a non-terrestrial LTE network. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_NTN_EUTRAN_SIGNAL_REPORTING_HYSTERESIS_MS_INT:kotlin.String` An interval in milliseconds for E-UTRAN signal reporting measurement type defining the required time change between reports when connected to a non-terrestrial LTE network. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_NTN_LTE_RSRP_THRESHOLDS_INT_ARRAY:kotlin.String` This threshold is used when connected to a non-terrestrial LTE network. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_NTN_LTE_RSRQ_THRESHOLDS_INT_ARRAY:kotlin.String` This threshold is used when connected to a non-terrestrial LTE network. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_NTN_LTE_RSSNR_THRESHOLDS_INT_ARRAY:kotlin.String` This threshold is used when connected to a non-terrestrial LTE network. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_NTN_NGRAN_SIGNAL_REPORTING_HYSTERESIS_MS_INT:kotlin.String` An interval in milliseconds for NG-RAN signal reporting measurement type defining the required time change between reports when connected to a non-terrestrial NR network. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_NTN_NGRAN_SSRSRP_HYSTERESIS_DB_INT:kotlin.String` An interval in dB for NG-RAN reference signal received power (SSRSRP) measurement type defining the required magnitude change between reports when connected to a non-terrestrial NR network. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_NTN_NGRAN_SSRSRQ_HYSTERESIS_DB_INT:kotlin.String` An interval in dB for NG-RAN reference signal received quality (SSRSRQ) measurement type defining the required magnitude change between reports when connected to a non-terrestrial NR network. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_NTN_NGRAN_SSSINR_HYSTERESIS_DB_INT:kotlin.String` An interval in dB for NG-RAN reference signal to noise and interference ratio (SSSINR) measurement type defining the required magnitude change between reports when connected to a non-terrestrial NR network. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_ONLY_AUTO_SELECT_IN_HOME_NETWORK_BOOL:kotlin.String` Only allow auto selection in Advanced Network Settings when in home network. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_ONLY_SINGLE_DC_ALLOWED_INT_ARRAY:kotlin.String` List of network type constants which support only a single data connection at a time. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_OPERATOR_SELECTION_EXPAND_BOOL:kotlin.String` Control whether users can choose a network operator. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_OPPORTUNISTIC_NETWORK_BACKOFF_TIME_LONG:kotlin.String` Controls back off time in milli seconds for switching back to opportunistic subscription. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_OPPORTUNISTIC_NETWORK_DATA_SWITCH_EXIT_HYSTERESIS_TIME_LONG:kotlin.String` Controls hysteresis time in milli seconds for which OpportunisticNetworkService will wait before switching data from opportunistic network to primary network. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_OPPORTUNISTIC_NETWORK_DATA_SWITCH_HYSTERESIS_TIME_LONG:kotlin.String` Controls hysteresis time in milli seconds for which OpportunisticNetworkService will wait before switching data to an opportunistic network. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_OPPORTUNISTIC_NETWORK_ENTRY_OR_EXIT_HYSTERESIS_TIME_LONG:kotlin.String` Controls hysteresis time in milli seconds for which OpportunisticNetworkService will wait before attaching to a network. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_OPPORTUNISTIC_NETWORK_ENTRY_THRESHOLD_BANDWIDTH_INT:kotlin.String` Controls bandwidth threshold in Kbps at which OpportunisticNetworkService will decide whether the opportunistic network is good enough for internet data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_OPPORTUNISTIC_NETWORK_ENTRY_THRESHOLD_RSRP_INT:kotlin.String` Controls RSRP threshold, in dBm, at which OpportunisticNetworkService will decide whether the opportunistic network is good enough for internet data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_OPPORTUNISTIC_NETWORK_ENTRY_THRESHOLD_RSSNR_INT:kotlin.String` Controls RSSNR threshold, in dB, at which OpportunisticNetworkService will decide whether the opportunistic network is good enough for internet data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_OPPORTUNISTIC_NETWORK_EXIT_THRESHOLD_RSRP_INT:kotlin.String` Controls RSRP threshold, in dBm, below which OpportunisticNetworkService will decide whether the opportunistic network available is not good enough for internet data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_OPPORTUNISTIC_NETWORK_EXIT_THRESHOLD_RSSNR_INT:kotlin.String` Controls RSSNR threshold, in dB, below which OpportunisticNetworkService will decide whether the opportunistic network available is not good enough for internet data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_OPPORTUNISTIC_NETWORK_MAX_BACKOFF_TIME_LONG:kotlin.String` Controls the max back off time in milli seconds for switching back to opportunistic subscription. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_OPPORTUNISTIC_NETWORK_PING_PONG_TIME_LONG:kotlin.String` Controls the ping pong determination of opportunistic network. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_OPP_AUTO_DATA_SWITCH_POLICY_INT:kotlin.String` Auto data network switch policies between primary and opportunistic profiles in the same subscription group. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_OVERRIDE_WFC_ROAMING_MODE_WHILE_USING_NTN_BOOL:kotlin.String` Determine whether to override roaming Wi-Fi Calling preference when device is connected to non-terrestrial network. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_PARAMETERS_USED_FOR_NTN_LTE_SIGNAL_BAR_INT:kotlin.String` This threshold is used when connected to a non-terrestrial LTE network. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_PING_TEST_BEFORE_DATA_SWITCH_BOOL:kotlin.String` Controls whether to do ping test before switching data to opportunistic network. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_PREFER_2G_BOOL:kotlin.String` Used in the Preferred Network Types menu to determine if the 2G option is displayed. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_PREFER_3G_VISIBILITY_BOOL:kotlin.String` Used in the Preferred Network Types menu to determine if the 3G option is displayed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_PREMIUM_CAPABILITY_MAXIMUM_DAILY_NOTIFICATION_COUNT_INT:kotlin.String` The maximum number of times in a day that we display the notification for a performance boost via premium capabilities when `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#purchasePremiumCapability(kotlin.Int,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` returns a failure due to user action or timeout. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_PREMIUM_CAPABILITY_MAXIMUM_MONTHLY_NOTIFICATION_COUNT_INT:kotlin.String` The maximum number of times in a month that we display the notification for a performance boost via premium capabilities when `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#purchasePremiumCapability(kotlin.Int,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` returns a failure due to user action or timeout. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_PREMIUM_CAPABILITY_NETWORK_SETUP_TIME_MILLIS_LONG:kotlin.String` The amount of time in milliseconds within which the network must set up a slicing configuration for the premium capability after `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#purchasePremiumCapability(kotlin.Int,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` returns `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_SUCCESS:kotlin.Int`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_PREMIUM_CAPABILITY_NOTIFICATION_BACKOFF_HYSTERESIS_TIME_MILLIS_LONG:kotlin.String` The amount of time in milliseconds that the notification for a performance boost via premium capabilities should be blocked when `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#purchasePremiumCapability(kotlin.Int,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` returns a failure due to user action or timeout. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_PREMIUM_CAPABILITY_NOTIFICATION_DISPLAY_TIMEOUT_MILLIS_LONG:kotlin.String` The amount of time in milliseconds the notification for a performance boost via premium capabilities will be visible to the user after `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#purchasePremiumCapability(kotlin.Int,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` requests user action to purchase the boost from the carrier. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_PREMIUM_CAPABILITY_PURCHASE_CONDITION_BACKOFF_HYSTERESIS_TIME_MILLIS_LONG:kotlin.String` The amount of time in milliseconds that the purchase request should be throttled when `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#purchasePremiumCapability(kotlin.Int,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` returns a failure due to the carrier. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_PREMIUM_CAPABILITY_PURCHASE_URL_STRING:kotlin.String` The URL to redirect to when the user clicks on the notification for a performance boost via premium capabilities after applications call `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#purchasePremiumCapability(kotlin.Int,%20java.util.concurrent.Executor,%20java.util.function.Consumer)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_PREMIUM_CAPABILITY_SUPPORTED_ON_LTE_BOOL:kotlin.String` Whether to allow premium capabilities to be purchased when the device is connected to LTE. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_PREVENT_CLIR_ACTIVATION_AND_DEACTIVATION_CODE_BOOL:kotlin.String` Flag specifying whether to prevent sending CLIR activation("\*31#") and deactivation("#31#") code only without dialing number. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_RADIO_RESTART_FAILURE_CAUSES_INT_ARRAY:kotlin.String` A list of failure cause codes that will trigger a modem restart when telephony receiving one of those during data setup. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_RATCHET_NR_ADVANCED_BANDWIDTH_IF_RRC_IDLE_BOOL:kotlin.String` Indicating whether to ratchet the aggregated cell bandwidths on receiving new values when the device is in RRC IDLE mode. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_RCS_CONFIG_SERVER_URL_STRING:kotlin.String` The RCS configuration server URL. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_READ_ONLY_APN_FIELDS_STRING_ARRAY:kotlin.String` APN fields that user is not allowed to modify. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_READ_ONLY_APN_TYPES_STRING_ARRAY:kotlin.String` APN types that user is not allowed to modify. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_REGIONAL_SATELLITE_EARFCN_BUNDLE:kotlin.String` A PersistableBundle that contains a list of key-value pairs, where the values are integer arrays. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_REMOVE_SATELLITE_PLMN_IN_MANUAL_NETWORK_SCAN_BOOL:kotlin.String` Indicating whether plmns associated with carrier satellite can be exposed to user when manually scanning available cellular network. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_REQUIRE_ENTITLEMENT_CHECKS_BOOL:kotlin.String` Flag to require or skip entitlement checks. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_RESTART_RADIO_ON_PDP_FAIL_REGULAR_DEACTIVATION_BOOL:kotlin.String` Flag indicating whether radio is to be restarted on error PDP_FAIL_REGULAR_DEACTIVATION This is false by default. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_RTT_AUTO_UPGRADE_BOOL:kotlin.String` Indicates if the carrier supports auto-upgrading a call to RTT when receiving a call from a RTT-supported device. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_RTT_DOWNGRADE_SUPPORTED_BOOL:kotlin.String` Indicates if the carrier supports downgrading a RTT call to a voice call during the call. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_RTT_SUPPORTED_BOOL:kotlin.String` Flag indicating whether the carrier supports RTT over IMS. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_RTT_SUPPORTED_FOR_VT_BOOL:kotlin.String` Indicates if the carrier supports RTT during a video call. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_RTT_SUPPORTED_WHILE_ROAMING_BOOL:kotlin.String` Indicates whether RTT is supported while roaming. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_RTT_UPGRADE_SUPPORTED_BOOL:kotlin.String` Indicates if the carrier supports upgrading a voice call to an RTT call during the call. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_RTT_UPGRADE_SUPPORTED_FOR_DOWNGRADED_VT_CALL_BOOL:kotlin.String` Indicates if the carrier supports upgrading a call that was previously a VT call to RTT. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SATELLITE_ATTACH_SUPPORTED_BOOL:kotlin.String` This config enables modem to scan satellite PLMNs specified as per `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_SUPPORTED_SATELLITE_SERVICES_PER_PROVIDER_BUNDLE:kotlin.String` and attach to same in case cellular networks are not enabled. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SATELLITE_CONFIGS_PER_PLMN_BUNDLE:kotlin.String` A PersistableBundle that contains a list of key-value pairs, where keys are satellite provider PLMNs and values are bundles containing satellite configurations for that PLMN. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SATELLITE_CONNECTED_NOTIFICATION_THROTTLE_MILLIS_INT:kotlin.String` Satellite notification display restriction reset time in seconds. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SATELLITE_CONNECTION_HYSTERESIS_SEC_INT:kotlin.String` The carrier-enabled satellite connection hysteresis time in seconds for which the device continues in satellite mode after it loses the connection with the satellite network. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SATELLITE_DATA_SUPPORT_MODE_INT:kotlin.String` Indicates what kind of traffic an `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities.html#NET_CAPABILITY_NOT_RESTRICTED:kotlin.Int` satellite network can possibly support. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SATELLITE_DISPLAY_NAME_STRING:kotlin.String` The display name that will be used for satellite functionality within the UI. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SATELLITE_ENTITLEMENT_APP_NAME_STRING:kotlin.String` Indicates the appName that is used when querying the entitlement server for satellite. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SATELLITE_ENTITLEMENT_STATUS_REFRESH_DAYS_INT:kotlin.String` An integer key holds the time interval for refreshing or re-querying the satellite entitlement status from the entitlement server to ensure it is the latest. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SATELLITE_ENTITLEMENT_SUPPORTED_BOOL:kotlin.String` This configuration enables device to query the entitlement server to get the satellite configuration. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SATELLITE_ESOS_SUPPORTED_BOOL:kotlin.String` Indicate whether carrier roaming to satellite is using ESOS (Emergency SOS) which connects to an emergency provider instead of PSAP (Public Safety Answering Point) for emergency messaging. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SATELLITE_IGNORE_DATA_ROAMING_SETTING_BOOL:kotlin.String` Determines whether data roaming off setting should be ignored and satellite data should be allowed even when data roaming is off. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SATELLITE_INFORMATION_REDIRECT_URL_STRING:kotlin.String` URL to redirect user to get more information about the carrier support for satellite. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SATELLITE_NIDD_APN_NAME_STRING:kotlin.String` Defines the NIDD (Non-IP Data Delivery) APN to be used for carrier roaming to satellite attachment. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SATELLITE_ROAMING_ESOS_INACTIVITY_TIMEOUT_SEC_INT:kotlin.String` An integer key holds the timeout duration in seconds used to determine whether to exit ESOS mode and start TN scanning. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SATELLITE_ROAMING_P2P_SMS_INACTIVITY_TIMEOUT_SEC_INT:kotlin.String` An integer key holds the timeout duration in seconds used to determine whether to exit P2P SMS mode and start TN scanning. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SATELLITE_ROAMING_P2P_SMS_SUPPORTED_BOOL:kotlin.String` Indicate whether carrier roaming to satellite is using P2P SMS. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SATELLITE_ROAMING_SCREEN_OFF_INACTIVITY_TIMEOUT_SEC_INT:kotlin.String` An integer key holds the timeout duration in seconds used to determine whether to exit carrier-roaming NB-IOT satellite mode. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SATELLITE_ROAMING_TURN_OFF_SESSION_FOR_EMERGENCY_CALL_BOOL:kotlin.String` Default value `true`, meaning when an emergency call request comes in, if the device is in emergency satellite mode but hasn't sent the first satellite datagram, then exits satellite mode to allow the emergency call to go through. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SATELLITE_SOS_MAX_DATAGRAM_SIZE_BYTES_INT:kotlin.String` This value is used to set the max datagram size in bytes. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SATELLITE_SUPPORTED_DISASTER_PLMN_STRING_ARRAY:kotlin.String` A string array containing the list of supported disaster satellite PLMNs. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SATELLITE_SUPPORTED_EMERGENCY_PLMN_STRING_ARRAY:kotlin.String` A string array containing the list of supported emergency satellite PLMNs. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SATELLITE_SUPPORTED_MSG_APPS_STRING_ARRAY:kotlin.String` A string array containing the list of messaging apps that support satellite. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SHOW_4G_FOR_3G_DATA_ICON_BOOL:kotlin.String` Boolean indicating if default data account should show 4G icon when in 3G. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SHOW_4G_FOR_LTE_DATA_ICON_BOOL:kotlin.String` Boolean indicating if default data account should show LTE or 4G icon. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SHOW_APN_SETTING_CDMA_BOOL:kotlin.String` Show APN Settings for some CDMA carriers |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SHOW_AVOID_BAD_WIFI_TOGGLE_BOOL:kotlin.String` Used to decide if the device's UI should present the "avoid bad Wi-Fi" from carrier config. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SHOW_BLOCKING_PAY_PHONE_OPTION_BOOL:kotlin.String` Flag specifying whether to show blocking pay phone option in blocked numbers screen. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SHOW_CALL_BLOCKING_DISABLED_NOTIFICATION_ALWAYS_BOOL:kotlin.String` Flag specifying whether to show notification(call blocking disabled) when Enhanced Call Blocking(KEY_SUPPORT_ENHANCED_CALL_BLOCKING_BOOL) is enabled and making emergency call. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SHOW_CDMA_CHOICES_BOOL:kotlin.String` Show cdma network mode choices 1x, 3G, global etc. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SHOW_FORWARDED_NUMBER_BOOL:kotlin.String` Flag specifying whether to show forwarded number on call-in-progress screen. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SHOW_ICCID_IN_SIM_STATUS_BOOL:kotlin.String` Flag specifying whether ICCID is showed in SIM Status screen, default to false. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SHOW_IMS_REGISTRATION_STATUS_BOOL:kotlin.String` Flag specifying whether IMS registration state menu is shown in Status Info setting, default to false. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SHOW_ONSCREEN_DIAL_BUTTON_BOOL:kotlin.String` If true, show an onscreen "Dial" button in the dialer. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SHOW_ROAMING_INDICATOR_BOOL:kotlin.String` Config to show the roaming indicator (i.e. the "R" icon) from the status bar when roaming. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SHOW_SIGNAL_STRENGTH_IN_SIM_STATUS_BOOL:kotlin.String` Flag specifying whether the `https://developer.android.com/reference/kotlin/android/telephony/SignalStrength` is shown in the SIM Status screen. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SHOW_VIDEO_CALL_CHARGES_ALERT_DIALOG_BOOL:kotlin.String` Flag specifying whether to show an alert dialog for video call charges. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SHOW_WFC_LOCATION_PRIVACY_POLICY_BOOL:kotlin.String` Determines whether wifi calling location privacy policy is shown. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SIMPLIFIED_NETWORK_SETTINGS_BOOL:kotlin.String` Control whether users receive a simplified network settings UI and improved network selection. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SIM_COUNTRY_ISO_OVERRIDE_STRING:kotlin.String` String to override sim country iso. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SIM_NETWORK_UNLOCK_ALLOW_DISMISS_BOOL:kotlin.String` Flag indicating whether the Phone app should provide a "Dismiss" button on the SIM network unlock screen. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SMDP_SERVER_ADDRESS_STRING:kotlin.String` SMDP+ server address for downloading opportunistic eSIM profile. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SMS_REQUIRES_DESTINATION_NUMBER_CONVERSION_BOOL:kotlin.String` Determines if the carrier requires converting the destination number before sending out an SMS. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SUBSCRIPTION_GROUP_UUID_STRING:kotlin.String` The UUID of a Group of related subscriptions in which to place the current subscription. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SUPPORTED_PREMIUM_CAPABILITIES_INT_ARRAY:kotlin.String` A list of premium capabilities the carrier supports. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SUPPORTS_BUSINESS_CALL_COMPOSER_BOOL:kotlin.String` Indicates if the carrier supports a business call composer. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SUPPORTS_CALL_COMPOSER_BOOL:kotlin.String` Indicates if the carrier supports call composer. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SUPPORTS_CUSTOMIZED_RINGING_SIGNAL_BOOL:kotlin.String` Indicates if the carrier supports Customized Ringing Signal (CRS). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SUPPORTS_DEVICE_TO_DEVICE_COMMUNICATION_USING_DTMF_BOOL:kotlin.String` Indicates whether the carrier supports the use of DTMF digits A-D for the purpose of device to device communication while in a call. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SUPPORTS_DEVICE_TO_DEVICE_COMMUNICATION_USING_RTP_BOOL:kotlin.String` Indicates whether the carrier supports the use of RFC8285 compliant RTP header extensions for the purpose of device to device communication while in a call. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SUPPORTS_SDP_NEGOTIATION_OF_D2D_RTP_HEADER_EXTENSIONS_BOOL:kotlin.String` Indicates whether the carrier supports the negotiations of RFC8285 compliant RTP header extensions supported on a call during the Session Description Protocol (SDP). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SUPPORTS_UNIDIRECTIONAL_VIDEO_SERVICE_BOOL:kotlin.String` Indicates if the carrier supports a unidirectional video service call (UVS). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SUPPORTS_VIDEO_RINGBACK_BOOL:kotlin.String` Indicates if the carrier supports a video color ring back tone call (CRBT). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SUPPORT_3GPP_CALL_FORWARDING_WHILE_ROAMING_BOOL:kotlin.String` Indicates whether the carrier supports 3gpp call forwarding MMI codes while roaming. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SUPPORT_ADD_CONFERENCE_PARTICIPANTS_BOOL:kotlin.String` Determines whether conference participants can be added to existing call to form an adhoc conference call (in contrast to merging calls to form a conference). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SUPPORT_ADHOC_CONFERENCE_CALLS_BOOL:kotlin.String` Determines whether adhoc conference calls are supported by a carrier. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SUPPORT_CLIR_NETWORK_DEFAULT_BOOL:kotlin.String` Flag indicating whether to support "Network default" option in Caller ID settings for Calling Line Identification Restriction (CLIR). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SUPPORT_CONFERENCE_CALL_BOOL:kotlin.String` Determines whether conference calls are supported by a carrier. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SUPPORT_EMERGENCY_SMS_OVER_IMS_BOOL:kotlin.String` Flag indicating whether or not sending emergency SMS messages over IMS is supported when in LTE/limited LTE (Emergency only) service mode. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SUPPORT_ENHANCED_CALL_BLOCKING_BOOL:kotlin.String` Determines whether to enable enhanced call blocking feature on the device. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SUPPORT_IMS_CONFERENCE_EVENT_PACKAGE_BOOL:kotlin.String` Determines whether the IMS conference merge process supports and returns its participants data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SUPPORT_MULTI_PARTY_ANCHOR_CONFERENCE_BOOL:kotlin.String` Determine whether multi-party anchor conference calls are supported by a carrier. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SUPPORT_PAUSE_IMS_VIDEO_CALLS_BOOL:kotlin.String` For IMS video over LTE calls, determines whether video pause signalling is supported. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SUPPORT_PHONE_NUMBER_SOURCE_TS43_BOOL:kotlin.String` Determines if the carrier supports retrieving the phone number via the TS. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SUPPORT_SWAP_AFTER_MERGE_BOOL:kotlin.String` After a CDMA conference call is merged, the swap button should be displayed. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SUPPORT_TDSCDMA_BOOL:kotlin.String` Boolean to decide whether TD-SCDMA is supported. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SUPPORT_TDSCDMA_ROAMING_NETWORKS_STRING_ARRAY:kotlin.String` A list of mcc/mnc that support TD-SCDMA for device when connect to the roaming network. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SWITCH_DATA_TO_PRIMARY_IF_PRIMARY_IS_OOS_BOOL:kotlin.String` Controls whether to switch data to primary from opportunistic subscription if primary is out of service. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_TREAT_DOWNGRADED_VIDEO_CALLS_AS_VIDEO_CALLS_BOOL:kotlin.String` Flag indicating whether some telephony logic will treat a call which was formerly a video call as if it is still a video call. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_TTY_SUPPORTED_BOOL:kotlin.String` Boolean flag indicating whether the carrier supports TTY. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_UNLOGGABLE_NUMBERS_STRING_ARRAY:kotlin.String` A string array containing numbers that shouldn't be included in the call log. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_USE_ACS_FOR_RCS_BOOL:kotlin.String` Indicates if auto-configuration server is used for the RCS config Reference: GSMA RCC. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_USE_HFA_FOR_PROVISIONING_BOOL:kotlin.String` CDMA activation goes through HFA |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_USE_IP_FOR_CALLING_INDICATOR_BOOL:kotlin.String` Determines whether or not to use (IP) data connectivity as a supplemental condition to control the visibility of the no-calling indicator for this carrier in the System UI. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_USE_OTASP_FOR_PROVISIONING_BOOL:kotlin.String` CDMA activation goes through OTASP. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_USE_RCS_PRESENCE_BOOL:kotlin.String` Flag indicating whether or not the carrier supports the periodic exchange of phone numbers in the user's address book with the carrier's presence server in order to retrieve the RCS capabilities for each contact used in the RCS User Capability Exchange (UCE) procedure. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_USE_RCS_SIP_OPTIONS_BOOL:kotlin.String` Flag indicating whether the carrier supports RCS SIP OPTIONS indication for User Capability Exchange (UCE). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_USE_WFC_HOME_NETWORK_MODE_IN_ROAMING_NETWORK_BOOL:kotlin.String` Flag specifying whether the carrier will use the WFC home network mode in roaming network. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_VOICEMAIL_NOTIFICATION_PERSISTENT_BOOL:kotlin.String` Determine whether the voicemail notification is persistent in the notification bar. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_VOICE_PRIVACY_DISABLE_UI_BOOL:kotlin.String` If true, removes the Voice Privacy option from Call Settings |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_VOLTE_REPLACEMENT_RAT_INT:kotlin.String` If Voice Radio Technology is RIL_RADIO_TECHNOLOGY_LTE:14 or RIL_RADIO_TECHNOLOGY_UNKNOWN:0 this is the value that should be used instead. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_VONR_ENABLED_BOOL:kotlin.String` Flag specifying whether VoNR should be enabled for carrier. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_VONR_ON_BY_DEFAULT_BOOL:kotlin.String` Boolean indicating the default VoNR user preference setting. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_VONR_SETTING_VISIBILITY_BOOL:kotlin.String` Boolean indicating if the VoNR setting is visible in the Call Settings menu. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_VT_UPGRADE_SUPPORTED_FOR_DOWNGRADED_RTT_CALL_BOOL:kotlin.String` Indicates if the carrier supports upgrading a call that was previously an RTT call to VT. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_VVM_CELLULAR_DATA_REQUIRED_BOOL:kotlin.String` Whether cellular data is required to access visual voicemail. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_VVM_CLIENT_PREFIX_STRING:kotlin.String` The default OMTP visual voicemail client prefix to use. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_VVM_DESTINATION_NUMBER_STRING:kotlin.String` The carrier number mobile outgoing (MO) sms messages are sent to. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_VVM_DISABLED_CAPABILITIES_STRING_ARRAY:kotlin.String` A set of capabilities that should not be used even if it is reported by the visual voicemail IMAP CAPABILITY command. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_VVM_LEGACY_MODE_ENABLED_BOOL:kotlin.String` Whether legacy mode should be used when the visual voicemail client is disabled. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_VVM_PORT_NUMBER_INT:kotlin.String` The port through which the mobile outgoing (MO) sms messages are sent through. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_VVM_PREFETCH_BOOL:kotlin.String` Whether to prefetch audio data on new voicemail arrival, defaulted to true. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_VVM_SSL_ENABLED_BOOL:kotlin.String` Whether to use SSL to connect to the visual voicemail IMAP server. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_VVM_TYPE_STRING:kotlin.String` The type of visual voicemail protocol the carrier adheres to. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_WFC_EMERGENCY_ADDRESS_CARRIER_APP_STRING:kotlin.String` The Component Name of the activity that can setup the emergency address for WiFi Calling as per carrier requirement. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_WORLD_MODE_ENABLED_BOOL:kotlin.String` Boolean to decide whether world mode is enabled. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_WORLD_PHONE_BOOL:kotlin.String` Flag indicating if the phone is a world phone |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#OPP_AUTO_DATA_SWITCH_POLICY_DISABLED:kotlin.Int` Auto data network switch policy between primary and opportunistic profiles in the same subscription group: switching is disabled. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#OPP_AUTO_DATA_SWITCH_POLICY_FOLLOW_SYSTEM:kotlin.Int` Auto data network switch policy between primary and opportunistic profiles in the same subscription group: enable all system supported policies. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#OPP_AUTO_DATA_SWITCH_POLICY_FOR_AVAILABILITY:kotlin.Int` Auto data network switch policy between primary and opportunistic profiles in the same subscription group: switch to the network only with better availability. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#OPP_AUTO_DATA_SWITCH_POLICY_FOR_PERFORMANCE:kotlin.Int` Auto data network switch policy between primary and opportunistic profiles in the same subscription group: switch to the network with better data connection performance. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#REMOVE_GROUP_UUID_STRING:kotlin.String` Passing this value as `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SUBSCRIPTION_GROUP_UUID_STRING:kotlin.String` will remove the subscription from a group instead of adding it to a group. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#SATELLITE_DATA_SUPPORT_ALL:kotlin.Int` Support unrestricted satellite network that serves all traffic. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#SATELLITE_DATA_SUPPORT_BANDWIDTH_CONSTRAINED:kotlin.Int` Support unrestricted but bandwidth_constrained traffic on satellite network. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#SATELLITE_DATA_SUPPORT_ONLY_RESTRICTED:kotlin.Int` Doesn't support unrestricted traffic on satellite network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#SERVICE_CLASS_NONE:kotlin.Int` Service class flag if no specific service class is specified. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#SERVICE_CLASS_VOICE:kotlin.Int` Service class flag for voice telephony. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#USSD_OVER_CS_ONLY:kotlin.Int` Only send USSD over CS. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#USSD_OVER_CS_PREFERRED:kotlin.Int` Only send USSD over IMS while CS is out of service, otherwise send USSD over CS. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#USSD_OVER_IMS_ONLY:kotlin.Int` Only send USSD over IMS and disallow silent redial over CS. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#USSD_OVER_IMS_PREFERRED:kotlin.Int` Send USSD over IMS or CS while IMS is out of service or silent redial over CS if needed. |

| Public methods ||
|---|---|
| open [PersistableBundle](../android.os/PersistableBundle.md)? | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#getConfig()()` Gets the configuration values for the default subscription. |
| open [PersistableBundle](../android.os/PersistableBundle.md) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#getConfig(kotlin.String)(vararg keys: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Gets the configuration values of the specified config keys applied for the default subscription. |
| open [PersistableBundle](../android.os/PersistableBundle.md)? | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#getConfigByComponentForSubId(kotlin.String,%20kotlin.Int)(prefix: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, subId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets the configuration values for a component using its prefix. |
| --- | --- |
| open [PersistableBundle](../android.os/PersistableBundle.md)? | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#getConfigForSubId(kotlin.Int)(subId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets the configuration values for a particular subscription, which is associated with a specific SIM card. |
| open [PersistableBundle](../android.os/PersistableBundle.md) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#getConfigForSubId(kotlin.Int,%20kotlin.String)(subId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, vararg keys: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Gets the configuration values of the specified keys for a particular subscription. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#isConfigForIdentifiedCarrier(android.os.PersistableBundle)(bundle: https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#!)` Determines whether a configuration `https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#` obtained from `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#getConfig()` or `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#getConfigForSubId(kotlin.Int)` corresponds to an identified carrier. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#notifyConfigChangedForSubId(kotlin.Int)(subId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Calling this method triggers telephony services to fetch the current carrier configuration. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#registerCarrierConfigChangeListener(java.util.concurrent.Executor,%20android.telephony.CarrierConfigManager.CarrierConfigChangeListener)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.CarrierConfigChangeListener)` Register a `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.CarrierConfigChangeListener` to get a notification when carrier configurations have changed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#unregisterCarrierConfigChangeListener(android.telephony.CarrierConfigManager.CarrierConfigChangeListener)(listener: https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.CarrierConfigChangeListener)` Unregister the `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.CarrierConfigChangeListener` to stop notification on carrier configurations change. |
| --- | --- |

## Constants

### ACTION_CARRIER_CONFIG_CHANGED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_CARRIER_CONFIG_CHANGED: String
```

This intent is broadcast by the system when carrier config changes. An int is specified in `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#EXTRA_SLOT_INDEX:kotlin.String` to indicate the slot index that this is for. An optional int extra `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#EXTRA_SUBSCRIPTION_INDEX:kotlin.String` is included to indicate the subscription index if a valid one is available for the slot index. An optional int extra `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_CARRIER_ID:kotlin.String` is included to indicate the carrier id for the changed carrier configuration. An optional int extra `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_SPECIFIC_CARRIER_ID:kotlin.String` is included to indicate the precise carrier id for the changed carrier configuration.

 Value: "android.telephony.action.CARRIER_CONFIG_CHANGED"

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#getSimCarrierId()`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#getSimSpecificCarrierId()`

### CARRIER_NR_AVAILABILITY_NSA

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CARRIER_NR_AVAILABILITY_NSA: Int
```

Indicates CARRIER_NR_AVAILABILITY_NSA determine that the carrier enable the non-standalone (NSA) mode of 5G NR.

 Value: 1

### CARRIER_NR_AVAILABILITY_SA

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CARRIER_NR_AVAILABILITY_SA: Int
```

Indicates CARRIER_NR_AVAILABILITY_SA determine that the carrier enable the standalone (SA) mode of 5G NR.

 Value: 2

### CARRIER_ROAMING_NTN_CONNECT_AUTOMATIC

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CARRIER_ROAMING_NTN_CONNECT_AUTOMATIC: Int
```

Device can connect to carrier roaming non-terrestrial network automatically.

 Value: 0

### CARRIER_ROAMING_NTN_CONNECT_HYBRID

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CARRIER_ROAMING_NTN_CONNECT_HYBRID: Int
```

Device can connect to carrier roaming non-terrestrial network both automatically and manually i.e. Carrier would support multiple satellite providers with automatical and manually connect capabilities.

 Value: 2

### CARRIER_ROAMING_NTN_CONNECT_MANUAL

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CARRIER_ROAMING_NTN_CONNECT_MANUAL: Int
```

Device can connect to carrier roaming non-terrestrial network only if user manually triggers satellite connection.

 Value: 1

### CROSS_SIM_SPN_FORMAT_CARRIER_NAME_ONLY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CROSS_SIM_SPN_FORMAT_CARRIER_NAME_ONLY: Int
```

Specifies SPN format of displaying carrier name only.

 Value: 0

### CROSS_SIM_SPN_FORMAT_CARRIER_NAME_WITH_BRANDING

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CROSS_SIM_SPN_FORMAT_CARRIER_NAME_WITH_BRANDING: Int
```

Specifies SPN format of displaying carrier name along with "Cross-SIM calling".

 Value: 1

### DATA_CYCLE_THRESHOLD_DISABLED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_CYCLE_THRESHOLD_DISABLED: Int
```

Flag indicating that a data cycle threshold should be disabled.

If `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_DATA_WARNING_THRESHOLD_BYTES_LONG:kotlin.String` is set to this value, the platform's default data warning, if one exists, will be disabled. A user selected data warning will not be overridden.

If `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_DATA_LIMIT_THRESHOLD_BYTES_LONG:kotlin.String` is set to this value, the platform's default data limit, if one exists, will be disabled. A user selected data limit will not be overridden.

 Value: -2

### DATA_CYCLE_USE_PLATFORM_DEFAULT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_CYCLE_USE_PLATFORM_DEFAULT: Int
```

When `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MONTHLY_DATA_CYCLE_DAY_INT:kotlin.String`, `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_DATA_LIMIT_THRESHOLD_BYTES_LONG:kotlin.String`, or `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_DATA_WARNING_THRESHOLD_BYTES_LONG:kotlin.String` are set to this value, the platform default value will be used for that key.

 Value: -1

### ENABLE_EAP_METHOD_PREFIX_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENABLE_EAP_METHOD_PREFIX_BOOL: String
```

Specifies whether the system should prefix the EAP method to the anonymous identity. The following prefix will be added if this key is set to TRUE: EAP-AKA: "0" EAP-SIM: "1" EAP-AKA_PRIME: "6"

 Value: "enable_eap_method_prefix_bool"

### EXTRA_REBROADCAST_ON_UNLOCK

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_REBROADCAST_ON_UNLOCK: String
```

`https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#ACTION_CARRIER_CONFIG_CHANGED:kotlin.String` is broadcast once on device bootup and then again when the device is unlocked. Direct-Boot-aware applications may use the first broadcast as an early signal that the carrier config has been loaded, but other applications will only receive the second broadcast, when the device is unlocked. This extra is included in `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#ACTION_CARRIER_CONFIG_CHANGED:kotlin.String` to indicate whether this is a rebroadcast on unlock.

 Value: "android.telephony.extra.REBROADCAST_ON_UNLOCK"

### EXTRA_SLOT_INDEX

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_SLOT_INDEX: String
```

Extra included in `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#ACTION_CARRIER_CONFIG_CHANGED:kotlin.String` to indicate the slot index that the broadcast is for.

 Value: "android.telephony.extra.SLOT_INDEX"

### EXTRA_SUBSCRIPTION_INDEX

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_SUBSCRIPTION_INDEX: String
```

Optional extra included in `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#ACTION_CARRIER_CONFIG_CHANGED:kotlin.String` to indicate the subscription index that the broadcast is for, if a valid one is available.

 Value: "android.telephony.extra.SUBSCRIPTION_INDEX"

### IMSI_KEY_AVAILABILITY_INT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IMSI_KEY_AVAILABILITY_INT: String
```

Identifies if the key is available for WLAN or EPDG or both. The value is a bitmask. 0 indicates that neither EPDG or WLAN is enabled. 1 indicates that key type TelephonyManager#KEY_TYPE_EPDG is enabled. 2 indicates that key type TelephonyManager#KEY_TYPE_WLAN is enabled. 3 indicates that both are enabled.

 Value: "imsi_key_availability_int"

### KEY_5G_NR_SSRSRP_THRESHOLDS_INT_ARRAY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_5G_NR_SSRSRP_THRESHOLDS_INT_ARRAY: String
```

List of 4 customized 5G SS reference signal received power (SSRSRP) thresholds.

Reference: 3GPP TS 38.215

4 threshold integers must be within the boundaries \[-140 dB, -44 dB\], and the levels are:

- "NONE: \[-140, threshold1)"
- "POOR: \[threshold1, threshold2)"
- "MODERATE: \[threshold2, threshold3)"
- "GOOD: \[threshold3, threshold4)"
- "EXCELLENT: \[threshold4, -44\]"

This key is considered invalid if the format is violated. If the key is invalid or not configured, a default value set will apply.

 Value: "5g_nr_ssrsrp_thresholds_int_array"

### KEY_5G_NR_SSRSRQ_THRESHOLDS_INT_ARRAY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_5G_NR_SSRSRQ_THRESHOLDS_INT_ARRAY: String
```

List of 4 customized 5G SS reference signal received quality (SSRSRQ) thresholds.

Reference: 3GPP TS 38.215; 3GPP TS 38.133 section 10

4 threshold integers must be within the boundaries \[-43 dB, 20 dB\], and the levels are:

- "NONE: \[-43, threshold1)"
- "POOR: \[threshold1, threshold2)"
- "MODERATE: \[threshold2, threshold3)"
- "GOOD: \[threshold3, threshold4)"
- "EXCELLENT: \[threshold4, 20\]"

This key is considered invalid if the format is violated. If the key is invalid or not configured, a default value set will apply.

 Value: "5g_nr_ssrsrq_thresholds_int_array"

### KEY_5G_NR_SSSINR_THRESHOLDS_INT_ARRAY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_5G_NR_SSSINR_THRESHOLDS_INT_ARRAY: String
```

List of 4 customized 5G SS signal-to-noise and interference ratio (SSSINR) thresholds.

Reference: 3GPP TS 38.215, 3GPP TS 38.133 10.1.16.1

4 threshold integers must be within the boundaries \[-23 dB, 40 dB\], and the levels are:

- "NONE: \[-23, threshold1)"
- "POOR: \[threshold1, threshold2)"
- "MODERATE: \[threshold2, threshold3)"
- "GOOD: \[threshold3, threshold4)"
- "EXCELLENT: \[threshold4, 40\]"

This key is considered invalid if the format is violated. If the key is invalid or not configured, a default value set will apply.

 Value: "5g_nr_sssinr_thresholds_int_array"

### KEY_ADDITIONAL_CALL_SETTING_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ADDITIONAL_CALL_SETTING_BOOL: String
```

Does not display additional call setting for IMS phone based on GSM Phone

 Value: "additional_call_setting_bool"

### KEY_ADDITIONAL_SETTINGS_CALLER_ID_VISIBILITY_BOOL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ADDITIONAL_SETTINGS_CALLER_ID_VISIBILITY_BOOL: String
```

Boolean indicating if the "Caller ID" item is visible in the Additional Settings menu. true means visible. false means gone. The default value is true.

 Value: "additional_settings_caller_id_visibility_bool"

### KEY_ADDITIONAL_SETTINGS_CALL_WAITING_VISIBILITY_BOOL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ADDITIONAL_SETTINGS_CALL_WAITING_VISIBILITY_BOOL: String
```

Boolean indicating if the "Call Waiting" item is visible in the Additional Settings menu. true means visible. false means gone. The default value is true.

 Value: "additional_settings_call_waiting_visibility_bool"

### KEY_ALLOW_ADDING_APNS_BOOL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ALLOW_ADDING_APNS_BOOL: String
```

Allow user to add APNs

 Value: "allow_adding_apns_bool"

### KEY_ALLOW_ADD_CALL_DURING_VIDEO_CALL_BOOL

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ALLOW_ADD_CALL_DURING_VIDEO_CALL_BOOL: String
```

When `false`, indicates that adding a call is disabled when there is an ongoing video call or when there is an ongoing call on wifi which was downgraded from video and VoWifi is turned off. When `true`, indicates that another call can be added during an ongoing video call.

This is `true` by default.

 Value: "allow_add_call_during_video_call"

### KEY_ALLOW_EMERGENCY_NUMBERS_IN_CALL_LOG_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ALLOW_EMERGENCY_NUMBERS_IN_CALL_LOG_BOOL: String
```

Determines if the current device should allow emergency numbers to be logged in the Call Log. (Some carriers require that emergency calls \*not\* be logged, presumably to avoid the risk of accidental redialing from the call log UI. This is a good idea, so the default here is false.)

 Value: "allow_emergency_numbers_in_call_log_bool"

### KEY_ALLOW_EMERGENCY_VIDEO_CALLS_BOOL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ALLOW_EMERGENCY_VIDEO_CALLS_BOOL: String
```

Flag indicating whether to allow carrier video calls to emergency numbers. When `true`, video calls to emergency numbers will be allowed. When `false`, video calls to emergency numbers will be initiated as audio-only calls instead.

 Value: "allow_emergency_video_calls_bool"

### KEY_ALLOW_HOLD_CALL_DURING_EMERGENCY_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ALLOW_HOLD_CALL_DURING_EMERGENCY_BOOL: String
```

Flag indicating whether or not an ongoing call will be held when an outgoing emergency call is placed. If true, ongoing calls will be put on hold when an emergency call is placed. If false, placing an emergency call will trigger the disconnect of all ongoing calls before the emergency call is placed.

 Value: "allow_hold_call_during_emergency_bool"

### KEY_ALLOW_HOLD_IN_RTT_CALL_BOOL

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ALLOW_HOLD_IN_RTT_CALL_BOOL: String
```

Flag indicating whether RTT (Real-Time Text) calls support the hold/unhold capability. If false, the hold capability will be disabled for RTT calls. If true, RTT hold capability is determined by IMS service capabilities. The default value is `true`.

 Value: "allow_hold_in_rtt_call_bool"

### KEY_ALLOW_HOLD_VIDEO_CALL_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ALLOW_HOLD_VIDEO_CALL_BOOL: String
```

When `true`, indicates that video calls can be put on hold in order to swap to another call (e.g. a new outgoing call).

This is `true` by default.

 Value: "allow_hold_video_call_bool"

### KEY_ALLOW_LOCAL_DTMF_TONES_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ALLOW_LOCAL_DTMF_TONES_BOOL: String
```

Determine whether we want to play local DTMF tones in a call, or just let the radio/BP handle playing of the tones.

 Value: "allow_local_dtmf_tones_bool"

### KEY_ALLOW_MERGE_WIFI_CALLS_WHEN_VOWIFI_OFF_BOOL

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ALLOW_MERGE_WIFI_CALLS_WHEN_VOWIFI_OFF_BOOL: String
```

Flag indicating whether the carrier supports merging wifi calls when VoWIFI is disabled. This can happen in the case of a carrier which allows offloading video calls to WIFI separately of whether voice over wifi is enabled. In such a scenario when two video calls are downgraded to voice, they remain over wifi. However, if VoWIFI is disabled, these calls cannot be merged.

 Value: "allow_merge_wifi_calls_when_vowifi_off_bool"

### KEY_ALLOW_NON_EMERGENCY_CALLS_IN_ECM_BOOL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ALLOW_NON_EMERGENCY_CALLS_IN_ECM_BOOL: String
```

Determines whether the carrier supports making non-emergency phone calls while the phone is in emergency callback mode. Default value is `true`, meaning that non-emergency calls are allowed in emergency callback mode.

 Value: "allow_non_emergency_calls_in_ecm_bool"

### KEY_ALLOW_VIDEO_CALLING_FALLBACK_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ALLOW_VIDEO_CALLING_FALLBACK_BOOL: String
```

Whether system apps are allowed to use fallback if carrier video call is not available. Defaults to `true`.

 Value: "allow_video_calling_fallback_bool"

### KEY_ALLOW_VIDEO_CALL_IN_LOW_BATTERY_BOOL

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ALLOW_VIDEO_CALL_IN_LOW_BATTERY_BOOL: String
```

Flag indicating whether or not an incoming video call will be auto rejected and logged since device is in low battery.

 Value: "allow_video_call_in_low_battery_bool"

### KEY_ALWAYS_SHOW_DATA_RAT_ICON_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ALWAYS_SHOW_DATA_RAT_ICON_BOOL: String
```

Boolean indicating if show data RAT icon on status bar even when data is disabled.

 Value: "always_show_data_rat_icon_bool"

### KEY_ALWAYS_SHOW_EMERGENCY_ALERT_ONOFF_BOOL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ALWAYS_SHOW_EMERGENCY_ALERT_ONOFF_BOOL: String
```

**Deprecated:** *The allow alerts option is always shown now. No longer need a config for that.*

The default flag specifying whether "Allow alerts" option will be always shown in emergency alerts settings regardless developer options is turned on or not.

 Value: "always_show_emergency_alert_onoff_bool"

### KEY_ALWAYS_SHOW_PRIMARY_SIGNAL_BAR_IN_OPPORTUNISTIC_NETWORK_BOOLEAN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ALWAYS_SHOW_PRIMARY_SIGNAL_BAR_IN_OPPORTUNISTIC_NETWORK_BOOLEAN: String
```

Indicates when a carrier has a primary subscription and an opportunistic subscription active, and when Internet data is switched to opportunistic network, whether to still show signal bar of primary network. By default it will be false, meaning whenever data is going over opportunistic network, signal bar will reflect signal strength and rat icon of that network.

 Value: "always_show_primary_signal_bar_in_opportunistic_network_boolean"

### KEY_APN_EXPAND_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_APN_EXPAND_BOOL: String
```

Control whether users can edit APNs in Settings.

 Value: "apn_expand_bool"

### KEY_APN_SETTINGS_DEFAULT_APN_TYPES_STRING_ARRAY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_APN_SETTINGS_DEFAULT_APN_TYPES_STRING_ARRAY: String
```

Default value of APN types field if not specified by user when adding/modifying an APN.

 Value: "apn_settings_default_apn_types_string_array"

### KEY_AUTO_RETRY_ENABLED_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_AUTO_RETRY_ENABLED_BOOL: String
```

Flag indicating if auto retry is enabled

 Value: "auto_retry_enabled_bool"

### KEY_AUTO_UNHOLD_ON_REMOTE_DISCONNECT_BOOL

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_AUTO_UNHOLD_ON_REMOTE_DISCONNECT_BOOL: String
```

Flag indicating whether the carrier supports auto-unholding the background call on remotely disconnected calls.

 Value: "auto_unhold_on_remote_disconnect_bool"

### KEY_AVOID_BAD_WIFI_BOOL

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_AVOID_BAD_WIFI_BOOL: String
```

Used in reading the 'avoid bad Wi-Fi' setting from the carrier config. This allows the device to switch from Wi-Fi networks losing internet access to another available and working connection, such as mobile. This configuration was originally read from resources and could not be customized per-MVNO. Reading from the carrier config improves flexibility to meet the needs of different carriers.

 Value: "avoid_bad_wifi_bool"

### KEY_CALL_BARRING_DEFAULT_SERVICE_CLASS_INT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CALL_BARRING_DEFAULT_SERVICE_CLASS_INT: String
```

Specifies the service class for call barring service. Default value is `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#SERVICE_CLASS_VOICE:kotlin.Int`. The value set as below:

- 0: `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#SERVICE_CLASS_NONE:kotlin.Int`
- 1: `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#SERVICE_CLASS_VOICE:kotlin.Int`

<br />

 Value: "call_barring_default_service_class_int"

### KEY_CALL_BARRING_SUPPORTS_DEACTIVATE_ALL_BOOL

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CALL_BARRING_SUPPORTS_DEACTIVATE_ALL_BOOL: String
```

Flag indicating whether or not deactivating all call barring features via the "Call Barring" settings menu is supported. If true, the option will be visible in the "Call Barring" settings menu. If false, the option will not be visible. Enabled by default.

 Value: "call_barring_supports_deactivate_all_bool"

### KEY_CALL_BARRING_SUPPORTS_PASSWORD_CHANGE_BOOL

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CALL_BARRING_SUPPORTS_PASSWORD_CHANGE_BOOL: String
```

Flag indicating whether or not changing the call barring password via the "Call Barring" settings menu is supported. If true, the option will be visible in the "Call Barring" settings menu. If false, the option will not be visible. Enabled by default.

 Value: "call_barring_supports_password_change_bool"

### KEY_CALL_BARRING_VISIBILITY_BOOL

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CALL_BARRING_VISIBILITY_BOOL: String
```

Boolean indicating if the "Call barring" item is visible in the Call Settings menu. If true, the "Call Barring" menu will be visible. If false, the menu will be gone. Disabled by default.

 Value: "call_barring_visibility_bool"

### KEY_CALL_COMPOSER_PICTURE_SERVER_URL_STRING

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CALL_COMPOSER_PICTURE_SERVER_URL_STRING: String
```

Indicates the carrier server url that serves the call composer picture.

 Value: "call_composer_picture_server_url_string"

### KEY_CALL_FORWARDING_BLOCKS_WHILE_ROAMING_STRING_ARRAY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CALL_FORWARDING_BLOCKS_WHILE_ROAMING_STRING_ARRAY: String
```

An array containing custom call forwarding number prefixes that will be blocked while the device is reporting that it is roaming. By default, there are no custom call forwarding prefixes and none of these numbers will be filtered. If one or more entries are present, the system will not complete the call and display an error message. To display a message to the user when call forwarding fails for 3gpp MMI codes while roaming, use the `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SUPPORT_3GPP_CALL_FORWARDING_WHILE_ROAMING_BOOL:kotlin.String` option instead.

 Value: "call_forwarding_blocks_while_roaming_string_array"

### KEY_CALL_REDIRECTION_SERVICE_COMPONENT_NAME_STRING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CALL_REDIRECTION_SERVICE_COMPONENT_NAME_STRING: String
```

Specifies a carrier-defined `https://developer.android.com/reference/kotlin/android/telecom/CallRedirectionService.html#` which Telecom will bind to for outgoing calls. An empty string indicates that no carrier-defined `https://developer.android.com/reference/kotlin/android/telecom/CallRedirectionService.html#` is specified.

 Value: "call_redirection_service_component_name_string"

### KEY_CAPABILITIES_EXEMPT_FROM_SINGLE_DC_CHECK_INT_ARRAY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CAPABILITIES_EXEMPT_FROM_SINGLE_DC_CHECK_INT_ARRAY: String
```

Only apply if `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_ONLY_SINGLE_DC_ALLOWED_INT_ARRAY:kotlin.String` specifies the network types that support a single data connection at a time. This key defines a list of network capabilities which, if requested, will exempt the request from single data connection checks.

 Value: "capabilities_exempt_from_single_dc_check_int_array"

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities.html#`

### KEY_CARRIER_ALLOW_DEFLECT_IMS_CALL_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_ALLOW_DEFLECT_IMS_CALL_BOOL: String
```

Flag indicating whether the carrier supports call deflection for an incoming IMS call.

 Value: "carrier_allow_deflect_ims_call_bool"

### KEY_CARRIER_ALLOW_TURNOFF_IMS_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_ALLOW_TURNOFF_IMS_BOOL: String
```

Flag specifying whether IMS service can be turned off. If false then the service will not be turned-off completely, but individual features can be disabled.

 Value: "carrier_allow_turnoff_ims_bool"

### KEY_CARRIER_APP_REQUIRED_DURING_SIM_SETUP_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_APP_REQUIRED_DURING_SIM_SETUP_BOOL: String
```

Determines whether the carrier app needed to be involved when users try to finish setting up the SIM card to get network service.

 Value: "carrier_app_required_during_setup_bool"

### KEY_CARRIER_CALL_SCREENING_APP_STRING

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_CALL_SCREENING_APP_STRING: String
```

The Component Name of a carrier-provided CallScreeningService implementation. Telecom will bind to `https://developer.android.com/reference/kotlin/android/telecom/CallScreeningService.html#` for ALL incoming calls and provide the carrier CallScreeningService with the opportunity to allow or block calls.

The String includes the package name/the class name. Example: com.android.carrier/com.android.carrier.callscreeningserviceimpl

Using `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#flattenToString()` to convert a ComponentName object to String. Using `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#unflattenFromString(kotlin.String)` to convert a String object to a ComponentName.

 Value: "call_screening_app"

### KEY_CARRIER_CERTIFICATE_STRING_ARRAY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_CERTIFICATE_STRING_ARRAY: String
```

Holds the list of carrier certificate hashes, followed by optional package names. Format: "sha1/256" or "sha1/256:package1,package2,package3..." Note that each carrier has its own hashes.

 Value: "carrier_certificate_string_array"

### KEY_CARRIER_CONFIG_APPLIED_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_CONFIG_APPLIED_BOOL: String
```

Determines whether any carrier has been identified and its specific config has been applied, default to false.

 Value: "carrier_config_applied_bool"

### KEY_CARRIER_CONFIG_VERSION_STRING

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_CONFIG_VERSION_STRING: String
```

Specifies a value that identifies the version of the carrier configuration that is currently in use. This string is displayed on the UI. The format of the string is not specified.

 Value: "carrier_config_version_string"

### KEY_CARRIER_CROSS_SIM_IMS_AVAILABLE_BOOL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_CROSS_SIM_IMS_AVAILABLE_BOOL: String
```

Flag specifying whether Cross SIM over IMS should be available for carrier. When `false` the carrier does not support cross SIM calling. When `true` the carrier does support cross sim calling, where available

 Value: "carrier_cross_sim_ims_available_bool"

### KEY_CARRIER_DATA_CALL_PERMANENT_FAILURE_STRINGS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_DATA_CALL_PERMANENT_FAILURE_STRINGS: String
```

**Deprecated:** *This API key was added in mistake and is not used anymore by the telephony data frameworks.*

Data call setup permanent failure causes by the carrier.

 Value: "carrier_data_call_permanent_failure_strings"

### KEY_CARRIER_DEFAULT_ACTIONS_ON_DCFAILURE_STRING_ARRAY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_DEFAULT_ACTIONS_ON_DCFAILURE_STRING_ARRAY: String
```

Defines carrier-specific actions which act upon CARRIER_SIGNAL_REQUEST_NETWORK_FAILED and configured signal args: android.telephony.TelephonyManager#EXTRA_APN_TYPE, android.telephony.TelephonyManager#EXTRA_ERROR_CODE used for customization of the default carrier app Format: { "APN_1, ERROR_CODE_1 : CARRIER_ACTION_IDX_1, CARRIER_ACTION_IDX_2...", "APN_1, ERROR_CODE_2 : CARRIER_ACTION_IDX_1 " } Where `APN_1` is an integer defined in `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting` (e.g. `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_DEFAULT:kotlin.Int` `ERROR_CODE_1` is an integer defined in android.telephony.DataFailCause Example: android.telephony.DataFailCause#MISSING_UNKNOWN_APN `CARRIER_ACTION_IDX_1` is an integer defined in com.android.carrierdefaultapp.CarrierActionUtils Example: com.android.carrierdefaultapp.CarrierActionUtils#CARRIER_ACTION_DISABLE_METERED_APNS disables metered APNs

 Value: "carrier_default_actions_on_dcfailure_string_array"

### KEY_CARRIER_DEFAULT_ACTIONS_ON_DEFAULT_NETWORK_AVAILABLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_DEFAULT_ACTIONS_ON_DEFAULT_NETWORK_AVAILABLE: String
```

Defines carrier-specific actions which act upon com.android.internal.telephony.CARRIER_SIGNAL_DEFAULT_NETWORK_AVAILABLE, used for customization of the default carrier app. Format: { "true : CARRIER_ACTION_IDX_1", "false: CARRIER_ACTION_IDX_2" } Where `true` is a boolean indicates default network available/unavailable Where `CARRIER_ACTION_IDX` is an integer defined in com.android.carrierdefaultapp.CarrierActionUtils CarrierActionUtils Example: com.android.carrierdefaultapp.CarrierActionUtils#CARRIER_ACTION_ENABLE_DEFAULT_URL_HANDLER enables the app as the default URL handler

 Value: "carrier_default_actions_on_default_network_available_string_array"

### KEY_CARRIER_DEFAULT_ACTIONS_ON_REDIRECTION_STRING_ARRAY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_DEFAULT_ACTIONS_ON_REDIRECTION_STRING_ARRAY: String
```

Defines carrier-specific actions which act upon com.android.internal.telephony.CARRIER_SIGNAL_REDIRECTED, used for customization of the default carrier app. Format: "CARRIER_ACTION_IDX, ..." Where `CARRIER_ACTION_IDX` is an integer defined in com.android.carrierdefaultapp.CarrierActionUtils Example: com.android.carrierdefaultapp.CarrierActionUtils#CARRIER_ACTION_DISABLE_METERED_APNS disables metered APNs

 Value: "carrier_default_actions_on_redirection_string_array"

### KEY_CARRIER_DEFAULT_ACTIONS_ON_RESET

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_DEFAULT_ACTIONS_ON_RESET: String
```

Defines carrier-specific actions which act upon CARRIER_SIGNAL_RESET, used for customization of the default carrier app. Format: "CARRIER_ACTION_IDX, ..." Where `CARRIER_ACTION_IDX` is an integer defined in com.android.carrierdefaultapp.CarrierActionUtils Example: com.android.carrierdefaultapp.CarrierActionUtils#CARRIER_ACTION_CANCEL_ALL_NOTIFICATIONS clears all notifications on reset

 Value: "carrier_default_actions_on_reset_string_array"

### KEY_CARRIER_DEFAULT_REDIRECTION_URL_STRING_ARRAY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_DEFAULT_REDIRECTION_URL_STRING_ARRAY: String
```

Defines a list of acceptable redirection url for default carrier app.

 Value: "carrier_default_redirection_url_string_array"

### KEY_CARRIER_DEFAULT_WFC_IMS_ENABLED_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_DEFAULT_WFC_IMS_ENABLED_BOOL: String
```

Default WFC_IMS_enabled: true VoWiFi by default is on false VoWiFi by default is off

 Value: "carrier_default_wfc_ims_enabled_bool"

### KEY_CARRIER_DEFAULT_WFC_IMS_MODE_INT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_DEFAULT_WFC_IMS_MODE_INT: String
```

Default mode for WFC over IMS on home network:

- 0: Wi-Fi only
- 1: prefer mobile network
- 2: prefer Wi-Fi

<br />

 Value: "carrier_default_wfc_ims_mode_int"

### KEY_CARRIER_DEFAULT_WFC_IMS_ROAMING_MODE_INT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_DEFAULT_WFC_IMS_ROAMING_MODE_INT: String
```

Default mode for WFC over IMS on roaming network. See `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_DEFAULT_WFC_IMS_MODE_INT:kotlin.String` for meaning of values.

 Value: "carrier_default_wfc_ims_roaming_mode_int"

### KEY_CARRIER_FORCE_DISABLE_ETWS_CMAS_TEST_BOOL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_FORCE_DISABLE_ETWS_CMAS_TEST_BOOL: String
```

**Deprecated:** *Use `com.android.cellbroadcastreceiver.CellBroadcastReceiver` resource `show_test_settings` to control whether to show test alert settings or not.*

The default flag specifying whether ETWS/CMAS test setting is forcibly disabled in Settings-\>More-\>Emergency broadcasts menu even though developer options is turned on.

 Value: "carrier_force_disable_etws_cmas_test_bool"

### KEY_CARRIER_IMS_GBA_REQUIRED_BOOL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_IMS_GBA_REQUIRED_BOOL: String
```

Flag specifying whether Generic Bootstrapping Architecture capable SIM is required for IMS.

 Value: "carrier_ims_gba_required_bool"

### KEY_CARRIER_INSTANT_LETTERING_AVAILABLE_BOOL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_INSTANT_LETTERING_AVAILABLE_BOOL: String
```

Flag specifying whether IMS instant lettering is available for the carrier. `True` if instant lettering is available for the carrier, `false` otherwise.

 Value: "carrier_instant_lettering_available_bool"

### KEY_CARRIER_INSTANT_LETTERING_ENCODING_STRING

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_INSTANT_LETTERING_ENCODING_STRING: String
```

When IMS instant lettering is available for a carrier (see `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_INSTANT_LETTERING_AVAILABLE_BOOL:kotlin.String`), determines the character encoding which will be used when determining the length of messages. Used in the InCall UI to limit the number of characters the user may type. If empty-string, the instant lettering message size limit will be enforced on a 1:1 basis. That is, each character will count towards the messages size limit as a single byte. If a character encoding is specified, the message size limit will be based on the number of bytes in the message per the specified encoding.

 Value: "carrier_instant_lettering_encoding_string"

### KEY_CARRIER_INSTANT_LETTERING_ESCAPED_CHARS_STRING

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_INSTANT_LETTERING_ESCAPED_CHARS_STRING: String
```

When IMS instant lettering is available for a carrier (see `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_INSTANT_LETTERING_AVAILABLE_BOOL:kotlin.String`), determines a list of characters which must be escaped with a backslash '\\' character. Should be specified as a string containing the characters to be escaped. For example to escape quote and backslash the string would be a quote and a backslash.

 Value: "carrier_instant_lettering_escaped_chars_string"

### KEY_CARRIER_INSTANT_LETTERING_INVALID_CHARS_STRING

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_INSTANT_LETTERING_INVALID_CHARS_STRING: String
```

When IMS instant lettering is available for a carrier (see `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_INSTANT_LETTERING_AVAILABLE_BOOL:kotlin.String`), determines the list of characters which may not be contained in messages. Should be specified as a regular expression suitable for use with `https://developer.android.com/reference/kotlin/java/lang/String.html#matches(kotlin.String)`.

 Value: "carrier_instant_lettering_invalid_chars_string"

### KEY_CARRIER_INSTANT_LETTERING_LENGTH_LIMIT_INT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_INSTANT_LETTERING_LENGTH_LIMIT_INT: String
```

When IMS instant lettering is available for a carrier (see `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_INSTANT_LETTERING_AVAILABLE_BOOL:kotlin.String`), the length limit for messages. Used in the InCall UI to ensure the user cannot enter more characters than allowed by the carrier. See also `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_INSTANT_LETTERING_ENCODING_STRING:kotlin.String` for more information on how the length of the message is calculated.

 Value: "carrier_instant_lettering_length_limit_int"

### KEY_CARRIER_METERED_APN_TYPES_STRINGS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_METERED_APN_TYPES_STRINGS: String
```

A string array indicating the default APN types that are metered by the carrier. The string in the array is the name of the APN type. For example, "default" for `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_DEFAULT:kotlin.Int`, "mms" for `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_MMS:kotlin.Int`, etc. The default value is `{"default", "mms", "dun", "supl"}`.

 Value: "carrier_metered_apn_types_strings"

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_DEFAULT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_MMS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_SUPL:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_DUN:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_HIPRI:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_FOTA:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_IMS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_CBS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_IA:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_EMERGENCY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_MCX:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_XCAP:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_BIP:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_VSIM:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_ENTERPRISE:kotlin.Int`

### KEY_CARRIER_METERED_ROAMING_APN_TYPES_STRINGS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_METERED_ROAMING_APN_TYPES_STRINGS: String
```

A string array indicating the default APN types that are roaming-metered by the carrier. The string in the array is the name of the APN type. For example, "default" for `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_DEFAULT:kotlin.Int`, "mms" for `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_MMS:kotlin.Int`, etc. The default value is `{"default", "mms", "dun", "supl"}`.

 Value: "carrier_metered_roaming_apn_types_strings"

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_DEFAULT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_MMS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_SUPL:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_DUN:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_HIPRI:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_FOTA:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_IMS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_CBS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_IA:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_EMERGENCY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_MCX:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_XCAP:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_BIP:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_VSIM:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_ENTERPRISE:kotlin.Int`

### KEY_CARRIER_NAME_OVERRIDE_BOOL

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_NAME_OVERRIDE_BOOL: String
```

Unconditionally override the carrier name string using #KEY_CARRIER_NAME_STRING. If true, then the carrier name string will be #KEY_CARRIER_NAME_STRING, unconditionally.

If false, then the override will be performed conditionally and the #KEY_CARRIER_NAME_STRING will have the lowest-precedence; it will only be used in the event that the name string would otherwise be empty, allowing it to serve as a last-resort. If used, this value functions in place of the SPN on any/all ICC records for the corresponding subscription.

 Value: "carrier_name_override_bool"

### KEY_CARRIER_NAME_STRING

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_NAME_STRING: String
```

String to identify carrier name in CarrierConfig app. This string overrides SPN if #KEY_CARRIER_NAME_OVERRIDE_BOOL is true; otherwise, it will be used if its value is provided and SPN is unavailable

 Value: "carrier_name_string"

### KEY_CARRIER_NR_AVAILABILITIES_INT_ARRAY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_NR_AVAILABILITIES_INT_ARRAY: String
```

A list of carrier nr availability is used to determine whether the carrier enable the non-standalone (NSA) mode of 5G NR, standalone (SA) mode of 5G NR

The value of list is `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#CARRIER_NR_AVAILABILITY_NSA:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#CARRIER_NR_AVAILABILITY_SA:kotlin.Int`.

For example, if both NSA and SA are used, the list value is { `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#CARRIER_NR_AVAILABILITY_NSA:kotlin.Int`,`https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#CARRIER_NR_AVAILABILITY_SA:kotlin.Int`}. If the carrier doesn't support 5G NR, the value is the empty array. If the key is invalid or not configured, the default value { `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#CARRIER_NR_AVAILABILITY_NSA:kotlin.Int`,`https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#CARRIER_NR_AVAILABILITY_SA:kotlin.Int`} will apply.

 Value: "carrier_nr_availabilities_int_array"

### KEY_CARRIER_PROVISIONS_WIFI_MERGED_NETWORKS_BOOL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_PROVISIONS_WIFI_MERGED_NETWORKS_BOOL: String
```

Indicates whether or not the carrier will provision merged carrier Wi-Fi offload networks. Such networks are considered part of the core carrier network. This configuration will be use to gate whether such configurations are allowed to the carrier and correspondingly enable UI elements which are required for such configurations.

 Value: "carrier_provisions_wifi_merged_networks_bool"

### KEY_CARRIER_RCS_PROVISIONING_REQUIRED_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_RCS_PROVISIONING_REQUIRED_BOOL: String
```

Flag specifying whether provisioning is required for RCS.

 Value: "carrier_rcs_provisioning_required_bool"

### KEY_CARRIER_ROAMING_NTN_CONNECT_TYPE_INT

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_ROAMING_NTN_CONNECT_TYPE_INT: String
```

Indicates carrier roaming non-terrestrial network SatelliteManager.ConnectType that the device can use to perform satellite communication.

 Value: "carrier_roaming_ntn_connect_type_int"

### KEY_CARRIER_ROAMING_NTN_EMERGENCY_CALL_TO_SATELLITE_HANDOVER_TYPE_INT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_ROAMING_NTN_EMERGENCY_CALL_TO_SATELLITE_HANDOVER_TYPE_INT: String
```

Indicates carrier roaming non-terrestrial network emergency call handover type that the device will use to perform a handover between ESOS or T911. If this key is set to android.telephony.satellite.SatelliteManager#EMERGENCY_CALL_TO_SATELLITE_HANDOVER_TYPE_SOS then the handover will be made to ESOS. If this key is set to android.telephony.satellite.SatelliteManager#EMERGENCY_CALL_TO_SATELLITE_HANDOVER_TYPE_T911 then the handover will be made to T911. The default value is android.telephony.satellite.SatelliteManager#EMERGENCY_CALL_TO_SATELLITE_HANDOVER_TYPE_T911.

 Value: "carrier_roaming_ntn_emergency_call_to_satellite_handover_type_int"

### KEY_CARRIER_ROAMING_SATELLITE_DEFAULT_SERVICES_INT_ARRAY

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_ROAMING_SATELLITE_DEFAULT_SERVICES_INT_ARRAY: String
```

An int array that contains default capabilities for carrier enabled satellite roaming. If any PLMN is provided from the entitlement server, and it is not listed in `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_SUPPORTED_SATELLITE_SERVICES_PER_PROVIDER_BUNDLE:kotlin.String`, default capabilities will be used instead.

The default capabilities are `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#SERVICE_TYPE_SMS:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#SERVICE_TYPE_MMS:kotlin.Int`

 Value: "carrier_roaming_satellite_default_services_int_array"

### KEY_CARRIER_ROAMING_SATELLITE_T911_TO_ESOS_HANDOVER_SUPPORTED_BOOL

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_ROAMING_SATELLITE_T911_TO_ESOS_HANDOVER_SUPPORTED_BOOL: String
```

Indicate whether carrier roaming satellite supports handover from T911 to ESOS.

This config will be read by Android Messaging application to determine whether to allow user to show the option of moving to eSOS when they try to send emergency message. This config requires `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SATELLITE_ESOS_SUPPORTED_BOOL:kotlin.String` to be true as well.

The default value is false.

 Value: "carrier_roaming_satellite_t911_to_esos_handover_supported_bool"

### KEY_CARRIER_SERVICE_NAME_STRING_ARRAY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_SERVICE_NAME_STRING_ARRAY: String
```

String array containing the list of names for service numbers provided by carriers. This key should be used with `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_SERVICE_NUMBER_STRING_ARRAY:kotlin.String`. The names provided in this array will be mapped 1:1 with the numbers provided in the `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_SERVICE_NUMBER_STRING_ARRAY:kotlin.String` array.

The data would be considered valid if and only if:

- The number of items in both the arrays are equal
- The data added to the `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_SERVICE_NUMBER_STRING_ARRAY:kotlin.String` array is valid. See `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_SERVICE_NUMBER_STRING_ARRAY:kotlin.String` for more information.

Example:

```kotlin
<code>&lt;string-array name="carrier_service_name_array" num="2"&gt;
    &lt;item value="Police"/&gt;
    &lt;item value="Ambulance"/&gt;
  &lt;/string-array&gt;
  </code>
```

 Value: "carrier_service_name_array"

### KEY_CARRIER_SERVICE_NUMBER_STRING_ARRAY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_SERVICE_NUMBER_STRING_ARRAY: String
```

String array containing the list of service numbers provided by carriers. This key should be used with `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_SERVICE_NAME_STRING_ARRAY:kotlin.String`. The numbers provided in this array will be mapped 1:1 with the names provided in the `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_SERVICE_NAME_STRING_ARRAY:kotlin.String` array.

The data would be considered valid if and only if:

- The number of items in both the arrays are equal
- The item should contain dialable characters only which includes 0-9, -, \*, #, (, ), SPACE.

Example:

```kotlin
<code>&lt;string-array name="carrier_service_number_array" num="2"&gt;
    &lt;item value="*123"/&gt;
    &lt;item value="+ (111) 111-111"/&gt;
  &lt;/string-array&gt;
  </code>
```

 Value: "carrier_service_number_array"

### KEY_CARRIER_SETTINGS_ACTIVITY_COMPONENT_NAME_STRING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_SETTINGS_ACTIVITY_COMPONENT_NAME_STRING: String
```

Flatten `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` of the carrier's settings activity.

 Value: "carrier_settings_activity_component_name_string"

### KEY_CARRIER_SETTINGS_ENABLE_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_SETTINGS_ENABLE_BOOL: String
```

Display carrier settings menu if true

 Value: "carrier_settings_enable_bool"

### KEY_CARRIER_SUPPORTED_SATELLITE_NOTIFICATION_HYSTERESIS_SEC_INT

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_SUPPORTED_SATELLITE_NOTIFICATION_HYSTERESIS_SEC_INT: String
```

The carrier roaming non-terrestrial network hysteresis time in seconds. If the device supports P2P satellite messaging which is defined by `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_SUPPORTED_SATELLITE_SERVICES_PER_PROVIDER_BUNDLE:kotlin.String` and the device is in `https://developer.android.com/reference/kotlin/android/telephony/ServiceState#STATE_OUT_OF_SERVICE:kotlin.Int`, not connected to Wi-Fi, then hysteresis timer defined by this key will start. After the timer is expired, device is marked as eligible for satellite communication. The default value is 180 seconds.

 Value: "carrier_supported_satellite_notification_hysteresis_sec_int"

### KEY_CARRIER_SUPPORTED_SATELLITE_SERVICES_PER_PROVIDER_BUNDLE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_SUPPORTED_SATELLITE_SERVICES_PER_PROVIDER_BUNDLE: String
```

A PersistableBundle that contains a list of key-value pairs, where the values are integer arrays.

Keys are the PLMNs of satellite providers as strings and values are integer arrays of supported services with the following value:

- 1 = `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#SERVICE_TYPE_VOICE:kotlin.Int`
- 2 = `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#SERVICE_TYPE_DATA:kotlin.Int`
- 3 = `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#SERVICE_TYPE_SMS:kotlin.Int`
- 4 = `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#SERVICE_TYPE_VIDEO:kotlin.Int`
- 5 = `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#SERVICE_TYPE_EMERGENCY:kotlin.Int`
- 6 = `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#SERVICE_TYPE_MMS:kotlin.Int`
- 7 = `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#SERVICE_TYPE_EMERGENCY_SMS:kotlin.Int`

An example config for two PLMNs "123411" and "123412":

```kotlin
<code>&lt;carrier_config&gt;
    &lt;pbundle_as_map name="carrier_supported_satellite_services_per_provider_bundle"&gt;
      &lt;int-array name = "123411" num = "2"&gt;
        &lt;item value = "3"/&gt;
        &lt;item value = "5"/&gt;
      &lt;/int-array&gt;
      &lt;int-array name = "123412" num = "1"&gt;
        &lt;item value = "3"/&gt;
      &lt;/int-array&gt;
    &lt;/pbundle_as_map&gt;
  &lt;/carrier_config&gt;
  </code>
```

This config is empty by default.

 Value: "carrier_supported_satellite_services_per_provider_bundle"

### KEY_CARRIER_SUPPORTS_OPP_DATA_AUTO_PROVISIONING_BOOL

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_SUPPORTS_OPP_DATA_AUTO_PROVISIONING_BOOL: String
```

Configuration to indicate that the carrier supports opportunistic data auto provisioning. Based on this flag, the device downloads and activates corresponding opportunistic profile.

 Value: "carrier_supports_opp_data_auto_provisioning_bool"

### KEY_CARRIER_SUPPORTS_SS_OVER_UT_BOOL

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_SUPPORTS_SS_OVER_UT_BOOL: String
```

Flag indicating whether or not the carrier supports Supplementary Services over the UT interface for this subscription. If true, the device will use Supplementary Services over UT when provisioned (see `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_UT_PROVISIONING_REQUIRED_BOOL:kotlin.String`). If false, this device will fallback to circuit switch for supplementary services and will disable this capability for IMS entirely. The default value for this key is `false`.

 Value: "carrier_supports_ss_over_ut_bool"

### KEY_CARRIER_SUPPORTS_TETHERING_BOOL

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_SUPPORTS_TETHERING_BOOL: String
```

Flag indicating if the carrier supports tethering of mobile data.

 Value: "carrier_supports_tethering_bool"

### KEY_CARRIER_USE_IMS_FIRST_FOR_EMERGENCY_BOOL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_USE_IMS_FIRST_FOR_EMERGENCY_BOOL: String
```

Flag specifying whether IMS should be the first phone attempted for E911 even if the phone is not in service.

 Value: "carrier_use_ims_first_for_emergency_bool"

### KEY_CARRIER_USSD_METHOD_INT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_USSD_METHOD_INT: String
```

Specify the method of selection for UE sending USSD requests. The default value is `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#USSD_OVER_CS_PREFERRED:kotlin.Int`.

Available options:

- 0: `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#USSD_OVER_CS_PREFERRED:kotlin.Int`
- 1: `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#USSD_OVER_IMS_PREFERRED:kotlin.Int`
- 2: `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#USSD_OVER_CS_ONLY:kotlin.Int`
- 3: `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#USSD_OVER_IMS_ONLY:kotlin.Int`

 Value: "carrier_ussd_method_int"

### KEY_CARRIER_UT_PROVISIONING_REQUIRED_BOOL

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_UT_PROVISIONING_REQUIRED_BOOL: String
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.Ims#KEY_MMTEL_REQUIRES_PROVISIONING_BUNDLE:kotlin.String` instead for determining if UT requires provisioning.*

Flag indicating whether or not the IMS MmTel UT capability requires carrier provisioning before it can be set as enabled. If true, the UT capability will be set to false for the newly loaded subscription and will require the carrier provisioning app to set the persistent provisioning result. If false, the platform will not wait for provisioning status updates for the UT capability and enable the UT over IMS capability for the subscription when the subscription is loaded. The default value for this key is `false`.

 Value: "carrier_ut_provisioning_required_bool"

### KEY_CARRIER_VOLTE_AVAILABLE_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_VOLTE_AVAILABLE_BOOL: String
```

Flag specifying whether VoLTE should be available for carrier, independent of carrier provisioning. If false: hard disabled. If true: then depends on carrier provisioning, availability, etc.

 Value: "carrier_volte_available_bool"

### KEY_CARRIER_VOLTE_OVERRIDE_WFC_PROVISIONING_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_VOLTE_OVERRIDE_WFC_PROVISIONING_BOOL: String
```

Flag specifying if WFC provisioning depends on VoLTE provisioning. `false`: default value; honor actual WFC provisioning state. `true`: when VoLTE is not provisioned, treat WFC as not provisioned; when VoLTE is provisioned, honor actual WFC provisioning state. As of now, Verizon is the only carrier enforcing this dependency in their WFC awareness and activation requirements.

 Value: "carrier_volte_override_wfc_provisioning_bool"

### KEY_CARRIER_VOLTE_PROVISIONED_BOOL

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_VOLTE_PROVISIONED_BOOL: String
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_RCS_PROVISIONING_REQUIRED_BOOL:kotlin.String` instead.*

This flag specifies whether VoLTE availability is based on provisioning. By default this is false. Used for UCE to determine if EAB provisioning checks should be based on provisioning.

 Value: "carrier_volte_provisioned_bool"

### KEY_CARRIER_VOLTE_PROVISIONING_REQUIRED_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_VOLTE_PROVISIONING_REQUIRED_BOOL: String
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.Ims#KEY_MMTEL_REQUIRES_PROVISIONING_BUNDLE:kotlin.String` instead for finer-grained control. changing carrier_volte_provisioning_required_bool requires changes to mmtel_requires_provisioning_bundle and vice versa `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.Ims#KEY_MMTEL_REQUIRES_PROVISIONING_BUNDLE:kotlin.String`*

Flag specifying whether provisioning is required for VoLTE, Video Telephony, and WiFi Calling. Combines VoLTE, VT, VoWiFI calling provisioning into one parameter.

 Value: "carrier_volte_provisioning_required_bool"

### KEY_CARRIER_VOLTE_TTY_SUPPORTED_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_VOLTE_TTY_SUPPORTED_BOOL: String
```

Flag specifying whether VoLTE TTY is supported.

 Value: "carrier_volte_tty_supported_bool"

### KEY_CARRIER_VT_AVAILABLE_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_VT_AVAILABLE_BOOL: String
```

Flag specifying whether video telephony is available for carrier. If false: hard disabled. If true: then depends on carrier provisioning, availability, etc.

 Value: "carrier_vt_available_bool"

### KEY_CARRIER_VVM_PACKAGE_NAME_STRING

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_VVM_PACKAGE_NAME_STRING: String
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_VVM_PACKAGE_NAME_STRING_ARRAY:kotlin.String`.*

The package name of the carrier's visual voicemail app to ensure that dialer visual voicemail and carrier visual voicemail are not active at the same time.

 Value: "carrier_vvm_package_name_string"

### KEY_CARRIER_VVM_PACKAGE_NAME_STRING_ARRAY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_VVM_PACKAGE_NAME_STRING_ARRAY: String
```

A list of the carrier's visual voicemail app package names to ensure that dialer visual voicemail and carrier visual voicemail are not active at the same time.

 Value: "carrier_vvm_package_name_string_array"

### KEY_CARRIER_WFC_IMS_AVAILABLE_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_WFC_IMS_AVAILABLE_BOOL: String
```

Flag specifying whether WFC over IMS should be available for carrier: independent of carrier provisioning. If false: hard disabled. If true: then depends on carrier provisioning, availability etc.

 Value: "carrier_wfc_ims_available_bool"

### KEY_CARRIER_WFC_SUPPORTS_WIFI_ONLY_BOOL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CARRIER_WFC_SUPPORTS_WIFI_ONLY_BOOL: String
```

Flag specifying whether WFC over IMS supports the "wifi only" option. If false, the wifi calling settings will not include an option for "wifi only". If true, the wifi calling settings will include an option for "wifi only"

By default, it is assumed that WFC supports "wifi only".

 Value: "carrier_wfc_supports_wifi_only_bool"

### KEY_CDMA_3WAYCALL_FLASH_DELAY_INT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CDMA_3WAYCALL_FLASH_DELAY_INT: String
```

**Deprecated:** *Legacy CDMA is unsupported.*

For carriers which require an empty flash to be sent before sending the normal 3-way calling flash, the duration in milliseconds of the empty flash to send. When `0`, no empty flash is sent.

 Value: "cdma_3waycall_flash_delay_int"

### KEY_CDMA_DTMF_TONE_DELAY_INT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CDMA_DTMF_TONE_DELAY_INT: String
```

**Deprecated:** *Legacy CDMA is unsupported.*

Specifies the amount of gap to be added in millis between postdial DTMF tones. When a non-zero value is specified, the UE shall wait for the specified amount of time before it sends out successive DTMF tones on the network.

 Value: "cdma_dtmf_tone_delay_int"

### KEY_CDMA_NONROAMING_NETWORKS_STRING_ARRAY

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CDMA_NONROAMING_NETWORKS_STRING_ARRAY: String
```

**Deprecated:** *Legacy CDMA is unsupported.*

Override the platform's notion of a network operator being considered non roaming. Value is string array of SIDs to be considered not roaming for 3GPP2 RATs.

 Value: "cdma_nonroaming_networks_string_array"

### KEY_CDMA_ROAMING_MODE_INT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CDMA_ROAMING_MODE_INT: String
```

**Deprecated:** *Legacy CDMA is unsupported.*

The CDMA roaming mode (aka CDMA system select).

The value should be one of the CDMA_ROAMING_MODE_ constants in `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager`. Values other than `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CDMA_ROAMING_MODE_RADIO_DEFAULT:kotlin.Int` (which is the default) will take precedence over user selection.

 Value: "cdma_roaming_mode_int"

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CDMA_ROAMING_MODE_RADIO_DEFAULT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CDMA_ROAMING_MODE_HOME:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CDMA_ROAMING_MODE_AFFILIATED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CDMA_ROAMING_MODE_ANY:kotlin.Int`

### KEY_CDMA_ROAMING_NETWORKS_STRING_ARRAY

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CDMA_ROAMING_NETWORKS_STRING_ARRAY: String
```

**Deprecated:** *Legacy CDMA is unsupported.*

Override the platform's notion of a network operator being considered roaming. Value is string array of SIDs to be considered roaming for 3GPP2 RATs.

 Value: "cdma_roaming_networks_string_array"

### KEY_CELLULAR_SERVICE_CAPABILITIES_INT_ARRAY

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CELLULAR_SERVICE_CAPABILITIES_INT_ARRAY: String
```

An array of cellular services supported by a subscription.

Permissible values include:

- `SubscriptionManager#SERVICE_CAPABILITY_VOICE` for voice services
- `SubscriptionManager#SERVICE_CAPABILITY_SMS` for SMS services
- `SubscriptionManager#SERVICE_CAPABILITY_DATA` for data services

Carrier-specific factors may influence how these services are supported. Therefore, modifying this carrier configuration might not always enable the specified services. These capability bitmasks should be considered as indicators of a carrier's preferred services to enhance user experience, rather than as absolute platform guarantees.

Device-level service capabilities, defined by `TelephonyManager#isDeviceVoiceCapable` and `TelephonyManager#isDeviceSmsCapable`, take precedence over these subscription-level settings. For instance, a device where `TelephonyManager#isDeviceVoiceCapable` returns false may not be able to make voice calls, even if subscribed to a service marked as voice-capable.

To determine a subscription's cellular service capabilities, use `SubscriptionInfo#getServiceCapabilities()`. To track changes in services, register a `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.OnSubscriptionsChangedListener` and invoke the same method in its callback.

Emergency service availability may not depend on the cellular service capabilities. For example, emergency calls might be possible on a subscription even if it lacks `SubscriptionManager#SERVICE_CAPABILITY_VOICE`.

If unset, the default value is "\[1, 2, 3\]" (supports all cellular services).

 Value: "cellular_service_capabilities_int_array"

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#isDeviceVoiceCapable()`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#isDeviceSmsCapable()`
- `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo#getServiceCapabilities()`
- `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.OnSubscriptionsChangedListener`

### KEY_CELLULAR_USAGE_SETTING_INT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CELLULAR_USAGE_SETTING_INT: String
```

Controls the cellular usage setting. The usage setting indicates whether a device will remain attached to a network based on the primary use case for the service. A device will detach and search for a more-preferred network if the primary use case (voice or data) is not satisfied. Depending on the type of device, it may operate in a voice or data-centric mode by default.

Sets the usage setting in accordance with 3gpp 24.301 sec 4.3 and 3gpp 24.501 sec 4.3. Also refer to "UE's usage setting" as defined in 3gpp 24.301 section 3.1 and 3gpp 23.221 Annex A. Either omit this key or pass a value of `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#USAGE_SETTING_UNKNOWN:kotlin.Int` to preserve the current setting.

Devices that support configuration of the cellular usage setting, including devices with HAL capability to set the cellular usage setting, must honor this setting accordingly. `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#USAGE_SETTING_DEFAULT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#USAGE_SETTING_VOICE_CENTRIC:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#USAGE_SETTING_DATA_CENTRIC:kotlin.Int`.

 Value: "cellular_usage_setting_int"

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo#getUsageSetting()`

### KEY_CHECK_PRICING_WITH_CARRIER_FOR_DATA_ROAMING_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CHECK_PRICING_WITH_CARRIER_FOR_DATA_ROAMING_BOOL: String
```

Determines whether we should show a warning asking the user to check with their carrier on pricing when the user enabled data roaming, default to false.

 Value: "check_pricing_with_carrier_data_roaming_bool"

### KEY_CI_ACTION_ON_SYS_UPDATE_BOOL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CI_ACTION_ON_SYS_UPDATE_BOOL: String
```

Flag specifying whether an additional (client initiated) intent needs to be sent on System update

 Value: "ci_action_on_sys_update_bool"

### KEY_CI_ACTION_ON_SYS_UPDATE_EXTRA_STRING

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CI_ACTION_ON_SYS_UPDATE_EXTRA_STRING: String
```

Extra to be included in the intent sent for additional action on System update

 Value: "ci_action_on_sys_update_extra_string"

### KEY_CI_ACTION_ON_SYS_UPDATE_EXTRA_VAL_STRING

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CI_ACTION_ON_SYS_UPDATE_EXTRA_VAL_STRING: String
```

Value of extra included in intent sent for additional action on System update

 Value: "ci_action_on_sys_update_extra_val_string"

### KEY_CI_ACTION_ON_SYS_UPDATE_INTENT_STRING

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CI_ACTION_ON_SYS_UPDATE_INTENT_STRING: String
```

Intent to be sent for the additional action on System update

 Value: "ci_action_on_sys_update_intent_string"

### KEY_CONFIG_IMS_MMTEL_PACKAGE_OVERRIDE_STRING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CONFIG_IMS_MMTEL_PACKAGE_OVERRIDE_STRING: String
```

The package name containing the ImsService that will be bound to the telephony framework to support IMS MMTEL feature functionality instead of the device default ImsService for this subscription.

 Value: "config_ims_mmtel_package_override_string"

### KEY_CONFIG_IMS_PACKAGE_OVERRIDE_STRING

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CONFIG_IMS_PACKAGE_OVERRIDE_STRING: String
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CONFIG_IMS_MMTEL_PACKAGE_OVERRIDE_STRING:kotlin.String` and `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CONFIG_IMS_RCS_PACKAGE_OVERRIDE_STRING:kotlin.String` instead to configure these values separately. If any of those values are not empty, they will override this value.*

The package name containing the ImsService that will be bound to the telephony framework to support both IMS MMTEL and RCS feature functionality instead of the device default ImsService for this subscription.

 Value: "config_ims_package_override_string"

### KEY_CONFIG_IMS_RCS_PACKAGE_OVERRIDE_STRING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CONFIG_IMS_RCS_PACKAGE_OVERRIDE_STRING: String
```

The package name containing the ImsService that will be bound to the telephony framework to support IMS RCS feature functionality instead of the device default ImsService for this subscription.

 Value: "config_ims_rcs_package_override_string"

### KEY_CONFIG_PLANS_PACKAGE_OVERRIDE_STRING

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CONFIG_PLANS_PACKAGE_OVERRIDE_STRING: String
```

Override the package that will manage `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan` information instead of the `https://developer.android.com/reference/kotlin/android/service/carrier/CarrierService.html#` that defines this value.

 Value: "config_plans_package_override_string"

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getSubscriptionPlans(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#setSubscriptionPlans(kotlin.Int,%20kotlin.collections.MutableList)`

### KEY_CONFIG_TELEPHONY_USE_OWN_NUMBER_FOR_VOICEMAIL_BOOL

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CONFIG_TELEPHONY_USE_OWN_NUMBER_FOR_VOICEMAIL_BOOL: String
```

Flag that specifies to use the user's own phone number as the voicemail number when there is no pre-loaded voicemail number on the SIM card.

`https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_DEFAULT_VM_NUMBER_STRING:kotlin.String` takes precedence over this flag.

If false, the system default (\*86) will be used instead.

 Value: "config_telephony_use_own_number_for_voicemail_bool"

### KEY_CONFIG_WIFI_DISABLE_IN_ECBM

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CONFIG_WIFI_DISABLE_IN_ECBM: String
```

Flag to indicate if Wi-Fi needs to be disabled in ECBM.

 Value: "config_wifi_disable_in_ecbm"

### KEY_CROSS_SIM_SPN_FORMAT_INT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CROSS_SIM_SPN_FORMAT_INT: String
```

Indexes of SPN format strings in crossSimSpnFormats.

Available options are:

- `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#CROSS_SIM_SPN_FORMAT_CARRIER_NAME_ONLY:kotlin.Int`: %s
- `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#CROSS_SIM_SPN_FORMAT_CARRIER_NAME_WITH_BRANDING:kotlin.Int`: %s Cross-SIM Calling

%s will be filled with carrier name

 Value: "cross_sim_spn_format_int"

### KEY_CSP_ENABLED_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CSP_ENABLED_BOOL: String
```

If this is true, the SIM card (through Customer Service Profile EF file) will be able to prevent manual operator selection. If false, this SIM setting will be ignored and manual operator selection will always be available. See CPHS4_2.WW6, CPHS B.4.7.1 for more information

 Value: "csp_enabled_bool"

### KEY_DATA_LIMIT_NOTIFICATION_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_DATA_LIMIT_NOTIFICATION_BOOL: String
```

Controls if the device should automatically notify the user as they reach their cellular data limit. When set to `false` the carrier is expected to have implemented their own notification mechanism. `true` by default.

 Value: "data_limit_notification_bool"

### KEY_DATA_LIMIT_THRESHOLD_BYTES_LONG

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_DATA_LIMIT_THRESHOLD_BYTES_LONG: String
```

Controls the cellular data limit.

If the user uses more than this amount of data in their billing cycle, as defined by `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MONTHLY_DATA_CYCLE_DAY_INT:kotlin.String`, cellular data will be turned off by the user's phone. If the value is set to `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#DATA_CYCLE_THRESHOLD_DISABLED:kotlin.Int`, the data limit will be disabled.

This setting may be overridden by explicit user choice. By default, `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#DATA_CYCLE_USE_PLATFORM_DEFAULT:kotlin.Int` will be used.

 Value: "data_limit_threshold_bytes_long"

### KEY_DATA_RAPID_NOTIFICATION_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_DATA_RAPID_NOTIFICATION_BOOL: String
```

Controls if the device should automatically notify the user when rapid cellular data usage is observed. When set to `false` the carrier is expected to have implemented their own notification mechanism. `true` by default.

 Value: "data_rapid_notification_bool"

### KEY_DATA_SWITCH_VALIDATION_MIN_INTERVAL_MILLIS_LONG

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_DATA_SWITCH_VALIDATION_MIN_INTERVAL_MILLIS_LONG: String
```

Data switch validation minimal interval, in milliseconds. If a connection to the default (Internet) PDN for the current subscription is validated on a given operator within a given tracking area, re-validations to that matching operator will be skipped if they would occur within the specified interval. Instead, the connection will automatically considered validated. If the network was validated within the interval but the latest validation result was false, the validation will not be skipped. If not set or set to 0, validation will not be skipped. The valid range of value is between 0 millisecond and 24 hours, inclusive in both sides. The default value is 24 hours.

 Value: "data_switch_validation_min_gap_long"

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities.html#NET_CAPABILITY_VALIDATED:kotlin.Int`

### KEY_DATA_SWITCH_VALIDATION_TIMEOUT_LONG

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_DATA_SWITCH_VALIDATION_TIMEOUT_LONG: String
```

Upon data switching between subscriptions within a carrier group, if switch depends on validation result, this value defines customized value of how long we wait for validation success before we fail and revoke the switch. Time out is in milliseconds.

 Value: "data_switch_validation_timeout_long"

### KEY_DATA_WARNING_NOTIFICATION_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_DATA_WARNING_NOTIFICATION_BOOL: String
```

Controls if the device should automatically notify the user as they reach their cellular data warning. When set to `false` the carrier is expected to have implemented their own notification mechanism. `true` by default.

 Value: "data_warning_notification_bool"

### KEY_DATA_WARNING_THRESHOLD_BYTES_LONG

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_DATA_WARNING_THRESHOLD_BYTES_LONG: String
```

Controls the data usage warning.

If the user uses more than this amount of data in their billing cycle, as defined by `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_MONTHLY_DATA_CYCLE_DAY_INT:kotlin.String`, the user will be alerted about the usage. If the value is set to `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#DATA_CYCLE_THRESHOLD_DISABLED:kotlin.Int`, the data usage warning will be disabled.

This setting may be overridden by explicit user choice. By default, `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#DATA_CYCLE_USE_PLATFORM_DEFAULT:kotlin.Int` will be used.

 Value: "data_warning_threshold_bytes_long"

### KEY_DEFAULT_SIM_CALL_MANAGER_STRING

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_DEFAULT_SIM_CALL_MANAGER_STRING: String
```

The default sim call manager to use when the default dialer doesn't implement one. A sim call manager can control and route outgoing and incoming phone calls, even if they're placed using another connection service (PSTN, for example).

 Value: "default_sim_call_manager_string"

### KEY_DEFAULT_VM_NUMBER_ROAMING_AND_IMS_UNREGISTERED_STRING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_DEFAULT_VM_NUMBER_ROAMING_AND_IMS_UNREGISTERED_STRING: String
```

Where there is no preloaded voicemail number on a SIM card, specifies the carrier's default voicemail number while the device is both roaming and not registered for IMS. When empty string, no default voicemail number is specified for roaming network and unregistered state in IMS.

 Value: "default_vm_number_roaming_and_ims_unregistered_string"

### KEY_DEFAULT_VM_NUMBER_STRING

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_DEFAULT_VM_NUMBER_STRING: String
```

Where there is no preloaded voicemail number on a SIM card, specifies the carrier's default voicemail number. When empty string, no default voicemail number is specified.

 Value: "default_vm_number_string"

### KEY_DIAL_STRING_REPLACE_STRING_ARRAY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_DIAL_STRING_REPLACE_STRING_ARRAY: String
```

Specifies a map from dialstrings to replacements for roaming network service numbers which cannot be replaced on the carrier side.

Individual entries have the format: \[dialstring to replace\]:\[replacement\]

 Value: "dial_string_replace_string_array"

### KEY_DISABLE_CDMA_ACTIVATION_CODE_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_DISABLE_CDMA_ACTIVATION_CODE_BOOL: String
```

**Deprecated:** *Legacy CDMA is unsupported.*

Disables dialing "\*228" (OTASP provisioning) on CDMA carriers where it is not supported or is potentially harmful by locking the SIM to 3G.

 Value: "disable_cdma_activation_code_bool"

### KEY_DISABLE_CHARGE_INDICATION_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_DISABLE_CHARGE_INDICATION_BOOL: String
```

The flag to disable the popup dialog which warns the user of data charges.

 Value: "disable_charge_indication_bool"

### KEY_DISABLE_DUN_APN_WHILE_ROAMING_WITH_PRESET_APN_BOOL

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_DISABLE_DUN_APN_WHILE_ROAMING_WITH_PRESET_APN_BOOL: String
```

Indicating whether DUN APN should be disabled when the device is roaming. In that case, the default APN (i.e. internet) will be used for tethering. This config is only available when using Preset APN(not user edited) as Preferred APN.

 Value: "disable_dun_apn_while_roaming_with_preset_apn_bool"

### KEY_DISABLE_SUPPLEMENTARY_SERVICES_IN_AIRPLANE_MODE_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_DISABLE_SUPPLEMENTARY_SERVICES_IN_AIRPLANE_MODE_BOOL: String
```

Boolean indicating the Supplementary Services(SS) is disable when airplane mode on in the Call Settings menu. `true`: SS is disable when airplane mode on. `false`: SS is enable when airplane mode on. The default value for this key is `false`

 Value: "disable_supplementary_services_in_airplane_mode_bool"

### KEY_DISALLOW_ADDING_APN_STRING_ARRAY

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_DISALLOW_ADDING_APN_STRING_ARRAY: String
```

Specifies disallowed substrings for the `https://developer.android.com/reference/kotlin/android/provider/Telephony.Carriers.html#APN:kotlin.String`. Note: If the preset APN contains these strings, then adding or editing is not allowed.

 Value: "disallow_adding_apn_string_array"

### KEY_DISCONNECT_CAUSE_PLAY_BUSYTONE_INT_ARRAY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_DISCONNECT_CAUSE_PLAY_BUSYTONE_INT_ARRAY: String
```

DisconnectCause array to play busy tone. Value should be array of `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause`.

 Value: "disconnect_cause_play_busytone_int_array"

### KEY_DISPLAY_CALL_STRENGTH_INDICATOR_BOOL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_DISPLAY_CALL_STRENGTH_INDICATOR_BOOL: String
```

Determine whether or not to display a call strength indicator for this carrier in the System UI. Disabling the indication may be reasonable if the carrier's calling is not integrated into the Android telephony stack (e.g. it is OTT). true: Use telephony APIs to detect the current networking medium of calling and display a UI indication based on the current strength (e.g. signal level) of that medium. false: Do not display the call strength indicator.

 Value: "display_call_strength_indicator_bool"

### KEY_DISPLAY_HD_AUDIO_PROPERTY_BOOL

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_DISPLAY_HD_AUDIO_PROPERTY_BOOL: String
```

Determines whether High Definition audio property is displayed in the dialer UI. If `false`, remove the HD audio property from the connection so that HD audio related UI is not displayed. If `true`, keep HD audio property as it is configured.

 Value: "display_hd_audio_property_bool"

### KEY_DROP_VIDEO_CALL_WHEN_ANSWERING_AUDIO_CALL_BOOL

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_DROP_VIDEO_CALL_WHEN_ANSWERING_AUDIO_CALL_BOOL: String
```

When `true`, if the user is in an ongoing video call over WIFI and answers an incoming audio call, the video call will be disconnected before the audio call is answered. This is in contrast to the usual expected behavior where a foreground video call would be put into the background and held when an incoming audio call is answered.

 Value: "drop_video_call_when_answering_audio_call_bool"

### KEY_DTMF_TYPE_ENABLED_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_DTMF_TYPE_ENABLED_BOOL: String
```

Flag indicating if dtmf tone type is enabled

 Value: "dtmf_type_enabled_bool"

### KEY_DURATION_BLOCKING_DISABLED_AFTER_EMERGENCY_INT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_DURATION_BLOCKING_DISABLED_AFTER_EMERGENCY_INT: String
```

The duration in seconds that platform call and message blocking is disabled after the user contacts emergency services. Platform considers values for below cases: 1) 0 \<= VALUE \<= 604800(one week): the value will be used as the duration directly. 2) VALUE \> 604800(one week): will use the default value as duration instead. 3) VALUE \< 0: block will be disabled forever until user re-enable block manually, the suggested value to disable forever is -1. See `android.provider.BlockedNumberContract#notifyEmergencyContact(Context)` See `android.provider.BlockedNumberContract#isBlocked(Context, String)`.

 Value: "duration_blocking_disabled_after_emergency_int"

### KEY_EDITABLE_ENHANCED_4G_LTE_BOOL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_EDITABLE_ENHANCED_4G_LTE_BOOL: String
```

Determine whether user can toggle Enhanced 4G LTE Mode in Settings.

 Value: "editable_enhanced_4g_lte_bool"

### KEY_EDITABLE_VOICEMAIL_NUMBER_BOOL

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_EDITABLE_VOICEMAIL_NUMBER_BOOL: String
```

Since the default voicemail number is empty, if a SIM card does not have a voicemail number available the user cannot use voicemail. This flag allows the user to edit the voicemail number in such cases, and is false by default.

 Value: "editable_voicemail_number_bool"

### KEY_EDITABLE_VOICEMAIL_NUMBER_SETTING_BOOL

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_EDITABLE_VOICEMAIL_NUMBER_SETTING_BOOL: String
```

Determine whether user can edit voicemail number in Settings.

 Value: "editable_voicemail_number_setting_bool"

### KEY_EDITABLE_WFC_MODE_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_EDITABLE_WFC_MODE_BOOL: String
```

Determine whether user can switch Wi-Fi preferred or Cellular preferred in calling preference. Some operators support Wi-Fi Calling only, not VoLTE. They don't need "Cellular preferred" option. In this case, set uneditable attribute for preferred preference.

 Value: "editable_wfc_mode_bool"

### KEY_EDITABLE_WFC_ROAMING_MODE_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_EDITABLE_WFC_ROAMING_MODE_BOOL: String
```

Determine whether user can change Wi-Fi Calling preference in roaming. `false` - roaming preference cannot be changed by user independently. If `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_USE_WFC_HOME_NETWORK_MODE_IN_ROAMING_NETWORK_BOOL:kotlin.String` is false, `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_DEFAULT_WFC_IMS_ROAMING_MODE_INT:kotlin.String` is used as the default value. If `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_USE_WFC_HOME_NETWORK_MODE_IN_ROAMING_NETWORK_BOOL:kotlin.String` is true, roaming preference is the same as home preference and `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_DEFAULT_WFC_IMS_MODE_INT:kotlin.String` is used as the default value. `true` - roaming preference can be changed by user independently if `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_USE_WFC_HOME_NETWORK_MODE_IN_ROAMING_NETWORK_BOOL:kotlin.String` is false. If `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_USE_WFC_HOME_NETWORK_MODE_IN_ROAMING_NETWORK_BOOL:kotlin.String` is true, this configuration is ignored and roaming preference cannot be changed.

 Value: "editable_wfc_roaming_mode_bool"

### KEY_EMERGENCY_CALL_TO_SATELLITE_T911_HANDOVER_TIMEOUT_MILLIS_INT

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_EMERGENCY_CALL_TO_SATELLITE_T911_HANDOVER_TIMEOUT_MILLIS_INT: String
```

An integer key holds the timeout duration in milliseconds used to determine whether to hand over an emergency call to satellite T911. The timer is started when there is an ongoing emergency call, and the IMS is not registered, and cellular service is not available. When the timer expires, com.android.internal.telephony.satellite.SatelliteSOSMessageRecommender will send the event `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EVENT_DISPLAY_EMERGENCY_MESSAGE:kotlin.String` to Dialer, which will then prompt user to switch to using satellite emergency messaging. The default value is 30 seconds.

 Value: "emergency_call_to_satellite_t911_handover_timeout_millis_int"

### KEY_EMERGENCY_MESSAGING_SUPPORTED_BOOL

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_EMERGENCY_MESSAGING_SUPPORTED_BOOL: String
```

Indicate whether a carrier supports emergency messaging. When this config is `false`, emergency call to satellite T911 handover will be disabled. This will need agreement with carriers before enabling this flag. The default value is false.

 Value: "emergency_messaging_supported_bool"

### KEY_EMERGENCY_NOTIFICATION_DELAY_INT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_EMERGENCY_NOTIFICATION_DELAY_INT: String
```

Time delay (in ms) after which we show the notification for emergency calls, while the device is registered over WFC. Default value is -1, which indicates that this notification is not pertinent for a particular carrier. We've added a delay to prevent false positives.

 Value: "emergency_notification_delay_int"

### KEY_EMERGENCY_NUMBER_PREFIX_STRING_ARRAY

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_EMERGENCY_NUMBER_PREFIX_STRING_ARRAY: String
```

Indicates zero or more emergency number prefix(es), because some carrier requires if users dial an emergency number address with a specific prefix, the combination of the prefix and the address is also a valid emergency number to dial. For example, an emergency number prefix is 318, and the emergency number is 911. Both 318911 and 911 can be dialed by users for emergency call. An empty array of string indicates that current carrier does not have this requirement.

 Value: "emergency_number_prefix_string_array"

### KEY_ENABLE_4G_OPPORTUNISTIC_NETWORK_SCAN_BOOL

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ENABLE_4G_OPPORTUNISTIC_NETWORK_SCAN_BOOL: String
```

Controls whether 4G opportunistic networks should be scanned for possible data switch.

 Value: "enabled_4g_opportunistic_network_scan_bool"

### KEY_ENABLE_CROSS_SIM_CALLING_ON_OPPORTUNISTIC_DATA_BOOL

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ENABLE_CROSS_SIM_CALLING_ON_OPPORTUNISTIC_DATA_BOOL: String
```

Flag specifying whether cross sim calling on opportunistic data is supported for carrier. When `false` the carrier does not support cross sim calling on opportunistic data. When `true` the carrier does support cross sim calling on opportunistic data.

 Value: "enable_cross_sim_calling_on_opportunistic_data_bool"

### KEY_ENABLE_DIALER_KEY_VIBRATION_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ENABLE_DIALER_KEY_VIBRATION_BOOL: String
```

If true, enable vibration (haptic feedback) for key presses in the EmergencyDialer activity. The pattern is set on a per-platform basis using config_virtualKeyVibePattern. To be consistent with the regular Dialer, this value should agree with the corresponding values from config.xml under apps/Contacts.

 Value: "enable_dialer_key_vibration_bool"

### KEY_ENHANCED_4G_LTE_ON_BY_DEFAULT_BOOL

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ENHANCED_4G_LTE_ON_BY_DEFAULT_BOOL: String
```

Sets the default state for the "Enhanced 4G LTE" or "Advanced Calling" mode toggle set by the user. When this is `true`, this mode by default is on, otherwise if `false`, this mode by default is off.

 Value: "enhanced_4g_lte_on_by_default_bool"

### KEY_ENHANCED_4G_LTE_TITLE_VARIANT_INT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ENHANCED_4G_LTE_TITLE_VARIANT_INT: String
```

The index indicates the carrier specified title string of Enhanced 4G LTE Mode settings. Default value is 0, which indicates the default title string.

 Value: "enhanced_4g_lte_title_variant_int"

### KEY_ESIM_DOWNLOAD_RETRY_BACKOFF_TIMER_SEC_INT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ESIM_DOWNLOAD_RETRY_BACKOFF_TIMER_SEC_INT: String
```

This timer value is used in the eSIM Exponential Backoff download retry algorithm. Value should be in seconds.

1. When the first download failure occurs, retry download after BACKOFF_TIMER_VALUE seconds.
2. If download fails again then, retry after either BACKOFF_TIMER_VALUE, 2xBACKOFF_TIMER_VALUE, or 3xBACKOFF_TIMER_VALUE seconds.
3. In general after the cth failed attempt, retry after k \* BACKOFF_TIMER_VALUE seconds, where k is a random integer between 1 and 2\^c − 1. Max c value is `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_ESIM_MAX_DOWNLOAD_RETRY_ATTEMPTS_INT:kotlin.String`

<br />

 Value: "esim_download_retry_backoff_timer_sec_int"

### KEY_ESIM_MAX_DOWNLOAD_RETRY_ATTEMPTS_INT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ESIM_MAX_DOWNLOAD_RETRY_ATTEMPTS_INT: String
```

If eSIM profile download fails then, the number of retry attempts by UE will be based on this configuration. If download still fails even after the MAX attempts configured by this item then the retry is postponed until next device bootup.

 Value: "esim_max_download_retry_attempts_int"

### KEY_FORCE_HOME_NETWORK_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_FORCE_HOME_NETWORK_BOOL: String
```

Override the platform's notion of a network operator being considered non roaming. If true all networks are considered as home network a.k.a. non-roaming. When false, the 2 pairs of CMDA and GSM roaming/non-roaming arrays are consulted.

 Value: "force_home_network_bool"

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_GSM_ROAMING_NETWORKS_STRING_ARRAY:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_GSM_NONROAMING_NETWORKS_STRING_ARRAY:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CDMA_ROAMING_NETWORKS_STRING_ARRAY:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CDMA_NONROAMING_NETWORKS_STRING_ARRAY:kotlin.String`

### KEY_GSM_DTMF_TONE_DELAY_INT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_GSM_DTMF_TONE_DELAY_INT: String
```

Specifies the amount of gap to be added in millis between postdial DTMF tones. When a non-zero value is specified, the UE shall wait for the specified amount of time before it sends out successive DTMF tones on the network.

 Value: "gsm_dtmf_tone_delay_int"

### KEY_GSM_NONROAMING_NETWORKS_STRING_ARRAY

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_GSM_NONROAMING_NETWORKS_STRING_ARRAY: String
```

Override the platform's notion of a network operator being considered not roaming. Value is string array of MCCMNCs to be considered not roaming for 3GPP RATs.

 Value: "gsm_nonroaming_networks_string_array"

### KEY_GSM_ROAMING_NETWORKS_STRING_ARRAY

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_GSM_ROAMING_NETWORKS_STRING_ARRAY: String
```

Override the platform's notion of a network operator being considered roaming. Value is string array of MCCMNCs to be considered roaming for 3GPP RATs.

 Value: "gsm_roaming_networks_string_array"

### KEY_HAS_IN_CALL_NOISE_SUPPRESSION_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_HAS_IN_CALL_NOISE_SUPPRESSION_BOOL: String
```

Determines if device implements a noise suppression device for in call audio.

 Value: "has_in_call_noise_suppression_bool"

### KEY_HIDE_CARRIER_NETWORK_SETTINGS_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_HIDE_CARRIER_NETWORK_SETTINGS_BOOL: String
```

Control whether users can reach the carrier portions of Cellular Network Settings.

 Value: "hide_carrier_network_settings_bool"

### KEY_HIDE_ENHANCED_4G_LTE_BOOL

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_HIDE_ENHANCED_4G_LTE_BOOL: String
```

Determines whether the Enhanced 4G LTE toggle will be shown in the settings. When this option is `true`, the toggle will be hidden regardless of whether the device and carrier supports 4G LTE or not.

 Value: "hide_enhanced_4g_lte_bool"

### KEY_HIDE_IMS_APN_BOOL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_HIDE_IMS_APN_BOOL: String
```

Determine whether IMS apn can be shown.

 Value: "hide_ims_apn_bool"

### KEY_HIDE_LTE_PLUS_DATA_ICON_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_HIDE_LTE_PLUS_DATA_ICON_BOOL: String
```

Boolean indicating if LTE+ icon should be shown if available.

 Value: "hide_lte_plus_data_icon_bool"

### KEY_HIDE_PREFERRED_NETWORK_TYPE_BOOL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_HIDE_PREFERRED_NETWORK_TYPE_BOOL: String
```

Determine whether preferred network type can be shown.

 Value: "hide_preferred_network_type_bool"

### KEY_HIDE_PRESET_APN_DETAILS_BOOL

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_HIDE_PRESET_APN_DETAILS_BOOL: String
```

Flag to hide Preset APN details. If true, user cannot enter ApnEditor view of Preset APN, and cannot view details of the APN. If false, user can enter ApnEditor view of Preset APN. Default value is false.

 Value: "hide_preset_apn_details_bool"

### KEY_HIDE_SIM_LOCK_SETTINGS_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_HIDE_SIM_LOCK_SETTINGS_BOOL: String
```

Control whether users can reach the SIM lock settings.

 Value: "hide_sim_lock_settings_bool"

### KEY_HIDE_TTY_HCO_VCO_WITH_RTT_BOOL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_HIDE_TTY_HCO_VCO_WITH_RTT_BOOL: String
```

Indicates if the TTY HCO and VCO options should be hidden in the accessibility menu if the device is capable of RTT.

 Value: "hide_tty_hco_vco_with_rtt"

### KEY_IGNORE_DATA_ENABLED_CHANGED_FOR_VIDEO_CALLS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_IGNORE_DATA_ENABLED_CHANGED_FOR_VIDEO_CALLS: String
```

When `true`, changes to the mobile data enabled switch will not cause the VT registration state to change. That is, turning on or off mobile data will not cause VT to be enabled or disabled. When `false`, disabling mobile data will cause VT to be de-registered.

 Value: "ignore_data_enabled_changed_for_video_calls"

### KEY_IGNORE_RTT_MODE_SETTING_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_IGNORE_RTT_MODE_SETTING_BOOL: String
```

When `true`, the phone will always tell the IMS stack to keep RTT enabled and determine on a per-call basis (based on extras from the dialer app) whether a call should be an RTT call or not. When `false`, the old behavior is used, where the toggle in accessibility settings is used to set the IMS stack's RTT enabled state.

 Value: "ignore_rtt_mode_setting_bool"

### KEY_IGNORE_SIM_NETWORK_LOCKED_EVENTS_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_IGNORE_SIM_NETWORK_LOCKED_EVENTS_BOOL: String
```

Flag indicating whether the Phone app should ignore EVENT_SIM_NETWORK_LOCKED events from the Sim. If true, this will prevent the IccNetworkDepersonalizationPanel from being shown, and effectively disable the "Sim network lock" feature.

 Value: "ignore_sim_network_locked_events_bool"

### KEY_IMS_CONFERENCE_SIZE_LIMIT_INT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_IMS_CONFERENCE_SIZE_LIMIT_INT: String
```

Determines the maximum number of participants the carrier supports for a conference call. This number is exclusive of the current device. A conference between 3 devices, for example, would have a size limit of 2 participants. Enforced when `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_IS_IMS_CONFERENCE_SIZE_ENFORCED_BOOL:kotlin.String` is `true`.

 Value: "ims_conference_size_limit_int"

### KEY_IMS_DTMF_TONE_DELAY_INT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_IMS_DTMF_TONE_DELAY_INT: String
```

Specifies the amount of gap to be added in millis between DTMF tones. When a non-zero value is specified, the UE shall wait for the specified amount of time before it sends out successive DTMF tones on the network.

 Value: "ims_dtmf_tone_delay_int"

### KEY_INCLUDE_LTE_FOR_NR_ADVANCED_THRESHOLD_BANDWIDTH_BOOL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_INCLUDE_LTE_FOR_NR_ADVANCED_THRESHOLD_BANDWIDTH_BOOL: String
```

Indicating whether to include LTE cell bandwidths when determining whether the aggregated cell bandwidth meets the required threshold for NR advanced.

 Value: "include_lte_for_nr_advanced_threshold_bandwidth_bool"

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyDisplayInfo#OVERRIDE_NETWORK_TYPE_NR_ADVANCED:kotlin.Int`

### KEY_IS_IMS_CONFERENCE_SIZE_ENFORCED_BOOL

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_IS_IMS_CONFERENCE_SIZE_ENFORCED_BOOL: String
```

Determines whether a maximum size limit for IMS conference calls is enforced on the device. When `true`, IMS conference calls will be limited to at most `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_IMS_CONFERENCE_SIZE_LIMIT_INT:kotlin.String` participants. When `false`, no attempt is made to limit the number of participants in a conference (the carrier will raise an error when an attempt is made to merge too many participants into a conference).

Note: The maximum size of a conference can ONLY be supported where `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SUPPORT_IMS_CONFERENCE_EVENT_PACKAGE_BOOL:kotlin.String` is `true` since the platform needs conference event package data to accurately know the number of participants in the conference.

 Value: "is_ims_conference_size_enforced_bool"

### KEY_IS_OPPORTUNISTIC_SUBSCRIPTION_BOOL

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_IS_OPPORTUNISTIC_SUBSCRIPTION_BOOL: String
```

A boolean property indicating whether this subscription should be managed as an opportunistic subscription. If true, then this subscription will be selected based on available coverage and will not be available for a user in settings menus for selecting macro network providers. If unset, defaults to "false".

This key will work all the way back to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int`.

 Value: "is_opportunistic_subscription_bool"

### KEY_IS_PRIVATE_NETWORK_BOOL

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_IS_PRIVATE_NETWORK_BOOL: String
```

Controls whether the subscription is used exclusively for private networks.

If `true`, this subscription will be considered a private network subscription. System apps like Settings and SystemUI may adjust their behavior based on this flag.

 Value: "is_private_network_bool"

### KEY_LOG_CALLS_ANSWERED_ELSEWHERE_BOOL

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_LOG_CALLS_ANSWERED_ELSEWHERE_BOOL: String
```

Flag indicating whether to log calls which were answered on another device.

If `true`, calls which are disconnected with `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause.html#ANSWERED_ELSEWHERE:kotlin.Int` will be added to the call log.

If `false`, these calls will not be added to the call log. The default value is `true`.

 Value: "log_calls_answered_elsewhere_bool"

### KEY_LOW_BATTERY_ALERT_INTERVAL_INT

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_LOW_BATTERY_ALERT_INTERVAL_INT: String
```

Interval between consecutive battery alert tones, in seconds.

This flag controls how frequently (in seconds) an alert tone should be played after the battery level drops below the defined threshold. A shorter interval means more frequent alerts.

Type: Integer

Valid values: 0 or greater

Default value: `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount.html#LOW_BATTERY_ALERT_DISABLED:kotlin.Int` (feature disabled)

If set to `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount.html#LOW_BATTERY_ALERT_DISABLED:kotlin.Int`, the alert tone is disabled entirely.

 Value: "low_battery_alert_interval_int"

### KEY_LOW_BATTERY_ALERT_THRESHOLD_INT

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_LOW_BATTERY_ALERT_THRESHOLD_INT: String
```

Battery level threshold (in percentage) to trigger an audio alert.

This flag defines the minimum battery percentage at which an audio alert will be played. When the device battery level falls below this threshold, a tone or audio warning may be triggered to notify the user.

Type: Integer

Valid values: 0--100

Default value: `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount.html#LOW_BATTERY_ALERT_DISABLED:kotlin.Int` (feature disabled)

If the value is set to `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount.html#LOW_BATTERY_ALERT_DISABLED:kotlin.Int`, the audio alert for low battery is not enabled.

 Value: "low_battery_alert_threshold_int"

### KEY_LTE_ENABLED_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_LTE_ENABLED_BOOL: String
```

Boolean to decide whether LTE is enabled.

 Value: "lte_enabled_bool"

### KEY_LTE_RSRQ_THRESHOLDS_INT_ARRAY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_LTE_RSRQ_THRESHOLDS_INT_ARRAY: String
```

A list of 4 customized LTE Reference Signal Received Quality (RSRQ) thresholds. Reference: TS 136.133 v12.6.0 section 9.1.7 - RSRQ Measurement Report Mapping. 4 threshold integers must be within the boundaries \[-34 dB, 3 dB\], and the levels are: "NONE: \[-34, threshold1)" "POOR: \[threshold1, threshold2)" "MODERATE: \[threshold2, threshold3)" "GOOD: \[threshold3, threshold4)" "EXCELLENT: \[threshold4, 3\]" This key is considered invalid if the format is violated. If the key is invalid or not configured, a default value set will apply.

 Value: "lte_rsrq_thresholds_int_array"

### KEY_LTE_RSSNR_THRESHOLDS_INT_ARRAY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_LTE_RSSNR_THRESHOLDS_INT_ARRAY: String
```

A list of 4 customized LTE Reference Signal Signal to Noise Ratio (RSSNR) thresholds. 4 threshold integers must be within the boundaries \[-20 dB, 30 dB\], and the levels are: "NONE: \[-20, threshold1)" "POOR: \[threshold1, threshold2)" "MODERATE: \[threshold2, threshold3)" "GOOD: \[threshold3, threshold4)" "EXCELLENT: \[threshold4, 30\]" This key is considered invalid if the format is violated. If the key is invalid or not configured, a default value set will apply.

 Value: "lte_rssnr_thresholds_int_array"

### KEY_MDN_IS_ADDITIONAL_VOICEMAIL_NUMBER_BOOL

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MDN_IS_ADDITIONAL_VOICEMAIL_NUMBER_BOOL: String
```

When checking if a given number is the voicemail number, if this flag is true then in addition to comparing the given number to the voicemail number, we also compare it to the mdn. If this flag is false, the given number is only compared to the voicemail number. By default this value is false.

 Value: "mdn_is_additional_voicemail_number_bool"

### KEY_MMS_ALIAS_ENABLED_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MMS_ALIAS_ENABLED_BOOL: String
```

 Value: "aliasEnabled"

### KEY_MMS_ALIAS_MAX_CHARS_INT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MMS_ALIAS_MAX_CHARS_INT: String
```

 Value: "aliasMaxChars"

### KEY_MMS_ALIAS_MIN_CHARS_INT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MMS_ALIAS_MIN_CHARS_INT: String
```

 Value: "aliasMinChars"

### KEY_MMS_ALLOW_ATTACH_AUDIO_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MMS_ALLOW_ATTACH_AUDIO_BOOL: String
```

 Value: "allowAttachAudio"

### KEY_MMS_APPEND_TRANSACTION_ID_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MMS_APPEND_TRANSACTION_ID_BOOL: String
```

 Value: "enabledTransID"

### KEY_MMS_CLOSE_CONNECTION_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MMS_CLOSE_CONNECTION_BOOL: String
```

If true, add "Connection: close" header to MMS HTTP requests so the connection is immediately closed (disabling keep-alive).

 Value: "mmsCloseConnection"

### KEY_MMS_EMAIL_GATEWAY_NUMBER_STRING

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MMS_EMAIL_GATEWAY_NUMBER_STRING: String
```

 Value: "emailGatewayNumber"

### KEY_MMS_GROUP_MMS_ENABLED_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MMS_GROUP_MMS_ENABLED_BOOL: String
```

 Value: "enableGroupMms"

### KEY_MMS_HTTP_PARAMS_STRING

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MMS_HTTP_PARAMS_STRING: String
```

 Value: "httpParams"

### KEY_MMS_HTTP_SOCKET_TIMEOUT_INT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MMS_HTTP_SOCKET_TIMEOUT_INT: String
```

 Value: "httpSocketTimeout"

### KEY_MMS_MAX_IMAGE_HEIGHT_INT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MMS_MAX_IMAGE_HEIGHT_INT: String
```

 Value: "maxImageHeight"

### KEY_MMS_MAX_IMAGE_WIDTH_INT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MMS_MAX_IMAGE_WIDTH_INT: String
```

 Value: "maxImageWidth"

### KEY_MMS_MAX_MESSAGE_SIZE_INT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MMS_MAX_MESSAGE_SIZE_INT: String
```

 Value: "maxMessageSize"

### KEY_MMS_MAX_NTN_PAYLOAD_SIZE_BYTES_INT

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MMS_MAX_NTN_PAYLOAD_SIZE_BYTES_INT: String
```

Maximum size in bytes of the PDU to send or download when connected to a non-terrestrial network. MmsService will return a result code of MMS_ERROR_TOO_LARGE_FOR_TRANSPORT if the PDU exceeds this limit when connected to a non-terrestrial network.

 Value: "mms_max_ntn_payload_size_bytes_int"

### KEY_MMS_MESSAGE_TEXT_MAX_SIZE_INT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MMS_MESSAGE_TEXT_MAX_SIZE_INT: String
```

 Value: "maxMessageTextSize"

### KEY_MMS_MMS_DELIVERY_REPORT_ENABLED_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MMS_MMS_DELIVERY_REPORT_ENABLED_BOOL: String
```

 Value: "enableMMSDeliveryReports"

### KEY_MMS_MMS_ENABLED_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MMS_MMS_ENABLED_BOOL: String
```

 Value: "enabledMMS"

### KEY_MMS_MMS_READ_REPORT_ENABLED_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MMS_MMS_READ_REPORT_ENABLED_BOOL: String
```

 Value: "enableMMSReadReports"

### KEY_MMS_MULTIPART_SMS_ENABLED_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MMS_MULTIPART_SMS_ENABLED_BOOL: String
```

 Value: "enableMultipartSMS"

### KEY_MMS_NAI_SUFFIX_STRING

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MMS_NAI_SUFFIX_STRING: String
```

 Value: "naiSuffix"

### KEY_MMS_NETWORK_RELEASE_TIMEOUT_MILLIS_INT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MMS_NETWORK_RELEASE_TIMEOUT_MILLIS_INT: String
```

Waiting time in milliseconds used before releasing an MMS data call. Not tearing down an MMS data connection immediately helps to reduce the message delivering latency if messaging continues between all parties in the conversation since the same data connection can be reused for further messages. This timer will control how long the data call will be kept alive before being torn down.

 Value: "mms_network_release_timeout_millis_int"

### KEY_MMS_NOTIFY_WAP_MMSC_ENABLED_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MMS_NOTIFY_WAP_MMSC_ENABLED_BOOL: String
```

 Value: "enabledNotifyWapMMSC"

### KEY_MMS_RECIPIENT_LIMIT_INT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MMS_RECIPIENT_LIMIT_INT: String
```

 Value: "recipientLimit"

### KEY_MMS_SEND_MULTIPART_SMS_AS_SEPARATE_MESSAGES_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MMS_SEND_MULTIPART_SMS_AS_SEPARATE_MESSAGES_BOOL: String
```

 Value: "sendMultipartSmsAsSeparateMessages"

### KEY_MMS_SHOW_CELL_BROADCAST_APP_LINKS_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MMS_SHOW_CELL_BROADCAST_APP_LINKS_BOOL: String
```

 Value: "config_cellBroadcastAppLinks"

### KEY_MMS_SMS_DELIVERY_REPORT_ENABLED_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MMS_SMS_DELIVERY_REPORT_ENABLED_BOOL: String
```

 Value: "enableSMSDeliveryReports"

### KEY_MMS_SMS_TO_MMS_TEXT_LENGTH_THRESHOLD_INT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MMS_SMS_TO_MMS_TEXT_LENGTH_THRESHOLD_INT: String
```

 Value: "smsToMmsTextLengthThreshold"

### KEY_MMS_SMS_TO_MMS_TEXT_THRESHOLD_INT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MMS_SMS_TO_MMS_TEXT_THRESHOLD_INT: String
```

 Value: "smsToMmsTextThreshold"

### KEY_MMS_SUBJECT_MAX_LENGTH_INT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MMS_SUBJECT_MAX_LENGTH_INT: String
```

 Value: "maxSubjectLength"

### KEY_MMS_SUPPORT_HTTP_CHARSET_HEADER_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MMS_SUPPORT_HTTP_CHARSET_HEADER_BOOL: String
```

 Value: "supportHttpCharsetHeader"

### KEY_MMS_SUPPORT_MMS_CONTENT_DISPOSITION_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MMS_SUPPORT_MMS_CONTENT_DISPOSITION_BOOL: String
```

 Value: "supportMmsContentDisposition"

### KEY_MMS_UA_PROF_TAG_NAME_STRING

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MMS_UA_PROF_TAG_NAME_STRING: String
```

 Value: "uaProfTagName"

### KEY_MMS_UA_PROF_URL_STRING

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MMS_UA_PROF_URL_STRING: String
```

 Value: "uaProfUrl"

### KEY_MMS_USER_AGENT_STRING

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MMS_USER_AGENT_STRING: String
```

 Value: "userAgent"

### KEY_MONTHLY_DATA_CYCLE_DAY_INT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MONTHLY_DATA_CYCLE_DAY_INT: String
```

The day of the month (1-31) on which the data cycle rolls over.

If the current month does not have this day, the cycle will roll over at the start of the next month.

This setting may be still overridden by explicit user choice. By default, `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#DATA_CYCLE_USE_PLATFORM_DEFAULT:kotlin.Int` will be used.

 Value: "monthly_data_cycle_day_int"

### KEY_NTN_5G_NR_SSRSRP_THRESHOLDS_INT_ARRAY

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_NTN_5G_NR_SSRSRP_THRESHOLDS_INT_ARRAY: String
```

This threshold is used when connected to a non-terrestrial NR network. List of 4 customized 5G SS reference signal received power (SSRSRP) thresholds.

Reference: 3GPP TS 38.215

4 threshold integers must be within the boundaries \[-140 dB, -44 dB\], and the levels are:

- "NONE: \[-140, threshold1)"
- "POOR: \[threshold1, threshold2)"
- "MODERATE: \[threshold2, threshold3)"
- "GOOD: \[threshold3, threshold4)"
- "EXCELLENT: \[threshold4, -44\]"

This key is considered invalid if the format is violated. If the key is invalid or not configured, a default value set will apply.

 Value: "ntn_5g_nr_ssrsrp_thresholds_int_array"

### KEY_NTN_5G_NR_SSRSRQ_THRESHOLDS_INT_ARRAY

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_NTN_5G_NR_SSRSRQ_THRESHOLDS_INT_ARRAY: String
```

This threshold is used when connected to a non-terrestrial NR network. List of 4 customized 5G SS reference signal received quality (SSRSRQ) thresholds.

Reference: 3GPP TS 38.215; 3GPP TS 38.133 section 10

4 threshold integers must be within the boundaries \[-43 dB, 20 dB\], and the levels are:

- "NONE: \[-43, threshold1)"
- "POOR: \[threshold1, threshold2)"
- "MODERATE: \[threshold2, threshold3)"
- "GOOD: \[threshold3, threshold4)"
- "EXCELLENT: \[threshold4, 20\]"

This key is considered invalid if the format is violated. If the key is invalid or not configured, a default value set will apply.

 Value: "ntn_5g_nr_ssrsrq_thresholds_int_array"

### KEY_NTN_5G_NR_SSSINR_THRESHOLDS_INT_ARRAY

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_NTN_5G_NR_SSSINR_THRESHOLDS_INT_ARRAY: String
```

This threshold is used when connected to a non-terrestrial NR network. List of 4 customized 5G SS signal-to-noise and interference ratio (SSSINR) thresholds.

Reference: 3GPP TS 38.215, 3GPP TS 38.133 10.1.16.1

4 threshold integers must be within the boundaries \[-23 dB, 40 dB\], and the levels are:

- "NONE: \[-23, threshold1)"
- "POOR: \[threshold1, threshold2)"
- "MODERATE: \[threshold2, threshold3)"
- "GOOD: \[threshold3, threshold4)"
- "EXCELLENT: \[threshold4, 40\]"

This key is considered invalid if the format is violated. If the key is invalid or not configured, a default value set will apply.

 Value: "ntn_5g_nr_sssinr_thresholds_int_array"

### KEY_NTN_EUTRAN_RSRP_HYSTERESIS_DB_INT

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_NTN_EUTRAN_RSRP_HYSTERESIS_DB_INT: String
```

An interval in dB for E-UTRAN reference signal received power (RSRP) measurement type defining the required magnitude change between reports when connected to a non-terrestrial LTE network.

The default value is 2 and the minimum allowed value is 0. If no value or negative value is set, the default value 2 is used.

 Value: "ntn_eutran_rsrp_hysteresis_db_int"

### KEY_NTN_EUTRAN_RSRQ_HYSTERESIS_DB_INT

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_NTN_EUTRAN_RSRQ_HYSTERESIS_DB_INT: String
```

An interval in dB for E-UTRAN reference signal received quality (RSRQ) measurement type defining the required magnitude change between reports when connected to a non-terrestrial LTE network.

The default value is 2 and the minimum allowed value is 0. If no value or negative value is set, the default value 2 is used.

 Value: "ntn_eutran_rsrq_hysteresis_db_int"

### KEY_NTN_EUTRAN_RSSNR_HYSTERESIS_DB_INT

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_NTN_EUTRAN_RSSNR_HYSTERESIS_DB_INT: String
```

An interval in dB for E-UTRAN reference signal to noise and interference ratio (RSSNR) measurement type defining the required magnitude change between reports when connected to a non-terrestrial LTE network.

The default value is 2 and the minimum allowed value is 0. If no value or negative value is set, the default value 2 is used.

 Value: "ntn_eutran_rssnr_hysteresis_db_int"

### KEY_NTN_EUTRAN_SIGNAL_REPORTING_HYSTERESIS_MS_INT

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_NTN_EUTRAN_SIGNAL_REPORTING_HYSTERESIS_MS_INT: String
```

An interval in milliseconds for E-UTRAN signal reporting measurement type defining the required time change between reports when connected to a non-terrestrial LTE network.

The default value is 5000 and the minimum allowed value is 0. If no value or negative value is set, the default value 5000 is used.

 Value: "ntn_eutran_signal_reporting_hysteresis_ms_int"

### KEY_NTN_LTE_RSRP_THRESHOLDS_INT_ARRAY

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_NTN_LTE_RSRP_THRESHOLDS_INT_ARRAY: String
```

This threshold is used when connected to a non-terrestrial LTE network. A list of 4 NTN LTE RSRP thresholds above which a signal level is considered POOR, MODERATE, GOOD, or EXCELLENT, to be used in SignalStrength reporting. Note that the min and max thresholds are fixed at -140 and -44, as explained in TS 136.133 9.1.4 - RSRP Measurement Report Mapping.

See SignalStrength#MAX_LTE_RSRP and SignalStrength#MIN_LTE_RSRP. Any signal level outside these boundaries is considered invalid.

 Value: "ntn_lte_rsrp_thresholds_int_array"

### KEY_NTN_LTE_RSRQ_THRESHOLDS_INT_ARRAY

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_NTN_LTE_RSRQ_THRESHOLDS_INT_ARRAY: String
```

This threshold is used when connected to a non-terrestrial LTE network. A list of 4 customized NTN LTE Reference Signal Received Quality (RSRQ) thresholds. Reference: TS 136.133 v12.6.0 section 9.1.7 - RSRQ Measurement Report Mapping. 4 threshold integers must be within the boundaries \[-34 dB, 3 dB\], and the levels are: "NONE: \[-34, threshold1)" "POOR: \[threshold1, threshold2)" "MODERATE: \[threshold2, threshold3)" "GOOD: \[threshold3, threshold4)" "EXCELLENT: \[threshold4, 3\]" This key is considered invalid if the format is violated. If the key is invalid or not configured, a default value set will apply.

 Value: "ntn_lte_rsrq_thresholds_int_array"

### KEY_NTN_LTE_RSSNR_THRESHOLDS_INT_ARRAY

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_NTN_LTE_RSSNR_THRESHOLDS_INT_ARRAY: String
```

This threshold is used when connected to a non-terrestrial LTE network. A list of 4 customized NTN LTE Reference Signal Signal to Noise Ratio (RSSNR) thresholds. 4 threshold integers must be within the boundaries \[-20 dB, 30 dB\], and the levels are: "NONE: \[-20, threshold1)" "POOR: \[threshold1, threshold2)" "MODERATE: \[threshold2, threshold3)" "GOOD: \[threshold3, threshold4)" "EXCELLENT: \[threshold4, 30\]" This key is considered invalid if the format is violated. If the key is invalid or not configured, a default value set will apply.

 Value: "ntn_lte_rssnr_thresholds_int_array"

### KEY_NTN_NGRAN_SIGNAL_REPORTING_HYSTERESIS_MS_INT

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_NTN_NGRAN_SIGNAL_REPORTING_HYSTERESIS_MS_INT: String
```

An interval in milliseconds for NG-RAN signal reporting measurement type defining the required time change between reports when connected to a non-terrestrial NR network.

The default value is 5000 and the minimum allowed value is 0. If no value or negative value is set, the default value 5000 is used.

 Value: "ntn_ngran_signal_reporting_hysteresis_ms_int"

### KEY_NTN_NGRAN_SSRSRP_HYSTERESIS_DB_INT

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_NTN_NGRAN_SSRSRP_HYSTERESIS_DB_INT: String
```

An interval in dB for NG-RAN reference signal received power (SSRSRP) measurement type defining the required magnitude change between reports when connected to a non-terrestrial NR network.

The default value is 2 and the minimum allowed value is 0. If no value or negative value is set, the default value 2 is used.

 Value: "ntn_ngran_ssrsrp_hysteresis_db_int"

### KEY_NTN_NGRAN_SSRSRQ_HYSTERESIS_DB_INT

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_NTN_NGRAN_SSRSRQ_HYSTERESIS_DB_INT: String
```

An interval in dB for NG-RAN reference signal received quality (SSRSRQ) measurement type defining the required magnitude change between reports when connected to a non-terrestrial NR network.

The default value is 2 and the minimum allowed value is 0. If no value or negative value is set, the default value 2 is used.

 Value: "ntn_ngran_ssrsrq_hysteresis_db_int"

### KEY_NTN_NGRAN_SSSINR_HYSTERESIS_DB_INT

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_NTN_NGRAN_SSSINR_HYSTERESIS_DB_INT: String
```

An interval in dB for NG-RAN reference signal to noise and interference ratio (SSSINR) measurement type defining the required magnitude change between reports when connected to a non-terrestrial NR network.

The default value is 2 and the minimum allowed value is 0. If no value or negative value is set, the default value 2 is used.

 Value: "ntn_ngran_sssinr_hysteresis_db_int"

### KEY_ONLY_AUTO_SELECT_IN_HOME_NETWORK_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ONLY_AUTO_SELECT_IN_HOME_NETWORK_BOOL: String
```

Only allow auto selection in Advanced Network Settings when in home network. Manual selection is allowed when in roaming network.

 Value: "only_auto_select_in_home_network"

### KEY_ONLY_SINGLE_DC_ALLOWED_INT_ARRAY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ONLY_SINGLE_DC_ALLOWED_INT_ARRAY: String
```

List of network type constants which support only a single data connection at a time. Some carriers do not support multiple PDP on UMTS.

 Value: "only_single_dc_allowed_int_array"

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager`
- `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_ONLY_SINGLE_DC_ALLOWED_INT_ARRAY:kotlin.String`

### KEY_OPERATOR_SELECTION_EXPAND_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_OPERATOR_SELECTION_EXPAND_BOOL: String
```

Control whether users can choose a network operator.

 Value: "operator_selection_expand_bool"

### KEY_OPPORTUNISTIC_NETWORK_BACKOFF_TIME_LONG

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_OPPORTUNISTIC_NETWORK_BACKOFF_TIME_LONG: String
```

Controls back off time in milli seconds for switching back to opportunistic subscription. This time will be added to `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_OPPORTUNISTIC_NETWORK_DATA_SWITCH_HYSTERESIS_TIME_LONG:kotlin.String` to determine hysteresis time if there is ping pong situation (determined by system app or 1st party app) between primary and opportunistic subscription. Ping ping situation is defined in #KEY_OPPORTUNISTIC_NETWORK_PING_PONG_TIME_LONG. If ping pong situation continuous #KEY_OPPORTUNISTIC_NETWORK_BACKOFF_TIME_LONG will be added to previously determined hysteresis time.

 Value: "opportunistic_network_backoff_time_long"

### KEY_OPPORTUNISTIC_NETWORK_DATA_SWITCH_EXIT_HYSTERESIS_TIME_LONG

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_OPPORTUNISTIC_NETWORK_DATA_SWITCH_EXIT_HYSTERESIS_TIME_LONG: String
```

Controls hysteresis time in milli seconds for which OpportunisticNetworkService will wait before switching data from opportunistic network to primary network.

 Value: "opportunistic_network_data_switch_exit_hysteresis_time_long"

### KEY_OPPORTUNISTIC_NETWORK_DATA_SWITCH_HYSTERESIS_TIME_LONG

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_OPPORTUNISTIC_NETWORK_DATA_SWITCH_HYSTERESIS_TIME_LONG: String
```

Controls hysteresis time in milli seconds for which OpportunisticNetworkService will wait before switching data to an opportunistic network.

 Value: "opportunistic_network_data_switch_hysteresis_time_long"

### KEY_OPPORTUNISTIC_NETWORK_ENTRY_OR_EXIT_HYSTERESIS_TIME_LONG

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_OPPORTUNISTIC_NETWORK_ENTRY_OR_EXIT_HYSTERESIS_TIME_LONG: String
```

Controls hysteresis time in milli seconds for which OpportunisticNetworkService will wait before attaching to a network.

 Value: "opportunistic_network_entry_or_exit_hysteresis_time_long"

### KEY_OPPORTUNISTIC_NETWORK_ENTRY_THRESHOLD_BANDWIDTH_INT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_OPPORTUNISTIC_NETWORK_ENTRY_THRESHOLD_BANDWIDTH_INT: String
```

Controls bandwidth threshold in Kbps at which OpportunisticNetworkService will decide whether the opportunistic network is good enough for internet data.

 Value: "opportunistic_network_entry_threshold_bandwidth_int"

### KEY_OPPORTUNISTIC_NETWORK_ENTRY_THRESHOLD_RSRP_INT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_OPPORTUNISTIC_NETWORK_ENTRY_THRESHOLD_RSRP_INT: String
```

Controls RSRP threshold, in dBm, at which OpportunisticNetworkService will decide whether the opportunistic network is good enough for internet data.

The value of `https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthLte#getRsrp()` will be compared with this threshold.

 Value: "opportunistic_network_entry_threshold_rsrp_int"

### KEY_OPPORTUNISTIC_NETWORK_ENTRY_THRESHOLD_RSSNR_INT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_OPPORTUNISTIC_NETWORK_ENTRY_THRESHOLD_RSSNR_INT: String
```

Controls RSSNR threshold, in dB, at which OpportunisticNetworkService will decide whether the opportunistic network is good enough for internet data.

The value of `https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthLte#getRssnr()` will be compared with this threshold.

 Value: "opportunistic_network_entry_threshold_rssnr_int"

### KEY_OPPORTUNISTIC_NETWORK_EXIT_THRESHOLD_RSRP_INT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_OPPORTUNISTIC_NETWORK_EXIT_THRESHOLD_RSRP_INT: String
```

Controls RSRP threshold, in dBm, below which OpportunisticNetworkService will decide whether the opportunistic network available is not good enough for internet data.

The value of `https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthLte#getRsrp()` will be compared with this threshold.

 Value: "opportunistic_network_exit_threshold_rsrp_int"

### KEY_OPPORTUNISTIC_NETWORK_EXIT_THRESHOLD_RSSNR_INT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_OPPORTUNISTIC_NETWORK_EXIT_THRESHOLD_RSSNR_INT: String
```

Controls RSSNR threshold, in dB, below which OpportunisticNetworkService will decide whether the opportunistic network available is not good enough for internet data.

The value of `https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthLte#getRssnr()` will be compared with this threshold.

 Value: "opportunistic_network_exit_threshold_rssnr_int"

### KEY_OPPORTUNISTIC_NETWORK_MAX_BACKOFF_TIME_LONG

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_OPPORTUNISTIC_NETWORK_MAX_BACKOFF_TIME_LONG: String
```

Controls the max back off time in milli seconds for switching back to opportunistic subscription. This time will be the max hysteresis that can be determined irrespective of there is continuous ping pong situation or not as described in #KEY_OPPORTUNISTIC_NETWORK_PING_PONG_TIME_LONG and #KEY_OPPORTUNISTIC_NETWORK_BACKOFF_TIME_LONG.

 Value: "opportunistic_network_max_backoff_time_long"

### KEY_OPPORTUNISTIC_NETWORK_PING_PONG_TIME_LONG

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_OPPORTUNISTIC_NETWORK_PING_PONG_TIME_LONG: String
```

Controls the ping pong determination of opportunistic network. If opportunistic network is determined as out of service or below #KEY_OPPORTUNISTIC_NETWORK_EXIT_THRESHOLD_RSRP_INT or #KEY_OPPORTUNISTIC_NETWORK_EXIT_THRESHOLD_RSSNR_INT within #KEY_OPPORTUNISTIC_NETWORK_PING_PONG_TIME_LONG of switching to opportunistic network, it will be determined as ping pong situation by system app or 1st party app.

 Value: "opportunistic_network_ping_pong_time_long"

### KEY_OPP_AUTO_DATA_SWITCH_POLICY_INT

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_OPP_AUTO_DATA_SWITCH_POLICY_INT: String
```

Auto data network switch policies between primary and opportunistic profiles in the same subscription group.

The default value is `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#OPP_AUTO_DATA_SWITCH_POLICY_DISABLED:kotlin.Int`, that is, auto data switch between primary and opportunistic networks is disabled.

Carriers can override the value for the primary subscription with `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#OPP_AUTO_DATA_SWITCH_POLICY_FOLLOW_SYSTEM:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#OPP_AUTO_DATA_SWITCH_POLICY_FOR_AVAILABILITY:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#OPP_AUTO_DATA_SWITCH_POLICY_FOR_PERFORMANCE:kotlin.Int` to enable all system supported policies or specific policy according to the business user cases.

None of the policies here impact the auto data switch between primary networks.

 Value: "opp_auto_data_switch_policy_int"

### KEY_OVERRIDE_WFC_ROAMING_MODE_WHILE_USING_NTN_BOOL

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_OVERRIDE_WFC_ROAMING_MODE_WHILE_USING_NTN_BOOL: String
```

Determine whether to override roaming Wi-Fi Calling preference when device is connected to non-terrestrial network. `true` - roaming preference cannot be changed by user independently. Roaming preference is overridden to `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#` `false` - roaming preference can be changed by user independently and is not overridden when device is connected to non-terrestrial network.

 Value: "override_wfc_roaming_mode_while_using_ntn_bool"

### KEY_PARAMETERS_USED_FOR_NTN_LTE_SIGNAL_BAR_INT

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_PARAMETERS_USED_FOR_NTN_LTE_SIGNAL_BAR_INT: String
```

This threshold is used when connected to a non-terrestrial LTE network. Bit-field integer to determine whether to use Reference Signal Received Power (RSRP), Reference Signal Received Quality (RSRQ), or/and Reference Signal Signal to Noise Ratio (RSSNR) for the number of NTN LTE signal bars and signal criteria reporting enabling.

If a measure is not set, signal criteria reporting from modem will not be triggered and not be used for calculating signal level. If multiple measures are set bit, the parameter whose value is smallest is used to indicate the signal level.

- RSRP = 1 \<\< 0
- RSRQ = 1 \<\< 1
- RSSNR = 1 \<\< 2

The value of this key must be bitwise OR of CellSignalStrengthLte#USE_RSRP, CellSignalStrengthLte#USE_RSRQ, CellSignalStrengthLte#USE_RSSNR.

For example, if both RSRP and RSRQ are used, the value of key is 3 (1 \<\< 0 | 1 \<\< 1). If the key is invalid or not configured, a default value (RSRP = 1 \<\< 0) will apply.
| --- | --- |

 Value: "parameters_used_for_ntn_lte_signal_bar_int"

### KEY_PING_TEST_BEFORE_DATA_SWITCH_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_PING_TEST_BEFORE_DATA_SWITCH_BOOL: String
```

Controls whether to do ping test before switching data to opportunistic network. This carrier config is used to disable this feature.

 Value: "ping_test_before_data_switch_bool"

### KEY_PREFER_2G_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_PREFER_2G_BOOL: String
```

Used in the Preferred Network Types menu to determine if the 2G option is displayed. Value defaults to false as of Android T to discourage the use of insecure 2G protocols.

 Value: "prefer_2g_bool"

### KEY_PREFER_3G_VISIBILITY_BOOL

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_PREFER_3G_VISIBILITY_BOOL: String
```

Used in the Preferred Network Types menu to determine if the 3G option is displayed.

 Value: "prefer_3g_visibility_bool"

### KEY_PREMIUM_CAPABILITY_MAXIMUM_DAILY_NOTIFICATION_COUNT_INT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_PREMIUM_CAPABILITY_MAXIMUM_DAILY_NOTIFICATION_COUNT_INT: String
```

The maximum number of times in a day that we display the notification for a performance boost via premium capabilities when `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#purchasePremiumCapability(kotlin.Int,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` returns a failure due to user action or timeout. The default value is 2 times.

 Value: "premium_capability_maximum_daily_notification_count_int"

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_USER_CANCELED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_TIMEOUT:kotlin.Int`

### KEY_PREMIUM_CAPABILITY_MAXIMUM_MONTHLY_NOTIFICATION_COUNT_INT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_PREMIUM_CAPABILITY_MAXIMUM_MONTHLY_NOTIFICATION_COUNT_INT: String
```

The maximum number of times in a month that we display the notification for a performance boost via premium capabilities when `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#purchasePremiumCapability(kotlin.Int,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` returns a failure due to user action or timeout. The default value is 10 times.

 Value: "premium_capability_maximum_monthly_notification_count_int"

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_USER_CANCELED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_TIMEOUT:kotlin.Int`

### KEY_PREMIUM_CAPABILITY_NETWORK_SETUP_TIME_MILLIS_LONG

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_PREMIUM_CAPABILITY_NETWORK_SETUP_TIME_MILLIS_LONG: String
```

The amount of time in milliseconds within which the network must set up a slicing configuration for the premium capability after `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#purchasePremiumCapability(kotlin.Int,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` returns `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_SUCCESS:kotlin.Int`. During the setup time, calls to `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#purchasePremiumCapability(kotlin.Int,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` will return `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_PENDING_NETWORK_SETUP:kotlin.Int`. If the network fails to set up a slicing configuration for the premium capability within the setup time, subsequent purchase requests will be allowed to go through again. The default value is 5 minutes.

 Value: "premium_capability_network_setup_time_millis_long"

### KEY_PREMIUM_CAPABILITY_NOTIFICATION_BACKOFF_HYSTERESIS_TIME_MILLIS_LONG

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_PREMIUM_CAPABILITY_NOTIFICATION_BACKOFF_HYSTERESIS_TIME_MILLIS_LONG: String
```

The amount of time in milliseconds that the notification for a performance boost via premium capabilities should be blocked when `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#purchasePremiumCapability(kotlin.Int,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` returns a failure due to user action or timeout. The maximum number of performance boost notifications to show the user are defined in `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_PREMIUM_CAPABILITY_MAXIMUM_DAILY_NOTIFICATION_COUNT_INT:kotlin.String` and `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_PREMIUM_CAPABILITY_MAXIMUM_MONTHLY_NOTIFICATION_COUNT_INT:kotlin.String`. The default value is 30 minutes.

 Value: "premium_capability_notification_backoff_hysteresis_time_millis_long"

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_USER_CANCELED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_TIMEOUT:kotlin.Int`

### KEY_PREMIUM_CAPABILITY_NOTIFICATION_DISPLAY_TIMEOUT_MILLIS_LONG

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_PREMIUM_CAPABILITY_NOTIFICATION_DISPLAY_TIMEOUT_MILLIS_LONG: String
```

The amount of time in milliseconds the notification for a performance boost via premium capabilities will be visible to the user after `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#purchasePremiumCapability(kotlin.Int,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` requests user action to purchase the boost from the carrier. Once the timeout expires, the performance boost notification will be automatically dismissed and the request will fail with `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_TIMEOUT:kotlin.Int`. The default value is 30 minutes.

 Value: "premium_capability_notification_display_timeout_millis_long"

### KEY_PREMIUM_CAPABILITY_PURCHASE_CONDITION_BACKOFF_HYSTERESIS_TIME_MILLIS_LONG

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_PREMIUM_CAPABILITY_PURCHASE_CONDITION_BACKOFF_HYSTERESIS_TIME_MILLIS_LONG: String
```

The amount of time in milliseconds that the purchase request should be throttled when `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#purchasePremiumCapability(kotlin.Int,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` returns a failure due to the carrier. The default value is 30 minutes.

 Value: "premium_capability_purchase_condition_backoff_hysteresis_time_millis_long"

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_CARRIER_ERROR:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_ENTITLEMENT_CHECK_FAILED:kotlin.Int`

### KEY_PREMIUM_CAPABILITY_PURCHASE_URL_STRING

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_PREMIUM_CAPABILITY_PURCHASE_URL_STRING: String
```

The URL to redirect to when the user clicks on the notification for a performance boost via premium capabilities after applications call `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#purchasePremiumCapability(kotlin.Int,%20java.util.concurrent.Executor,%20java.util.function.Consumer)`. If the URL is empty or invalid, the purchase request will return `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_FEATURE_NOT_SUPPORTED:kotlin.Int`. This is empty by default.

 Value: "premium_capability_purchase_url_string"

### KEY_PREMIUM_CAPABILITY_SUPPORTED_ON_LTE_BOOL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_PREMIUM_CAPABILITY_SUPPORTED_ON_LTE_BOOL: String
```

Whether to allow premium capabilities to be purchased when the device is connected to LTE. If this is `true`, applications can call `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#purchasePremiumCapability(kotlin.Int,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` when connected to `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_LTE:kotlin.Int` to purchase and use premium capabilities. If this is `false`, applications can only purchase and use premium capabilities when connected to `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_NR:kotlin.Int`. This is `false` by default.

 Value: "premium_capability_supported_on_lte_bool"

### KEY_PREVENT_CLIR_ACTIVATION_AND_DEACTIVATION_CODE_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_PREVENT_CLIR_ACTIVATION_AND_DEACTIVATION_CODE_BOOL: String
```

Flag specifying whether to prevent sending CLIR activation("\*31#") and deactivation("#31#") code only without dialing number. When `true`, these are prevented, `false` otherwise.

 Value: "prevent_clir_activation_and_deactivation_code_bool"

### KEY_RADIO_RESTART_FAILURE_CAUSES_INT_ARRAY

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_RADIO_RESTART_FAILURE_CAUSES_INT_ARRAY: String
```

A list of failure cause codes that will trigger a modem restart when telephony receiving one of those during data setup. The cause codes are defined in 3GPP TS 24.008 Annex I and TS 24.301 Annex B.

 Value: "radio_restart_failure_causes_int_array"

### KEY_RATCHET_NR_ADVANCED_BANDWIDTH_IF_RRC_IDLE_BOOL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_RATCHET_NR_ADVANCED_BANDWIDTH_IF_RRC_IDLE_BOOL: String
```

Indicating whether to ratchet the aggregated cell bandwidths on receiving new values when the device is in RRC IDLE mode. The aggregated cell bandwidths are used for determining NR advanced state. If this is `true`, we will only update the aggregate cell bandwidths if the new aggregate is higher than the current aggregate and the anchor NR cell is the same. If this is `false`, we will always update the aggregate cell bandwidths when receiving new values.

 Value: "ratchet_nr_advanced_bandwidth_if_rrc_idle_bool"

### KEY_RCS_CONFIG_SERVER_URL_STRING

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_RCS_CONFIG_SERVER_URL_STRING: String
```

The RCS configuration server URL. This URL is used to initiate RCS provisioning.

 Value: "rcs_config_server_url_string"

### KEY_READ_ONLY_APN_FIELDS_STRING_ARRAY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_READ_ONLY_APN_FIELDS_STRING_ARRAY: String
```

APN fields that user is not allowed to modify.

 Value: "read_only_apn_fields_string_array"

### KEY_READ_ONLY_APN_TYPES_STRING_ARRAY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_READ_ONLY_APN_TYPES_STRING_ARRAY: String
```

APN types that user is not allowed to modify.

 Value: "read_only_apn_types_string_array"

### KEY_REGIONAL_SATELLITE_EARFCN_BUNDLE

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_REGIONAL_SATELLITE_EARFCN_BUNDLE: String
```

A PersistableBundle that contains a list of key-value pairs, where the values are integer arrays.

Keys are the IDs of regional satellite configs as strings and values are integer arrays of earfcns in the corresponding regions. An example config for two regions "1" and "2":

```kotlin
<code>&lt;carrier_config&gt;
    &lt;pbundle_as_map name="regional_satellite_earfcn_bundle"&gt;
      &lt;int-array name = "1" num = "2"&gt;
        &lt;item value = "100"/&gt;
        &lt;item value = "200"/&gt;
      &lt;/int-array&gt;
      &lt;int-array name = "2" num = "1"&gt;
        &lt;item value = "200"/&gt;
      &lt;/int-array&gt;
    &lt;/pbundle_as_map&gt;
  &lt;/carrier_config&gt;
  </code>
```

This config is empty by default.

 Value: "regional_satellite_earfcn_bundle"

### KEY_REMOVE_SATELLITE_PLMN_IN_MANUAL_NETWORK_SCAN_BOOL

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_REMOVE_SATELLITE_PLMN_IN_MANUAL_NETWORK_SCAN_BOOL: String
```

Indicating whether plmns associated with carrier satellite can be exposed to user when manually scanning available cellular network. If key is `true`, satellite plmn should not be exposed to user and should be automatically set, `false` otherwise. Default value is `true`.

 Value: "remove_satellite_plmn_in_manual_network_scan_bool"

### KEY_REQUIRE_ENTITLEMENT_CHECKS_BOOL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_REQUIRE_ENTITLEMENT_CHECKS_BOOL: String
```

Flag to require or skip entitlement checks. If true, entitlement checks will be executed if device has been configured for it, If false, entitlement checks will be skipped.

 Value: "require_entitlement_checks_bool"

### KEY_RESTART_RADIO_ON_PDP_FAIL_REGULAR_DEACTIVATION_BOOL

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_RESTART_RADIO_ON_PDP_FAIL_REGULAR_DEACTIVATION_BOOL: String
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_RADIO_RESTART_FAILURE_CAUSES_INT_ARRAY:kotlin.String` instead*

Flag indicating whether radio is to be restarted on error PDP_FAIL_REGULAR_DEACTIVATION This is false by default.

 Value: "restart_radio_on_pdp_fail_regular_deactivation_bool"

### KEY_RTT_AUTO_UPGRADE_BOOL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_RTT_AUTO_UPGRADE_BOOL: String
```

Indicates if the carrier supports auto-upgrading a call to RTT when receiving a call from a RTT-supported device.

 Value: "rtt_auto_upgrade_bool"

### KEY_RTT_DOWNGRADE_SUPPORTED_BOOL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_RTT_DOWNGRADE_SUPPORTED_BOOL: String
```

Indicates if the carrier supports downgrading a RTT call to a voice call during the call.

 Value: "rtt_downgrade_supported_bool"

### KEY_RTT_SUPPORTED_BOOL

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_RTT_SUPPORTED_BOOL: String
```

Flag indicating whether the carrier supports RTT over IMS.

 Value: "rtt_supported_bool"

### KEY_RTT_SUPPORTED_FOR_VT_BOOL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_RTT_SUPPORTED_FOR_VT_BOOL: String
```

Indicates if the carrier supports RTT during a video call.

 Value: "rtt_supported_for_vt_bool"

### KEY_RTT_SUPPORTED_WHILE_ROAMING_BOOL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_RTT_SUPPORTED_WHILE_ROAMING_BOOL: String
```

Indicates whether RTT is supported while roaming.

 Value: "rtt_supported_while_roaming_bool"

### KEY_RTT_UPGRADE_SUPPORTED_BOOL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_RTT_UPGRADE_SUPPORTED_BOOL: String
```

Indicates if the carrier supports upgrading a voice call to an RTT call during the call.

 Value: "rtt_upgrade_supported_bool"

### KEY_RTT_UPGRADE_SUPPORTED_FOR_DOWNGRADED_VT_CALL_BOOL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_RTT_UPGRADE_SUPPORTED_FOR_DOWNGRADED_VT_CALL_BOOL: String
```

Indicates if the carrier supports upgrading a call that was previously a VT call to RTT.

 Value: "rtt_upgrade_supported_for_downgraded_vt_call"

### KEY_SATELLITE_ATTACH_SUPPORTED_BOOL

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SATELLITE_ATTACH_SUPPORTED_BOOL: String
```

This config enables modem to scan satellite PLMNs specified as per `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_SUPPORTED_SATELLITE_SERVICES_PER_PROVIDER_BUNDLE:kotlin.String` and attach to same in case cellular networks are not enabled. This will need specific agreement between satellite provider and the carrier before enabling this flag. The default value is false.

 Value: "satellite_attach_supported_bool"

### KEY_SATELLITE_CONFIGS_PER_PLMN_BUNDLE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SATELLITE_CONFIGS_PER_PLMN_BUNDLE: String
```

A PersistableBundle that contains a list of key-value pairs, where keys are satellite provider PLMNs and values are bundles containing satellite configurations for that PLMN. This allows for per-provider settings within a single carrier, which is necessary for hybrid scenarios where a carrier supports multiple satellite networks with different capabilities (e.g., AST and Skylo).

The keys in this bundle are PLMNs of satellite providers as strings. The values are PersistableBundles containing some of the **existing** satellite configurations for that PLMN.

The **allowed** satellite configuration keys that the PersistableBundle values can have are:

- `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_ROAMING_NTN_EMERGENCY_CALL_TO_SATELLITE_HANDOVER_TYPE_INT:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_ROAMING_NTN_CONNECT_TYPE_INT:kotlin.String`
- KEY_SATELLITE_TECHNOLOGY_INT_ARRAY
- KEY_SATELLITE_SUPPORTED_FREQUENCIES_INT_ARRAY

An example config for a hybrid carrier supporting two PLMNs (lets say "XXXXXX" is the PLMN of AST and "YYYYYY" is the PLMN of Skylo):

```kotlin
<code>&lt;pbundle_as_map name="satellite_configs_per_plmn_bundle"&gt;
      &lt;!-- AST PLMN's satellite configurations --&gt;
      &lt;pbundle_as_map name="XXXXXX"&gt;
          &lt;!-- SatelliteManager#EMERGENCY_CALL_TO_SATELLITE_HANDOVER_TYPE_T911 --&gt;
          &lt;int name="carrier_roaming_ntn_emergency_call_to_satellite_handover_type_int"
               value="2" /&gt;
          &lt;!-- CarrierConfigManager#CARRIER_ROAMING_NTN_CONNECT_AUTOMATIC --&gt;
          &lt;int name="carrier_roaming_ntn_connect_type_int" value="0" /&gt;
          &lt;!-- SatelliteManager#NT_RADIO_TECHNOLOGY_NR_NTN --&gt;
          &lt;int-array name="satellite_technology_type_int_array" num="1"&gt;
              &lt;item value="2" /&gt;
          &lt;/int-array&gt;
          &lt;!-- CarrierConfigManager#KEY_SATELLITE_SUPPORTED_FREQUENCIES_INT_ARRAY --&gt;
          &lt;int-array name="satellite_supported_frequencies_int_array" num="2"&gt;
              &lt;item value="229015" /&gt;
              &lt;item value="229016" /&gt;
          &lt;/int-array&gt;
      &lt;/pbundle_as_map&gt;
      &lt;!-- Skylo PLMN's satellite configurations --&gt;
      &lt;pbundle_as_map name="YYYYYY"&gt;
          &lt;!-- SatelliteManager#EMERGENCY_CALL_TO_SATELLITE_HANDOVER_TYPE_SOS --&gt;
          &lt;int name="carrier_roaming_ntn_emergency_call_to_satellite_handover_type_int"
               value="1" /&gt;
          &lt;!-- CarrierConfigManager#CARRIER_ROAMING_NTN_CONNECT_MANUAL --&gt;
          &lt;int name="carrier_roaming_ntn_connect_type_int" value="1" /&gt;
          &lt;!-- SatelliteManager#NT_RADIO_TECHNOLOGY_NB_IOT_NTN --&gt;
          &lt;int-array name="satellite_technology_type_int_array" num="1"&gt;
              &lt;item value="1" /&gt;
          &lt;/int-array&gt;
      &lt;/pbundle_as_map&gt;
  &lt;/pbundle_as_map&gt;
  </code>
```

When set, this PLMN config would take precedence over the global configs. For example, if the global handover type is set as `https://developer.android.com/reference/kotlin/android/telephony/satellite/SatelliteManager`, but if this config's current PLMN handover type is set as android.telephony.satellite.SatelliteManager#EMERGENCY_CALL_TO_SATELLITE_HANDOVER_TYPE_T911, then T911 would be effective way of handling emergency call.

This config is empty by default.

 Value: "satellite_configs_per_plmn_bundle"

### KEY_SATELLITE_CONNECTED_NOTIFICATION_THROTTLE_MILLIS_INT

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SATELLITE_CONNECTED_NOTIFICATION_THROTTLE_MILLIS_INT: String
```

Satellite notification display restriction reset time in seconds. The device shows a notification when it connects to a satellite. If the user interacts with the notification, it won't be shown again immediately. Instead, the notification will only reappear after below key mentioned amount of time has passed.

 Value: "satellite_connected_notification_throttle_millis_int"

### KEY_SATELLITE_CONNECTION_HYSTERESIS_SEC_INT

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SATELLITE_CONNECTION_HYSTERESIS_SEC_INT: String
```

The carrier-enabled satellite connection hysteresis time in seconds for which the device continues in satellite mode after it loses the connection with the satellite network.

If the device is in satellite mode, the following actions will be taken by the device:

- System UI will continue showing the satellite icon.
- When there is an ongoing emergency call, and the IMS is not registered, and cellular service is not available, and the device is in satellite mode, a timer with a duration defined by the overlay config `config_emergency_call_wait_for_connection_timeout_millis` will be started. When the timer expires, Telephony will send the event `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EVENT_DISPLAY_EMERGENCY_MESSAGE:kotlin.String` to Dialer, which will then prompt users to switch to using satellite emergency messaging.

The default value is 180 seconds.

 Value: "satellite_connection_hysteresis_sec_int"

### KEY_SATELLITE_DATA_SUPPORT_MODE_INT

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SATELLITE_DATA_SUPPORT_MODE_INT: String
```

Indicates what kind of traffic an `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities.html#NET_CAPABILITY_NOT_RESTRICTED:kotlin.Int` satellite network can possibly support. The network may be subject to further restrictions (or upgrades such as bandwidth level) based on entitlement etc. If no data is allowed on satellite network, exclude android.telephony.data.ApnSetting#INFRASTRUCTURE_SATELLITE from APN infrastructure_bitmask, and this configuration is ignored. By default it only supports restricted data.

 Value: "satellite_data_support_mode_int"

### KEY_SATELLITE_DISPLAY_NAME_STRING

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SATELLITE_DISPLAY_NAME_STRING: String
```

The display name that will be used for satellite functionality within the UI. The default string value is empty string.

 Value: "satellite_display_name_string"

### KEY_SATELLITE_ENTITLEMENT_APP_NAME_STRING

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SATELLITE_ENTITLEMENT_APP_NAME_STRING: String
```

Indicates the appName that is used when querying the entitlement server for satellite. The default value is androidSatmode. Reference: GSMA TS.43-v11, 2.8.5 Fast Authentication and Token Management. \`app_name\` is an optional attribute in the request and may vary depending on the carrier requirement.

 Value: "satellite_entitlement_app_name_string"

### KEY_SATELLITE_ENTITLEMENT_STATUS_REFRESH_DAYS_INT

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SATELLITE_ENTITLEMENT_STATUS_REFRESH_DAYS_INT: String
```

An integer key holds the time interval for refreshing or re-querying the satellite entitlement status from the entitlement server to ensure it is the latest. The default value is 1 day.

 Value: "satellite_entitlement_status_refresh_days_int"

### KEY_SATELLITE_ENTITLEMENT_SUPPORTED_BOOL

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SATELLITE_ENTITLEMENT_SUPPORTED_BOOL: String
```

This configuration enables device to query the entitlement server to get the satellite configuration. This will need agreement the carrier before enabling this flag. The default value is false.

 Value: "satellite_entitlement_supported_bool"

### KEY_SATELLITE_ESOS_SUPPORTED_BOOL

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SATELLITE_ESOS_SUPPORTED_BOOL: String
```

Indicate whether carrier roaming to satellite is using ESOS (Emergency SOS) which connects to an emergency provider instead of PSAP (Public Safety Answering Point) for emergency messaging. This will need agreement with carriers before enabling this flag. The default value is false.

 Value: "satellite_esos_supported_bool"

### KEY_SATELLITE_IGNORE_DATA_ROAMING_SETTING_BOOL

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SATELLITE_IGNORE_DATA_ROAMING_SETTING_BOOL: String
```

Determines whether data roaming off setting should be ignored and satellite data should be allowed even when data roaming is off. If the carrier would like to allow the device to use satellite connection when data roaming is off, this key should be set to `true`. The default value is `true` i.e. allow satellite data when data roaming is off.

 Value: "satellite_ignore_data_roaming_setting_bool"

### KEY_SATELLITE_INFORMATION_REDIRECT_URL_STRING

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SATELLITE_INFORMATION_REDIRECT_URL_STRING: String
```

URL to redirect user to get more information about the carrier support for satellite. The default value is empty string.

 Value: "satellite_information_redirect_url_string"

### KEY_SATELLITE_NIDD_APN_NAME_STRING

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SATELLITE_NIDD_APN_NAME_STRING: String
```

Defines the NIDD (Non-IP Data Delivery) APN to be used for carrier roaming to satellite attachment. For more on NIDD, see 3GPP TS 29.542. Note this config is the only source of truth regarding the definition of the APN.

 Value: "satellite_nidd_apn_name_string"

### KEY_SATELLITE_ROAMING_ESOS_INACTIVITY_TIMEOUT_SEC_INT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SATELLITE_ROAMING_ESOS_INACTIVITY_TIMEOUT_SEC_INT: String
```

An integer key holds the timeout duration in seconds used to determine whether to exit ESOS mode and start TN scanning. The timer is started when the device is not connected, user is not pointing to the satellite and no data transfer is happening. When the timer expires, the device will move to IDLE mode upon which TN scanning will start. The default value is 600 seconds.

 Value: "satellite_roaming_esos_inactivity_timeout_sec_int"

### KEY_SATELLITE_ROAMING_P2P_SMS_INACTIVITY_TIMEOUT_SEC_INT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SATELLITE_ROAMING_P2P_SMS_INACTIVITY_TIMEOUT_SEC_INT: String
```

An integer key holds the timeout duration in seconds used to determine whether to exit P2P SMS mode and start TN scanning. The timer is started when the device is not connected, user is not pointing to the satellite and no data transfer is happening. When the timer expires, the device will move to IDLE mode upon which TN scanning will start. The default value is 180 seconds.

 Value: "satellite_roaming_p2p_sms_inactivity_timeout_sec_int"

### KEY_SATELLITE_ROAMING_P2P_SMS_SUPPORTED_BOOL

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SATELLITE_ROAMING_P2P_SMS_SUPPORTED_BOOL: String
```

Indicate whether carrier roaming to satellite is using P2P SMS. This will need agreement with carriers before enabling this flag. The default value is false.

 Value: "satellite_roaming_p2p_sms_supported_bool"

### KEY_SATELLITE_ROAMING_SCREEN_OFF_INACTIVITY_TIMEOUT_SEC_INT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SATELLITE_ROAMING_SCREEN_OFF_INACTIVITY_TIMEOUT_SEC_INT: String
```

An integer key holds the timeout duration in seconds used to determine whether to exit carrier-roaming NB-IOT satellite mode. The timer is started when the device screen is turned off during a satellite session. When the timer expires, the device exits Carrier Roaming NB IOT NTN. The default value is 30 seconds.

 Value: "satellite_roaming_screen_off_inactivity_timeout_sec_int"

### KEY_SATELLITE_ROAMING_TURN_OFF_SESSION_FOR_EMERGENCY_CALL_BOOL

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SATELLITE_ROAMING_TURN_OFF_SESSION_FOR_EMERGENCY_CALL_BOOL: String
```

Default value `true`, meaning when an emergency call request comes in, if the device is in emergency satellite mode but hasn't sent the first satellite datagram, then exits satellite mode to allow the emergency call to go through. If `false`, the emergency call is always blocked if device is in emergency satellite mode. Note if device is NOT in emergency satellite mode, emergency call is always allowed.

 Value: "satellite_roaming_turn_off_session_for_emergency_call_bool"

### KEY_SATELLITE_SOS_MAX_DATAGRAM_SIZE_BYTES_INT

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SATELLITE_SOS_MAX_DATAGRAM_SIZE_BYTES_INT: String
```

This value is used to set the max datagram size in bytes. If the value is not available then the default value will be used. The default value is 255 bytes.

 Value: "satellite_sos_max_datagram_size_bytes_int"

### KEY_SATELLITE_SUPPORTED_DISASTER_PLMN_STRING_ARRAY

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SATELLITE_SUPPORTED_DISASTER_PLMN_STRING_ARRAY: String
```

A string array containing the list of supported disaster satellite PLMNs. The satellite services supported by these PLMNs are defined by `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_SUPPORTED_SATELLITE_SERVICES_PER_PROVIDER_BUNDLE:kotlin.String`.

This config is empty by default.

 Value: "satellite_supported_disaster_plmn_string_array"

### KEY_SATELLITE_SUPPORTED_EMERGENCY_PLMN_STRING_ARRAY

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SATELLITE_SUPPORTED_EMERGENCY_PLMN_STRING_ARRAY: String
```

A string array containing the list of supported emergency satellite PLMNs. The satellite services supported by these PLMNs are defined by `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_SUPPORTED_SATELLITE_SERVICES_PER_PROVIDER_BUNDLE:kotlin.String`.

This config is empty by default.

 Value: "satellite_supported_emergency_plmn_string_array"

### KEY_SATELLITE_SUPPORTED_MSG_APPS_STRING_ARRAY

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SATELLITE_SUPPORTED_MSG_APPS_STRING_ARRAY: String
```

A string array containing the list of messaging apps that support satellite. The default value contains only "com.google.android.apps.messaging"

 Value: "satellite_supported_msg_apps_string_array"

### KEY_SHOW_4G_FOR_3G_DATA_ICON_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SHOW_4G_FOR_3G_DATA_ICON_BOOL: String
```

Boolean indicating if default data account should show 4G icon when in 3G.

 Value: "show_4g_for_3g_data_icon_bool"

### KEY_SHOW_4G_FOR_LTE_DATA_ICON_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SHOW_4G_FOR_LTE_DATA_ICON_BOOL: String
```

Boolean indicating if default data account should show LTE or 4G icon.

 Value: "show_4g_for_lte_data_icon_bool"

### KEY_SHOW_APN_SETTING_CDMA_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SHOW_APN_SETTING_CDMA_BOOL: String
```

**Deprecated:** *Legacy CDMA is unsupported.*

Show APN Settings for some CDMA carriers

 Value: "show_apn_setting_cdma_bool"

### KEY_SHOW_AVOID_BAD_WIFI_TOGGLE_BOOL

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SHOW_AVOID_BAD_WIFI_TOGGLE_BOOL: String
```

Used to decide if the device's UI should present the "avoid bad Wi-Fi" from carrier config. This method effectively enables or disables the display of the relevant setting toggle. This is only used if KEY_AVOID_BAD_WIFI_BOOL is true. When KEY_AVOID_BAD_WIFI_BOOL is false, the setting is always shown even if this is false.

 Value: "show_avoid_bad_wifi_bool"

### KEY_SHOW_BLOCKING_PAY_PHONE_OPTION_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SHOW_BLOCKING_PAY_PHONE_OPTION_BOOL: String
```

Flag specifying whether to show blocking pay phone option in blocked numbers screen. Only show the option if payphone call presentation is present in the carrier's region.

 Value: "show_blocking_pay_phone_option_bool"

### KEY_SHOW_CALL_BLOCKING_DISABLED_NOTIFICATION_ALWAYS_BOOL

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SHOW_CALL_BLOCKING_DISABLED_NOTIFICATION_ALWAYS_BOOL: String
```

Flag specifying whether to show notification(call blocking disabled) when Enhanced Call Blocking(KEY_SUPPORT_ENHANCED_CALL_BLOCKING_BOOL) is enabled and making emergency call. When true, notification is shown always. When false, notification is shown only when any setting of "Enhanced Blocked number" is enabled.

 Value: "show_call_blocking_disabled_notification_always_bool"

### KEY_SHOW_CDMA_CHOICES_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SHOW_CDMA_CHOICES_BOOL: String
```

**Deprecated:** *Legacy CDMA is unsupported.*

Show cdma network mode choices 1x, 3G, global etc.

 Value: "show_cdma_choices_bool"

### KEY_SHOW_FORWARDED_NUMBER_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SHOW_FORWARDED_NUMBER_BOOL: String
```

Flag specifying whether to show forwarded number on call-in-progress screen. When true, forwarded number is shown. When false, forwarded number is not shown.

 Value: "show_forwarded_number_bool"

### KEY_SHOW_ICCID_IN_SIM_STATUS_BOOL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SHOW_ICCID_IN_SIM_STATUS_BOOL: String
```

Flag specifying whether ICCID is showed in SIM Status screen, default to false.

 Value: "show_iccid_in_sim_status_bool"

### KEY_SHOW_IMS_REGISTRATION_STATUS_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SHOW_IMS_REGISTRATION_STATUS_BOOL: String
```

Flag specifying whether IMS registration state menu is shown in Status Info setting, default to false.

 Value: "show_ims_registration_status_bool"

### KEY_SHOW_ONSCREEN_DIAL_BUTTON_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SHOW_ONSCREEN_DIAL_BUTTON_BOOL: String
```

If true, show an onscreen "Dial" button in the dialer. In practice this is used on all platforms, even the ones with hard SEND/END keys, but for maximum flexibility it's controlled by a flag here (which can be overridden on a per-product basis.)

 Value: "show_onscreen_dial_button_bool"

### KEY_SHOW_ROAMING_INDICATOR_BOOL

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SHOW_ROAMING_INDICATOR_BOOL: String
```

Config to show the roaming indicator (i.e. the "R" icon) from the status bar when roaming. The roaming indicator will be shown if this is `true` and will not be shown if this is `false`.

 Value: "show_roaming_indicator_bool"

### KEY_SHOW_SIGNAL_STRENGTH_IN_SIM_STATUS_BOOL

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SHOW_SIGNAL_STRENGTH_IN_SIM_STATUS_BOOL: String
```

Flag specifying whether the `https://developer.android.com/reference/kotlin/android/telephony/SignalStrength` is shown in the SIM Status screen. The default value is true.

 Value: "show_signal_strength_in_sim_status_bool"

### KEY_SHOW_VIDEO_CALL_CHARGES_ALERT_DIALOG_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SHOW_VIDEO_CALL_CHARGES_ALERT_DIALOG_BOOL: String
```

Flag specifying whether to show an alert dialog for video call charges. By default this value is `false`.

 Value: "show_video_call_charges_alert_dialog_bool"

### KEY_SHOW_WFC_LOCATION_PRIVACY_POLICY_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SHOW_WFC_LOCATION_PRIVACY_POLICY_BOOL: String
```

Determines whether wifi calling location privacy policy is shown.

 Value: "show_wfc_location_privacy_policy_bool"

### KEY_SIMPLIFIED_NETWORK_SETTINGS_BOOL

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SIMPLIFIED_NETWORK_SETTINGS_BOOL: String
```

**Deprecated:** *Never implemented. Has no behavior impact when override. DO NOT USE.*

Control whether users receive a simplified network settings UI and improved network selection.

 Value: "simplified_network_settings_bool"

### KEY_SIM_COUNTRY_ISO_OVERRIDE_STRING

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SIM_COUNTRY_ISO_OVERRIDE_STRING: String
```

String to override sim country iso. Sim country iso is based on sim MCC which is coarse and doesn't work with dual IMSI SIM where a SIM can have multiple MCC from different countries. Instead, each sim carrier should have a single country code, apply per carrier based iso code as an override. The overridden value can be read from `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#getSimCountryIso()` and `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo#getCountryIso()`

 Value: "sim_country_iso_override_string"

### KEY_SIM_NETWORK_UNLOCK_ALLOW_DISMISS_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SIM_NETWORK_UNLOCK_ALLOW_DISMISS_BOOL: String
```

Flag indicating whether the Phone app should provide a "Dismiss" button on the SIM network unlock screen. The default value is true. If set to false, there will be \*no way\* to dismiss the SIM network unlock screen if you don't enter the correct unlock code. (One important consequence: there will be no way to make an Emergency Call if your SIM is network-locked and you don't know the PIN.)

 Value: "sim_network_unlock_allow_dismiss_bool"

### KEY_SMDP_SERVER_ADDRESS_STRING

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SMDP_SERVER_ADDRESS_STRING: String
```

SMDP+ server address for downloading opportunistic eSIM profile. FQDN (Fully Qualified Domain Name) of the SM-DP+ (e.g., smdp.gsma.com) restricted to the Alphanumeric mode character set defined in table 5 of ISO/IEC 18004 excluding '$'.

 Value: "smdp_server_address_string"

### KEY_SMS_REQUIRES_DESTINATION_NUMBER_CONVERSION_BOOL

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SMS_REQUIRES_DESTINATION_NUMBER_CONVERSION_BOOL: String
```

Determines if the carrier requires converting the destination number before sending out an SMS. Certain networks and numbering plans require different formats.

 Value: "sms_requires_destination_number_conversion_bool"

### KEY_SUBSCRIPTION_GROUP_UUID_STRING

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SUBSCRIPTION_GROUP_UUID_STRING: String
```

The UUID of a Group of related subscriptions in which to place the current subscription. A grouped subscription will behave for billing purposes and other UI purposes as though it is a transparent extension of other subscriptions in the group.

If set to `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#REMOVE_GROUP_UUID_STRING:kotlin.String`, then the subscription will be removed from its current group.

This key will work all the way back to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int`.

 Value: "subscription_group_uuid_string"

### KEY_SUPPORTED_PREMIUM_CAPABILITIES_INT_ARRAY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SUPPORTED_PREMIUM_CAPABILITIES_INT_ARRAY: String
```

A list of premium capabilities the carrier supports. Applications can prompt users to purchase these premium capabilities from their carrier for a performance boost. Valid values are any of `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager`'s `PREMIUM_CAPABILITY_*` constants. This is empty by default, indicating that no premium capabilities are supported.

 Value: "supported_premium_capabilities_int_array"

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#isPremiumCapabilityAvailableForPurchase(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#purchasePremiumCapability(kotlin.Int,%20java.util.concurrent.Executor,%20java.util.function.Consumer)`

### KEY_SUPPORTS_BUSINESS_CALL_COMPOSER_BOOL

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SUPPORTS_BUSINESS_CALL_COMPOSER_BOOL: String
```

Indicates if the carrier supports a business call composer.

 Value: "supports_business_call_composer_bool"

### KEY_SUPPORTS_CALL_COMPOSER_BOOL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SUPPORTS_CALL_COMPOSER_BOOL: String
```

Indicates if the carrier supports call composer.

 Value: "supports_call_composer_bool"

### KEY_SUPPORTS_CUSTOMIZED_RINGING_SIGNAL_BOOL

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SUPPORTS_CUSTOMIZED_RINGING_SIGNAL_BOOL: String
```

Indicates if the carrier supports Customized Ringing Signal (CRS). The Customized Ringing Signal (CRS) is an operator-specific feature that allows a subscriber to customize the media played to the called party during the establishment of an incoming call. When the MT call is received, the device will present the CRS media instead of its standard ringtone. This CRS media can consist of audio, video, still images, or any combination thereof. If true, telephony will handle incoming calls with CRS media as specified by the vendor IMS stack.

 Value: "supports_customized_ringing_signal_bool"

### KEY_SUPPORTS_DEVICE_TO_DEVICE_COMMUNICATION_USING_DTMF_BOOL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SUPPORTS_DEVICE_TO_DEVICE_COMMUNICATION_USING_DTMF_BOOL: String
```

Indicates whether the carrier supports the use of DTMF digits A-D for the purpose of device to device communication while in a call.

 Value: "supports_device_to_device_communication_using_dtmf_bool"

### KEY_SUPPORTS_DEVICE_TO_DEVICE_COMMUNICATION_USING_RTP_BOOL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SUPPORTS_DEVICE_TO_DEVICE_COMMUNICATION_USING_RTP_BOOL: String
```

Indicates whether the carrier supports the use of RFC8285 compliant RTP header extensions for the purpose of device to device communication while in a call.

See also `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SUPPORTS_SDP_NEGOTIATION_OF_D2D_RTP_HEADER_EXTENSIONS_BOOL:kotlin.String`.

 Value: "supports_device_to_device_communication_using_rtp_bool"

### KEY_SUPPORTS_SDP_NEGOTIATION_OF_D2D_RTP_HEADER_EXTENSIONS_BOOL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SUPPORTS_SDP_NEGOTIATION_OF_D2D_RTP_HEADER_EXTENSIONS_BOOL: String
```

Indicates whether the carrier supports the negotiations of RFC8285 compliant RTP header extensions supported on a call during the Session Description Protocol (SDP). This option is only used when `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SUPPORTS_DEVICE_TO_DEVICE_COMMUNICATION_USING_RTP_BOOL:kotlin.String` is `true`.

When `true`, the RTP header extensions the platform uses for device to device communication will be offered to the remote end during the SDP negotiation process. When `false`, the RTP header extensions will not be negotiated during the SDP negotiation process and the platform will send RTP header extensions without prior negotiation if `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SUPPORTS_DEVICE_TO_DEVICE_COMMUNICATION_USING_RTP_BOOL:kotlin.String` is `true`.

 Value: "supports_sdp_negotiation_of_d2d_rtp_header_extensions_bool"

### KEY_SUPPORTS_UNIDIRECTIONAL_VIDEO_SERVICE_BOOL

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SUPPORTS_UNIDIRECTIONAL_VIDEO_SERVICE_BOOL: String
```

Indicates if the carrier supports a unidirectional video service call (UVS).

 Value: "supports_unidirectional_video_service_bool"

### KEY_SUPPORTS_VIDEO_RINGBACK_BOOL

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SUPPORTS_VIDEO_RINGBACK_BOOL: String
```

Indicates if the carrier supports a video color ring back tone call (CRBT).

 Value: "supports_video_back_tone_bool"

### KEY_SUPPORT_3GPP_CALL_FORWARDING_WHILE_ROAMING_BOOL

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SUPPORT_3GPP_CALL_FORWARDING_WHILE_ROAMING_BOOL: String
```

Indicates whether the carrier supports 3gpp call forwarding MMI codes while roaming. If false, the user will be notified that call forwarding is not available when the MMI code fails.

 Value: "support_3gpp_call_forwarding_while_roaming_bool"

### KEY_SUPPORT_ADD_CONFERENCE_PARTICIPANTS_BOOL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SUPPORT_ADD_CONFERENCE_PARTICIPANTS_BOOL: String
```

Determines whether conference participants can be added to existing call to form an adhoc conference call (in contrast to merging calls to form a conference). When `true`, adding conference participants to existing call is supported, `false otherwise`.

 Value: "support_add_conference_participants_bool"

### KEY_SUPPORT_ADHOC_CONFERENCE_CALLS_BOOL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SUPPORT_ADHOC_CONFERENCE_CALLS_BOOL: String
```

Determines whether adhoc conference calls are supported by a carrier. When `true`, adhoc conference calling is supported, `false otherwise`.

 Value: "support_adhoc_conference_calls_bool"

### KEY_SUPPORT_CLIR_NETWORK_DEFAULT_BOOL

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SUPPORT_CLIR_NETWORK_DEFAULT_BOOL: String
```

Flag indicating whether to support "Network default" option in Caller ID settings for Calling Line Identification Restriction (CLIR).

 Value: "support_clir_network_default_bool"

### KEY_SUPPORT_CONFERENCE_CALL_BOOL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SUPPORT_CONFERENCE_CALL_BOOL: String
```

Determines whether conference calls are supported by a carrier. When `true`, conference calling is supported, `false otherwise`.

 Value: "support_conference_call_bool"

### KEY_SUPPORT_EMERGENCY_SMS_OVER_IMS_BOOL

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SUPPORT_EMERGENCY_SMS_OVER_IMS_BOOL: String
```

Flag indicating whether or not sending emergency SMS messages over IMS is supported when in LTE/limited LTE (Emergency only) service mode.

Use `ImsSms#KEY_EMERGENCY_SMS_OVER_EMERGENCY_PDN_INT_ARRAY` instead to specify the network registration status (Home or Roaming) where the device should use Emergency PDN for Emergency SMS.

 Value: "support_emergency_sms_over_ims_bool"

### KEY_SUPPORT_ENHANCED_CALL_BLOCKING_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SUPPORT_ENHANCED_CALL_BLOCKING_BOOL: String
```

Determines whether to enable enhanced call blocking feature on the device. android.provider.BlockedNumberContract.SystemContract#ENHANCED_SETTING_KEY_BLOCK_UNREGISTERED android.provider.BlockedNumberContract.SystemContract#ENHANCED_SETTING_KEY_BLOCK_PRIVATE android.provider.BlockedNumberContract.SystemContract#ENHANCED_SETTING_KEY_BLOCK_PAYPHONE android.provider.BlockedNumberContract.SystemContract#ENHANCED_SETTING_KEY_BLOCK_UNKNOWN android.provider.BlockedNumberContract.SystemContract#ENHANCED_SETTING_KEY_BLOCK_UNAVAILABLE

1. For Single SIM(SS) device, it can be customized in both carrier_config_mccmnc.xml and vendor.xml.

2. For Dual SIM(DS) device, it should be customized in vendor.xml, since call blocking function is used regardless of SIM.

If `true` enable enhanced call blocking feature on the device, `false` otherwise.

 Value: "support_enhanced_call_blocking_bool"

### KEY_SUPPORT_IMS_CONFERENCE_EVENT_PACKAGE_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SUPPORT_IMS_CONFERENCE_EVENT_PACKAGE_BOOL: String
```

Determines whether the IMS conference merge process supports and returns its participants data. When `true`, on merge complete, conference call would have a list of its participants returned in XML format, `false otherwise`.

 Value: "support_ims_conference_event_package_bool"

### KEY_SUPPORT_MULTI_PARTY_ANCHOR_CONFERENCE_BOOL

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SUPPORT_MULTI_PARTY_ANCHOR_CONFERENCE_BOOL: String
```

Determine whether multi-party anchor conference calls are supported by a carrier. When `true`, merging a locally hosted conference call with a remotely hosted conference into a multi-party anchor conference call is permitted, `false otherwise`.

 Value: "support_multi_anchor_conf_bool"

### KEY_SUPPORT_PAUSE_IMS_VIDEO_CALLS_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SUPPORT_PAUSE_IMS_VIDEO_CALLS_BOOL: String
```

For IMS video over LTE calls, determines whether video pause signalling is supported.

 Value: "support_pause_ims_video_calls_bool"

### KEY_SUPPORT_PHONE_NUMBER_SOURCE_TS43_BOOL

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SUPPORT_PHONE_NUMBER_SOURCE_TS43_BOOL: String
```

Determines if the carrier supports retrieving the phone number via the TS.43 protocol. Reference: GSMA TS.43-v11 section 13

 Value: "support_phone_number_source_ts43_bool"

### KEY_SUPPORT_SWAP_AFTER_MERGE_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SUPPORT_SWAP_AFTER_MERGE_BOOL: String
```

**Deprecated:** *Legacy CDMA is unsupported.*

After a CDMA conference call is merged, the swap button should be displayed.

 Value: "support_swap_after_merge_bool"

### KEY_SUPPORT_TDSCDMA_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SUPPORT_TDSCDMA_BOOL: String
```

Boolean to decide whether TD-SCDMA is supported.

 Value: "support_tdscdma_bool"

### KEY_SUPPORT_TDSCDMA_ROAMING_NETWORKS_STRING_ARRAY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SUPPORT_TDSCDMA_ROAMING_NETWORKS_STRING_ARRAY: String
```

A list of mcc/mnc that support TD-SCDMA for device when connect to the roaming network.

 Value: "support_tdscdma_roaming_networks_string_array"

### KEY_SWITCH_DATA_TO_PRIMARY_IF_PRIMARY_IS_OOS_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SWITCH_DATA_TO_PRIMARY_IF_PRIMARY_IS_OOS_BOOL: String
```

Controls whether to switch data to primary from opportunistic subscription if primary is out of service. This control only affects system or 1st party app initiated data switch, but will not override data switch initiated by privileged carrier apps This carrier config is used to disable this feature.

 Value: "switch_data_to_primary_if_primary_is_oos_bool"

### KEY_TREAT_DOWNGRADED_VIDEO_CALLS_AS_VIDEO_CALLS_BOOL

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_TREAT_DOWNGRADED_VIDEO_CALLS_AS_VIDEO_CALLS_BOOL: String
```

Flag indicating whether some telephony logic will treat a call which was formerly a video call as if it is still a video call. When `true`:

Logic which will automatically drop a video call which takes place over WIFI when a voice call is answered (see `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_DROP_VIDEO_CALL_WHEN_ANSWERING_AUDIO_CALL_BOOL:kotlin.String`.

Logic which determines whether the user can use TTY calling.

 Value: "treat_downgraded_video_calls_as_video_calls_bool"

### KEY_TTY_SUPPORTED_BOOL

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_TTY_SUPPORTED_BOOL: String
```

Boolean flag indicating whether the carrier supports TTY.

Note that `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_VOLTE_TTY_SUPPORTED_BOOL:kotlin.String` controls availability of TTY over VoLTE; if this carrier configuration is disabled, then `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_VOLTE_TTY_SUPPORTED_BOOL:kotlin.String` is also implicitly disabled.

`https://developer.android.com/reference/kotlin/android/telecom/TelecomManager.html#isTtySupported()` should be used to determine if a device supports TTY, and this carrier config key should be used to see if the current carrier supports it.

 Value: "tty_supported_bool"

### KEY_UNLOGGABLE_NUMBERS_STRING_ARRAY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_UNLOGGABLE_NUMBERS_STRING_ARRAY: String
```

A string array containing numbers that shouldn't be included in the call log.

 Value: "unloggable_numbers_string_array"

### KEY_USE_ACS_FOR_RCS_BOOL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_USE_ACS_FOR_RCS_BOOL: String
```

Indicates if auto-configuration server is used for the RCS config Reference: GSMA RCC.14

 Value: "use_acs_for_rcs_bool"

### KEY_USE_HFA_FOR_PROVISIONING_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_USE_HFA_FOR_PROVISIONING_BOOL: String
```

CDMA activation goes through HFA

 Value: "use_hfa_for_provisioning_bool"

### KEY_USE_IP_FOR_CALLING_INDICATOR_BOOL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_USE_IP_FOR_CALLING_INDICATOR_BOOL: String
```

Determines whether or not to use (IP) data connectivity as a supplemental condition to control the visibility of the no-calling indicator for this carrier in the System UI. Setting the configuration to true may make sense for carriers that provide OTT calling. Config = true: show no-calling indication only if telephony does not have voice registration and if no (IP) data connectivity is available. Config = false: show no-calling indication only if telephony does not have voice registration.

 Value: "use_ip_for_calling_indicator_bool"

### KEY_USE_OTASP_FOR_PROVISIONING_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_USE_OTASP_FOR_PROVISIONING_BOOL: String
```

**Deprecated:** *Legacy CDMA is unsupported.*

CDMA activation goes through OTASP.

 Value: "use_otasp_for_provisioning_bool"

### KEY_USE_RCS_PRESENCE_BOOL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_USE_RCS_PRESENCE_BOOL: String
```

**Deprecated:** *No longer used in framework code, however it may still be used by applications that have not updated their code. This config should still be set to `true` if `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.Ims#KEY_RCS_BULK_CAPABILITY_EXCHANGE_BOOL:kotlin.String` is set to `true` and `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.Ims#KEY_ENABLE_PRESENCE_CAPABILITY_EXCHANGE_BOOL:kotlin.String` is set to `true`.*

Flag indicating whether or not the carrier supports the periodic exchange of phone numbers in the user's address book with the carrier's presence server in order to retrieve the RCS capabilities for each contact used in the RCS User Capability Exchange (UCE) procedure. See RCC.71, section 3 for more information.

The flag `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.Ims#KEY_ENABLE_PRESENCE_PUBLISH_BOOL:kotlin.String` must also be enabled if this flag is enabled, as sending a periodic SIP PUBLISH with this device's RCS capabilities is a requirement for capability exchange to begin.

When presence is supported, the device should use the `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns.html#CARRIER_PRESENCE:kotlin.String` bit mask and set the `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns.html#CARRIER_PRESENCE_VT_CAPABLE:kotlin.Int` bit to indicate whether each contact supports video calling. The UI is made aware that presence is enabled via `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount.html#CAPABILITY_VIDEO_CALLING_RELIES_ON_PRESENCE:kotlin.Int` and can choose to hide or show the video calling icon based on whether a contact supports video.

 Value: "use_rcs_presence_bool"

### KEY_USE_RCS_SIP_OPTIONS_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_USE_RCS_SIP_OPTIONS_BOOL: String
```

Flag indicating whether the carrier supports RCS SIP OPTIONS indication for User Capability Exchange (UCE).

 Value: "use_rcs_sip_options_bool"

### KEY_USE_WFC_HOME_NETWORK_MODE_IN_ROAMING_NETWORK_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_USE_WFC_HOME_NETWORK_MODE_IN_ROAMING_NETWORK_BOOL: String
```

Flag specifying whether the carrier will use the WFC home network mode in roaming network. `false` - roaming preference can be selected separately from the home preference. `true` - roaming preference is the same as home preference and `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_DEFAULT_WFC_IMS_MODE_INT:kotlin.String` is used as the default value.

 Value: "use_wfc_home_network_mode_in_roaming_network_bool"

### KEY_VOICEMAIL_NOTIFICATION_PERSISTENT_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_VOICEMAIL_NOTIFICATION_PERSISTENT_BOOL: String
```

Determine whether the voicemail notification is persistent in the notification bar. If true, the voicemail notifications cannot be dismissed from the notification bar.

 Value: "voicemail_notification_persistent_bool"

### KEY_VOICE_PRIVACY_DISABLE_UI_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_VOICE_PRIVACY_DISABLE_UI_BOOL: String
```

If true, removes the Voice Privacy option from Call Settings

 Value: "voice_privacy_disable_ui_bool"

### KEY_VOLTE_REPLACEMENT_RAT_INT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_VOLTE_REPLACEMENT_RAT_INT: String
```

If Voice Radio Technology is RIL_RADIO_TECHNOLOGY_LTE:14 or RIL_RADIO_TECHNOLOGY_UNKNOWN:0 this is the value that should be used instead. A configuration value of RIL_RADIO_TECHNOLOGY_UNKNOWN:0 means there is no replacement value and that the default assumption for phone type (GSM) should be used.

 Value: "volte_replacement_rat_int"

### KEY_VONR_ENABLED_BOOL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_VONR_ENABLED_BOOL: String
```

Flag specifying whether VoNR should be enabled for carrier. If true, VoNr will be enabled. If false, hard disabled. Disabled by default.

 Value: "vonr_enabled_bool"

### KEY_VONR_ON_BY_DEFAULT_BOOL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_VONR_ON_BY_DEFAULT_BOOL: String
```

Boolean indicating the default VoNR user preference setting. If true, the VoNR setting will be enabled. If false, it will be disabled initially. Enabled by default.

 Value: "vonr_on_by_default_bool"

### KEY_VONR_SETTING_VISIBILITY_BOOL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_VONR_SETTING_VISIBILITY_BOOL: String
```

Boolean indicating if the VoNR setting is visible in the Call Settings menu. If this flag is set and VoNR is enabled for this carrier (see `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_VONR_ENABLED_BOOL:kotlin.String`) the VoNR setting menu will be visible. If `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_VONR_ENABLED_BOOL:kotlin.String` or this setting is false, the menu will be gone. Enabled by default.

 Value: "vonr_setting_visibility_bool"

### KEY_VT_UPGRADE_SUPPORTED_FOR_DOWNGRADED_RTT_CALL_BOOL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_VT_UPGRADE_SUPPORTED_FOR_DOWNGRADED_RTT_CALL_BOOL: String
```

Indicates if the carrier supports upgrading a call that was previously an RTT call to VT.

 Value: "vt_upgrade_supported_for_downgraded_rtt_call"

### KEY_VVM_CELLULAR_DATA_REQUIRED_BOOL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_VVM_CELLULAR_DATA_REQUIRED_BOOL: String
```

Whether cellular data is required to access visual voicemail.

 Value: "vvm_cellular_data_required_bool"

### KEY_VVM_CLIENT_PREFIX_STRING

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_VVM_CLIENT_PREFIX_STRING: String
```

The default OMTP visual voicemail client prefix to use. Defaulted to "//VVM"

 Value: "vvm_client_prefix_string"

### KEY_VVM_DESTINATION_NUMBER_STRING

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_VVM_DESTINATION_NUMBER_STRING: String
```

The carrier number mobile outgoing (MO) sms messages are sent to.

 Value: "vvm_destination_number_string"

### KEY_VVM_DISABLED_CAPABILITIES_STRING_ARRAY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_VVM_DISABLED_CAPABILITIES_STRING_ARRAY: String
```

A set of capabilities that should not be used even if it is reported by the visual voicemail IMAP CAPABILITY command.

 Value: "vvm_disabled_capabilities_string_array"

### KEY_VVM_LEGACY_MODE_ENABLED_BOOL

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_VVM_LEGACY_MODE_ENABLED_BOOL: String
```

Whether legacy mode should be used when the visual voicemail client is disabled.

Legacy mode is a mode that on the carrier side visual voicemail is still activated, but on the client side all network operations are disabled. SMSs are still monitored so a new message SYNC SMS will be translated to show a message waiting indicator, like traditional voicemails.

This is for carriers that does not support VVM deactivation so voicemail can continue to function without the data cost.

 Value: "vvm_legacy_mode_enabled_bool"

### KEY_VVM_PORT_NUMBER_INT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_VVM_PORT_NUMBER_INT: String
```

The port through which the mobile outgoing (MO) sms messages are sent through.

 Value: "vvm_port_number_int"

### KEY_VVM_PREFETCH_BOOL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_VVM_PREFETCH_BOOL: String
```

Whether to prefetch audio data on new voicemail arrival, defaulted to true.

 Value: "vvm_prefetch_bool"

### KEY_VVM_SSL_ENABLED_BOOL

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_VVM_SSL_ENABLED_BOOL: String
```

Whether to use SSL to connect to the visual voicemail IMAP server. Defaulted to false.

 Value: "vvm_ssl_enabled_bool"

### KEY_VVM_TYPE_STRING

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_VVM_TYPE_STRING: String
```

The type of visual voicemail protocol the carrier adheres to. See `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager` for possible values. For example `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#VVM_TYPE_OMTP:kotlin.String`.

 Value: "vvm_type_string"

### KEY_WFC_EMERGENCY_ADDRESS_CARRIER_APP_STRING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_WFC_EMERGENCY_ADDRESS_CARRIER_APP_STRING: String
```

The Component Name of the activity that can setup the emergency address for WiFi Calling as per carrier requirement.

 Value: "wfc_emergency_address_carrier_app_string"

### KEY_WORLD_MODE_ENABLED_BOOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_WORLD_MODE_ENABLED_BOOL: String
```

Boolean to decide whether world mode is enabled.

 Value: "world_mode_enabled_bool"

### KEY_WORLD_PHONE_BOOL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_WORLD_PHONE_BOOL: String
```

Flag indicating if the phone is a world phone

 Value: "world_phone_bool"

### OPP_AUTO_DATA_SWITCH_POLICY_DISABLED

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPP_AUTO_DATA_SWITCH_POLICY_DISABLED: Int
```

Auto data network switch policy between primary and opportunistic profiles in the same subscription group: switching is disabled.

 Value: 0

### OPP_AUTO_DATA_SWITCH_POLICY_FOLLOW_SYSTEM

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPP_AUTO_DATA_SWITCH_POLICY_FOLLOW_SYSTEM: Int
```

Auto data network switch policy between primary and opportunistic profiles in the same subscription group: enable all system supported policies.

Enable data network switch by considering all supported information including but not limited on Network Registration State, Technologies (4G/5G), Signal Strength, Data subscription plan etc.

The system behavior may change over releases. Carriers can override with specific policies below if carriers would like a consistent behavior.

 Value: 2147483647

### OPP_AUTO_DATA_SWITCH_POLICY_FOR_AVAILABILITY

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPP_AUTO_DATA_SWITCH_POLICY_FOR_AVAILABILITY: Int
```

Auto data network switch policy between primary and opportunistic profiles in the same subscription group: switch to the network only with better availability.

In specific, when primary or opportunistic network is out of service while the other is active and in service, switch to the other one.

The availability-based switch is also restricted by the device resource config `auto_data_switch_availability_stability_time_threshold_millis`.

 Value: 1

### OPP_AUTO_DATA_SWITCH_POLICY_FOR_PERFORMANCE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPP_AUTO_DATA_SWITCH_POLICY_FOR_PERFORMANCE: Int
```

Auto data network switch policy between primary and opportunistic profiles in the same subscription group: switch to the network with better data connection performance.

In specific, when both networks are connected, device may switch to network with better technologies (e.g. NR over LTE) and/or signal strength.

The performance-based switch is also restricted by the device resource config `auto_data_switch_performance_stability_time_threshold_millis`.

Performance based policy implicitly include availability based policy, that is, when primary or opportunistic is out of service, follow the same behavior for policy `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#OPP_AUTO_DATA_SWITCH_POLICY_FOR_AVAILABILITY:kotlin.Int`.

 Value: 3

### REMOVE_GROUP_UUID_STRING

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REMOVE_GROUP_UUID_STRING: String
```

Passing this value as `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SUBSCRIPTION_GROUP_UUID_STRING:kotlin.String` will remove the subscription from a group instead of adding it to a group.

This value will work all the way back to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int`.

 Value: "00000000-0000-0000-0000-000000000000"

### SATELLITE_DATA_SUPPORT_ALL

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SATELLITE_DATA_SUPPORT_ALL: Int
```

Support unrestricted satellite network that serves all traffic.

 Value: 2

### SATELLITE_DATA_SUPPORT_BANDWIDTH_CONSTRAINED

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SATELLITE_DATA_SUPPORT_BANDWIDTH_CONSTRAINED: Int
```

Support unrestricted but bandwidth_constrained traffic on satellite network.

 Value: 1

### SATELLITE_DATA_SUPPORT_ONLY_RESTRICTED

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SATELLITE_DATA_SUPPORT_ONLY_RESTRICTED: Int
```

Doesn't support unrestricted traffic on satellite network.

 Value: 0

### SERVICE_CLASS_NONE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SERVICE_CLASS_NONE: Int
```

Service class flag if no specific service class is specified. Reference: 3GPP TS 27.007 Section 7.4 Facility lock +CLCK

 Value: 0

### SERVICE_CLASS_VOICE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SERVICE_CLASS_VOICE: Int
```

Service class flag for voice telephony. Reference: 3GPP TS 27.007 Section 7.4 Facility lock +CLCK

 Value: 1

### USSD_OVER_CS_ONLY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USSD_OVER_CS_ONLY: Int
```

Only send USSD over CS. `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_USSD_METHOD_INT:kotlin.String`

 Value: 2

### USSD_OVER_CS_PREFERRED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USSD_OVER_CS_PREFERRED: Int
```

Only send USSD over IMS while CS is out of service, otherwise send USSD over CS. `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_USSD_METHOD_INT:kotlin.String`

 Value: 0

### USSD_OVER_IMS_ONLY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USSD_OVER_IMS_ONLY: Int
```

Only send USSD over IMS and disallow silent redial over CS. `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_USSD_METHOD_INT:kotlin.String`

 Value: 3

### USSD_OVER_IMS_PREFERRED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USSD_OVER_IMS_PREFERRED: Int
```

Send USSD over IMS or CS while IMS is out of service or silent redial over CS if needed. `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_USSD_METHOD_INT:kotlin.String`

 Value: 1

## Public methods

### getConfig

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getConfig(): PersistableBundle?
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#getConfig(kotlin.String)` instead.*

Gets the configuration values for the default subscription. After using this method to get the configuration bundle, `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#isConfigForIdentifiedCarrier(android.os.PersistableBundle)` should be called to confirm whether any carrier specific configuration has been applied.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String`, or the calling app has carrier privileges (see `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges()`). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String`

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#?` | This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#getConfig(kotlin.String)`

### getConfig

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getConfig(vararg keys: String!): PersistableBundle
```

Gets the configuration values of the specified config keys applied for the default subscription.

If the value for the key can't be found, the returned bundle will filter the key out.

After using this method to get the configuration bundle, `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#isConfigForIdentifiedCarrier(android.os.PersistableBundle)` should be called to confirm whether any carrier specific configuration has been applied.

Note that on success, the key/value for `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_CONFIG_VERSION_STRING:kotlin.String` and `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_CONFIG_APPLIED_BOOL:kotlin.String` are always in the returned bundle, no matter if they were explicitly requested.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String`, or the calling app has carrier privileges for the default subscription (see `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges()`). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges()`

| Parameters ||
|---|---|
| `keys` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The config keys to retrieve values. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#` | A `https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#` with key/value mapping for the specified carrier configs on success, or an empty (but never null) bundle on failure. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#getConfigForSubId(kotlin.Int,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getDefaultSubscriptionId()`

### getConfigByComponentForSubId

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getConfigByComponentForSubId(
    prefix: String, 
    subId: Int
): PersistableBundle?
```

Gets the configuration values for a component using its prefix.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String`, or the calling app has carrier privileges (see `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges()`). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String`

| Parameters ||
|---|---|
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): prefix of the component. This value cannot be `null`. |
| `subId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the subscription ID, normally obtained from `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#?` | This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

**See Also**

### getConfigForSubId

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getConfigForSubId(subId: Int): PersistableBundle?
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#getConfigForSubId(kotlin.Int,%20kotlin.String)` instead.*

Gets the configuration values for a particular subscription, which is associated with a specific SIM card. If an invalid subId is used, the returned config will contain default values. After using this method to get the configuration bundle, `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#isConfigForIdentifiedCarrier(android.os.PersistableBundle)` should be called to confirm whether any carrier specific configuration has been applied.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String`, or the calling app has carrier privileges (see `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges()`). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String`

| Parameters ||
|---|---|
| `subId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the subscription ID, normally obtained from `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#?` | A `https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#` containing the config for the given subId, or default values for an invalid subId. This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### getConfigForSubId

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getConfigForSubId(
    subId: Int, 
    vararg keys: String!
): PersistableBundle
```

Gets the configuration values of the specified keys for a particular subscription.

If an invalid subId is used, the returned configuration will contain default values for the specified keys. If the value for the key can't be found, the returned configuration will filter the key out.

After using this method to get the configuration bundle, `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#isConfigForIdentifiedCarrier(android.os.PersistableBundle)` should be called to confirm whether any carrier specific configuration has been applied.

Note that on success, the key/value for `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_CONFIG_VERSION_STRING:kotlin.String` and `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_CONFIG_APPLIED_BOOL:kotlin.String` are always in the returned bundle, no matter if they were explicitly requested.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String`, or the calling app has carrier privileges on the specified subscription (see `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges()`). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges()`

| Parameters ||
|---|---|
| `subId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The subscription ID on which the carrier config should be retrieved. |
| `keys` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The carrier config keys to retrieve values. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#` | A `https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#` with key/value mapping for the specified configuration on success, or an empty (but never null) bundle on failure (for example, when the calling app has no permission). |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### isConfigForIdentifiedCarrier

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun isConfigForIdentifiedCarrier(bundle: PersistableBundle!): Boolean
```

Determines whether a configuration `https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#` obtained from `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#getConfig()` or `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#getConfigForSubId(kotlin.Int)` corresponds to an identified carrier.

When an app receives the `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#ACTION_CARRIER_CONFIG_CHANGED:kotlin.String` broadcast which informs it that the carrier configuration has changed, it is possible that another reload of the carrier configuration has begun since the intent was sent. In this case, the carrier configuration the app fetches (e.g. via `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#getConfig()`) may not represent the configuration for the current carrier. It should be noted that it does not necessarily mean the configuration belongs to current carrier when this function return true because it may belong to another previous identified carrier. Users should always call `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#getConfig()` or `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#getConfigForSubId(kotlin.Int)` after receiving the broadcast `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#ACTION_CARRIER_CONFIG_CHANGED:kotlin.String`.

After using `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#getConfig()` or `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#getConfigForSubId(kotlin.Int)` an app should always use this method to confirm whether any carrier specific configuration has been applied. Especially when an app misses the broadcast `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#ACTION_CARRIER_CONFIG_CHANGED:kotlin.String` but it still needs to get the current configuration, it must use this method to verify whether the configuration is default or carrier overridden.

| Parameters ||
|---|---|
| `bundle` | [PersistableBundle](../android.os/PersistableBundle.md)!: the configuration bundle to be checked. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | boolean true if any carrier specific configuration bundle has been applied, false otherwise or the bundle is null. |

### notifyConfigChangedForSubId

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun notifyConfigChangedForSubId(subId: Int): Unit
```

Calling this method triggers telephony services to fetch the current carrier configuration.

Normally this does not need to be called because the platform reloads config on its own. This should be called by a carrier service app if it wants to update config at an arbitrary moment.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String`, or the calling app has carrier privileges (see `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges()`).

This method returns before the reload has completed, and android.service.carrier.CarrierService#onLoadConfig will be called from an arbitrary thread. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String`

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `subId` is invalid. |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### registerCarrierConfigChangeListener

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerCarrierConfigChangeListener(
    executor: Executor, 
    listener: CarrierConfigManager.CarrierConfigChangeListener
): Unit
```

Register a `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.CarrierConfigChangeListener` to get a notification when carrier configurations have changed.

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): The executor on which the listener will be called. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `listener` | [CarrierConfigManager.CarrierConfigChangeListener](../android/telephony/CarrierConfigManager.CarrierConfigChangeListener.md): The CarrierConfigChangeListener called when carrier configs has changed. This value cannot be `null`. |

### unregisterCarrierConfigChangeListener

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unregisterCarrierConfigChangeListener(listener: CarrierConfigManager.CarrierConfigChangeListener): Unit
```

Unregister the `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.CarrierConfigChangeListener` to stop notification on carrier configurations change.

| Parameters ||
|---|---|
| `listener` | [CarrierConfigManager.CarrierConfigChangeListener](../android/telephony/CarrierConfigManager.CarrierConfigChangeListener.md): The CarrierConfigChangeListener which was registered with method `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#registerCarrierConfigChangeListener(java.util.concurrent.Executor,%20android.telephony.CarrierConfigManager.CarrierConfigChangeListener)`. This value cannot be `null`. |
