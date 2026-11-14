# DataFailCause

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DataFailCause

Kotlin| [Java](https://developer.android.com/reference/android/telephony/DataFailCause "View this page in Java") 

```
class DataFailCause
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.telephony.DataFailCause](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#) |

DataFailCause collects data connection failure causes code from different sources.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACCESS_ATTEMPT_ALREADY_IN_PROGRESS](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#ACCESS_ATTEMPT_ALREADY_IN_PROGRESS:kotlin.Int) Access attempt is already in progress. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACCESS_BLOCK](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#ACCESS_BLOCK:kotlin.Int) Access blocked by the base station. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACCESS_BLOCK_ALL](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#ACCESS_BLOCK_ALL:kotlin.Int) Access blocked by the base station for all mobile devices. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACCESS_CLASS_DSAC_REJECTION](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#ACCESS_CLASS_DSAC_REJECTION:kotlin.Int) Access class blocking restrictions for the current camped cell. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACCESS_CONTROL_LIST_CHECK_FAILURE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#ACCESS_CONTROL_LIST_CHECK_FAILURE:kotlin.Int) Access control list check failure at the lower layer. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACTIVATION_REJECTED_BCM_VIOLATION](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#ACTIVATION_REJECTED_BCM_VIOLATION:kotlin.Int) UE requested to modify QoS parameters or the bearer control mode, which is not compatible with the selected bearer control mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACTIVATION_REJECT_GGSN](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#ACTIVATION_REJECT_GGSN:kotlin.Int) Activation rejected by Gateway GPRS Support Node (GGSN), Serving Gateway or PDN Gateway. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACTIVATION_REJECT_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#ACTIVATION_REJECT_UNSPECIFIED:kotlin.Int) Activation rejected, unspecified. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACTIVE_PDP_CONTEXT_MAX_NUMBER_REACHED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#ACTIVE_PDP_CONTEXT_MAX_NUMBER_REACHED:kotlin.Int) Max number of Packet Data Protocol (PDP) context reached. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALL_MATCHING_RULES_FAILED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#ALL_MATCHING_RULES_FAILED:kotlin.Int) If connection failed for all matching URSP rules. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [APN_DISABLED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#APN_DISABLED:kotlin.Int) APN has been disabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [APN_DISALLOWED_ON_ROAMING](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#APN_DISALLOWED_ON_ROAMING:kotlin.Int) PDN connection to the APN is disallowed on the roaming network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [APN_MISMATCH](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#APN_MISMATCH:kotlin.Int) New PDN bring up is rejected during interface selection because the UE has already allotted the available interfaces for other PDNs. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [APN_PARAMETERS_CHANGED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#APN_PARAMETERS_CHANGED:kotlin.Int) APN-related parameters are changed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [APN_PENDING_HANDOVER](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#APN_PENDING_HANDOVER:kotlin.Int) Interface bring up is attempted for an APN that is yet to be handed over to target RAT. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [APN_TYPE_CONFLICT](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#APN_TYPE_CONFLICT:kotlin.Int) APN type conflict. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AUTH_FAILURE_ON_EMERGENCY_CALL](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#AUTH_FAILURE_ON_EMERGENCY_CALL:kotlin.Int) Authentication failure on emergency call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BEARER_HANDLING_NOT_SUPPORTED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#BEARER_HANDLING_NOT_SUPPORTED:kotlin.Int) Procedure requested by the UE was rejected because the bearer handling is not supported. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CALL_DISALLOWED_IN_ROAMING](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#CALL_DISALLOWED_IN_ROAMING:kotlin.Int) Roaming is disallowed during call bring up. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CALL_PREEMPT_BY_EMERGENCY_APN](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#CALL_PREEMPT_BY_EMERGENCY_APN:kotlin.Int) Emergency call bring up on a different ePDG. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CANNOT_ENCODE_OTA_MESSAGE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#CANNOT_ENCODE_OTA_MESSAGE:kotlin.Int) Unable to encode the OTA message for MT PDP or deactivate PDP. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CDMA_ALERT_STOP](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#CDMA_ALERT_STOP:kotlin.Int) Received an alert stop from the base station due to incoming only. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CDMA_INCOMING_CALL](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#CDMA_INCOMING_CALL:kotlin.Int) Receiving an incoming call from the base station. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CDMA_INTERCEPT](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#CDMA_INTERCEPT:kotlin.Int) Received an intercept order from the base station. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CDMA_LOCK](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#CDMA_LOCK:kotlin.Int) Device in CDMA locked state. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CDMA_RELEASE_DUE_TO_SO_REJECTION](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#CDMA_RELEASE_DUE_TO_SO_REJECTION:kotlin.Int) Receiving a release from the base station with a SO (Service Option) Reject reason. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CDMA_REORDER](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#CDMA_REORDER:kotlin.Int) Receiving a reorder from the base station. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CDMA_RETRY_ORDER](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#CDMA_RETRY_ORDER:kotlin.Int) Receiving a retry order from the base station. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHANNEL_ACQUISITION_FAILURE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#CHANNEL_ACQUISITION_FAILURE:kotlin.Int) Channel acquisition failures. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CLOSE_IN_PROGRESS](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#CLOSE_IN_PROGRESS:kotlin.Int) Tearing down is in progress. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COLLISION_WITH_NETWORK_INITIATED_REQUEST](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#COLLISION_WITH_NETWORK_INITIATED_REQUEST:kotlin.Int) Network has already initiated the activation, modification, or deactivation of bearer resources that was requested by the UE. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPANION_IFACE_IN_USE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#COMPANION_IFACE_IN_USE:kotlin.Int) Companion interface in use. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONCURRENT_SERVICES_INCOMPATIBLE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#CONCURRENT_SERVICES_INCOMPATIBLE:kotlin.Int) The concurrent services requested were not compatible. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONCURRENT_SERVICES_NOT_ALLOWED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#CONCURRENT_SERVICES_NOT_ALLOWED:kotlin.Int) In favor of a voice call or SMS when concurrent voice and data are not supported. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONCURRENT_SERVICE_NOT_SUPPORTED_BY_BASE_STATION](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#CONCURRENT_SERVICE_NOT_SUPPORTED_BY_BASE_STATION:kotlin.Int) Concurrent service is not supported by base station. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONDITIONAL_IE_ERROR](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#CONDITIONAL_IE_ERROR:kotlin.Int) Conditional Information Element (IE) error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONGESTION](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#CONGESTION:kotlin.Int) Network cannot serve a request from the MS due to congestion. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONNECTION_RELEASED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#CONNECTION_RELEASED:kotlin.Int) Indicate the connection was released. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CS_DOMAIN_NOT_AVAILABLE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#CS_DOMAIN_NOT_AVAILABLE:kotlin.Int) CS domain is not available. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CS_FALLBACK_CALL_ESTABLISHMENT_NOT_ALLOWED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#CS_FALLBACK_CALL_ESTABLISHMENT_NOT_ALLOWED:kotlin.Int) CS fallback call establishment is not allowed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DATA_PLAN_EXPIRED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#DATA_PLAN_EXPIRED:kotlin.Int) Network initiates a detach on LTE with error cause ""data plan has been replenished or has expired. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DATA_ROAMING_SETTINGS_DISABLED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#DATA_ROAMING_SETTINGS_DISABLED:kotlin.Int) PDN Connection to a given APN is disallowed because data roaming is disabled from the device user interface settings and the UE is roaming. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DATA_SETTINGS_DISABLED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#DATA_SETTINGS_DISABLED:kotlin.Int) PDN Connection to a given APN is disallowed because data is disabled from the device user interface settings. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DBM_OR_SMS_IN_PROGRESS](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#DBM_OR_SMS_IN_PROGRESS:kotlin.Int) DBM or SMS is in progress. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DDS_SWITCHED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#DDS_SWITCHED:kotlin.Int) DDS (Default data subscription) switch occurs. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DDS_SWITCH_IN_PROGRESS](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#DDS_SWITCH_IN_PROGRESS:kotlin.Int) Default data subscription switch is in progress. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DRB_RELEASED_BY_RRC](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#DRB_RELEASED_BY_RRC:kotlin.Int) Data radio bearer is released by the RRC. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DS_EXPLICIT_DEACTIVATION](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#DS_EXPLICIT_DEACTIVATION:kotlin.Int) Dedicated bearer will be deactivated regardless of the network response. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DUAL_SWITCH](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#DUAL_SWITCH:kotlin.Int) Dual switch from single standby to dual standby is in progress. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DUN_CALL_DISALLOWED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#DUN_CALL_DISALLOWED:kotlin.Int) Dial up networking (DUN) call bring up is rejected since UE is in eHRPD RAT. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DUPLICATE_BEARER_ID](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#DUPLICATE_BEARER_ID:kotlin.Int) Active dedicated bearer was requested using the same default bearer ID. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EHRPD_TO_HRPD_FALLBACK](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#EHRPD_TO_HRPD_FALLBACK:kotlin.Int) Device falls back from eHRPD to HRPD. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EMBMS_NOT_ENABLED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#EMBMS_NOT_ENABLED:kotlin.Int) Data call has been brought down because EMBMS is not enabled at the RRC layer. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EMBMS_REGULAR_DEACTIVATION](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#EMBMS_REGULAR_DEACTIVATION:kotlin.Int) EMBMS data call has been successfully brought down. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EMERGENCY_IFACE_ONLY](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#EMERGENCY_IFACE_ONLY:kotlin.Int) Emergency interface only. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EMERGENCY_MODE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#EMERGENCY_MODE:kotlin.Int) Device is operating in Emergency mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EMM_ACCESS_BARRED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#EMM_ACCESS_BARRED:kotlin.Int) EPS (Evolved Packet System) Mobility Management (EMM) access barred. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EMM_ACCESS_BARRED_INFINITE_RETRY](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#EMM_ACCESS_BARRED_INFINITE_RETRY:kotlin.Int) EPS (Evolved Packet System) Mobility Management (EMM) access barred infinity retry. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EMM_ATTACH_FAILED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#EMM_ATTACH_FAILED:kotlin.Int) Attach procedure is rejected by the network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EMM_ATTACH_STARTED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#EMM_ATTACH_STARTED:kotlin.Int) Attach procedure is started for EMC purposes. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EMM_DETACHED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#EMM_DETACHED:kotlin.Int) UE is detached. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EMM_T3417_EXPIRED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#EMM_T3417_EXPIRED:kotlin.Int) T3417 timer expiration of the service request procedure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EMM_T3417_EXT_EXPIRED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#EMM_T3417_EXT_EXPIRED:kotlin.Int) Extended service request fails due to expiration of the T3417 EXT timer. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EPS_SERVICES_AND_NON_EPS_SERVICES_NOT_ALLOWED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#EPS_SERVICES_AND_NON_EPS_SERVICES_NOT_ALLOWED:kotlin.Int) EPS and non-EPS services are not allowed by the network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EPS_SERVICES_NOT_ALLOWED_IN_PLMN](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#EPS_SERVICES_NOT_ALLOWED_IN_PLMN:kotlin.Int) EPS services are not allowed in the PLMN. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#ERROR_UNSPECIFIED:kotlin.Int) Data call fail due to unspecific errors. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ESM_BAD_OTA_MESSAGE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#ESM_BAD_OTA_MESSAGE:kotlin.Int) Bad OTA message is received from the network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ESM_BEARER_DEACTIVATED_TO_SYNC_WITH_NETWORK](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#ESM_BEARER_DEACTIVATED_TO_SYNC_WITH_NETWORK:kotlin.Int) Bearer must be deactivated to synchronize with the network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ESM_COLLISION_SCENARIOS](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#ESM_COLLISION_SCENARIOS:kotlin.Int) Collision scenarios for the UE and network-initiated procedures. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ESM_CONTEXT_TRANSFERRED_DUE_TO_IRAT](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#ESM_CONTEXT_TRANSFERRED_DUE_TO_IRAT:kotlin.Int) PDN was disconnected by the downlaod server due to IRAT. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ESM_DOWNLOAD_SERVER_REJECTED_THE_CALL](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#ESM_DOWNLOAD_SERVER_REJECTED_THE_CALL:kotlin.Int) Download server rejected the call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ESM_FAILURE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#ESM_FAILURE:kotlin.Int) ESM level failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ESM_INFO_NOT_RECEIVED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#ESM_INFO_NOT_RECEIVED:kotlin.Int) EPS Session Management (ESM) information is not received. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ESM_LOCAL_CAUSE_NONE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#ESM_LOCAL_CAUSE_NONE:kotlin.Int) No specific local cause is mentioned, usually a valid OTA cause. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ESM_NW_ACTIVATED_DED_BEARER_WITH_ID_OF_DEF_BEARER](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#ESM_NW_ACTIVATED_DED_BEARER_WITH_ID_OF_DEF_BEARER:kotlin.Int) Active dedicated bearer was requested for an existing default bearer. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ESM_PROCEDURE_TIME_OUT](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#ESM_PROCEDURE_TIME_OUT:kotlin.Int) ESM procedure maximum attempt timeout failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ESM_UNKNOWN_EPS_BEARER_CONTEXT](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#ESM_UNKNOWN_EPS_BEARER_CONTEXT:kotlin.Int) Invalid EPS bearer identity in the request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVDO_CONNECTION_DENY_BY_BILLING_OR_AUTHENTICATION_FAILURE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#EVDO_CONNECTION_DENY_BY_BILLING_OR_AUTHENTICATION_FAILURE:kotlin.Int) Received a connection deny due to billing or authentication failure on EVDO network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVDO_CONNECTION_DENY_BY_GENERAL_OR_NETWORK_BUSY](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#EVDO_CONNECTION_DENY_BY_GENERAL_OR_NETWORK_BUSY:kotlin.Int) Received a connection deny due to general or network busy on EVDO network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVDO_HDR_CHANGED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#EVDO_HDR_CHANGED:kotlin.Int) HDR system has been changed due to redirection or the PRL was not preferred. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVDO_HDR_CONNECTION_SETUP_TIMEOUT](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#EVDO_HDR_CONNECTION_SETUP_TIMEOUT:kotlin.Int) Connection setup on the HDR system was time out. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVDO_HDR_EXITED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#EVDO_HDR_EXITED:kotlin.Int) Device exited HDR due to redirection or the PRL was not preferred. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVDO_HDR_NO_SESSION](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#EVDO_HDR_NO_SESSION:kotlin.Int) Device does not have an HDR session. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVDO_USING_GPS_FIX_INSTEAD_OF_HDR_CALL](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#EVDO_USING_GPS_FIX_INSTEAD_OF_HDR_CALL:kotlin.Int) It is ending an HDR call origination in favor of a GPS fix. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FADE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#FADE:kotlin.Int) Device lost the system due to fade. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FAILED_TO_ACQUIRE_COLOCATED_HDR](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#FAILED_TO_ACQUIRE_COLOCATED_HDR:kotlin.Int) Device failed to acquire a co-located HDR for origination. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FEATURE_NOT_SUPP](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#FEATURE_NOT_SUPP:kotlin.Int) Feature not supported. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FILTER_SEMANTIC_ERROR](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#FILTER_SEMANTIC_ERROR:kotlin.Int) Semantic errors in packet filter. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FILTER_SYTAX_ERROR](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#FILTER_SYTAX_ERROR:kotlin.Int) Syntactical errors in packet filter(s). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORBIDDEN_APN_NAME](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#FORBIDDEN_APN_NAME:kotlin.Int) PDN being brought up with an APN that is part of forbidden APN Name list. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GPRS_REGISTRATION_FAIL](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#GPRS_REGISTRATION_FAIL:kotlin.Int) Data fail due to GPRS registration failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GPRS_SERVICES_AND_NON_GPRS_SERVICES_NOT_ALLOWED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#GPRS_SERVICES_AND_NON_GPRS_SERVICES_NOT_ALLOWED:kotlin.Int) Not allowed to operate either GPRS or non-GPRS services. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GPRS_SERVICES_NOT_ALLOWED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#GPRS_SERVICES_NOT_ALLOWED:kotlin.Int) MS is not allowed to operate GPRS services. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GPRS_SERVICES_NOT_ALLOWED_IN_THIS_PLMN](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#GPRS_SERVICES_NOT_ALLOWED_IN_THIS_PLMN:kotlin.Int) UE requests GPRS service or the network initiates a detach request in a PLMN that does not offer roaming for GPRS services. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HANDOFF_PREFERENCE_CHANGED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#HANDOFF_PREFERENCE_CHANGED:kotlin.Int) System preference change back to SRAT during handoff |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HDR_ACCESS_FAILURE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#HDR_ACCESS_FAILURE:kotlin.Int) HDR system access failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HDR_FADE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#HDR_FADE:kotlin.Int) HDR module released the call due to fade. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HDR_NO_LOCK_GRANTED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#HDR_NO_LOCK_GRANTED:kotlin.Int) HDR module could not be obtained because of the RF locked. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IFACE_AND_POL_FAMILY_MISMATCH](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#IFACE_AND_POL_FAMILY_MISMATCH:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IFACE_MISMATCH](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#IFACE_MISMATCH:kotlin.Int) Interface mismatch. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ILLEGAL_ME](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#ILLEGAL_ME:kotlin.Int) ME could not be authenticated and the ME used is not acceptable to the network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ILLEGAL_MS](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#ILLEGAL_MS:kotlin.Int) Network refuses service to the MS because either an identity of the MS is not acceptable to the network or the MS does not pass the authentication check. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IMEI_NOT_ACCEPTED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#IMEI_NOT_ACCEPTED:kotlin.Int) IMEI of the UE is not accepted by the network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IMPLICITLY_DETACHED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#IMPLICITLY_DETACHED:kotlin.Int) Mobile reachable timer has expired, or the GMM context data related to the subscription does not exist in the SGSN. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IMSI_UNKNOWN_IN_HOME_SUBSCRIBER_SERVER](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#IMSI_UNKNOWN_IN_HOME_SUBSCRIBER_SERVER:kotlin.Int) IMSI present in the UE is unknown in the home subscriber server. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INCOMING_CALL_REJECTED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#INCOMING_CALL_REJECTED:kotlin.Int) The other clients rejected incoming call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INSUFFICIENT_RESOURCES](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#INSUFFICIENT_RESOURCES:kotlin.Int) Insufficient resources. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INTERFACE_IN_USE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#INTERFACE_IN_USE:kotlin.Int) The current interface is being in use. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INTERNAL_CALL_PREEMPT_BY_HIGH_PRIO_APN](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#INTERNAL_CALL_PREEMPT_BY_HIGH_PRIO_APN:kotlin.Int) Internal data call preempt by high priority APN. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INTERNAL_EPC_NONEPC_TRANSITION](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#INTERNAL_EPC_NONEPC_TRANSITION:kotlin.Int) Rejected/Brought down since UE is transition between EPC and NONEPC RAT. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INVALID_CONNECTION_ID](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#INVALID_CONNECTION_ID:kotlin.Int) No PDP exists with the given connection ID while modifying or deactivating or activation for an already active PDP. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INVALID_DNS_ADDR](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#INVALID_DNS_ADDR:kotlin.Int) Not receiving a DNS address that was mandatory. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INVALID_EMM_STATE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#INVALID_EMM_STATE:kotlin.Int) Invalid EMM state. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INVALID_MANDATORY_INFO](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#INVALID_MANDATORY_INFO:kotlin.Int) Invalid mandatory information. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INVALID_MODE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#INVALID_MODE:kotlin.Int) Device operational mode is different from the mode requested in the traffic channel bring up. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INVALID_PCSCF_ADDR](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#INVALID_PCSCF_ADDR:kotlin.Int) Invalid Proxy-Call Session Control Function (P-CSCF) address. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INVALID_PCSCF_OR_DNS_ADDRESS](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#INVALID_PCSCF_OR_DNS_ADDRESS:kotlin.Int) Not receiving either a PCSCF or a DNS address, one of them being mandatory. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INVALID_PRIMARY_NSAPI](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#INVALID_PRIMARY_NSAPI:kotlin.Int) Primary context for NSAPI does not exist. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INVALID_SIM_STATE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#INVALID_SIM_STATE:kotlin.Int) SIM was marked by the network as invalid for the circuit and/or packet service domain. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INVALID_TRANSACTION_ID](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#INVALID_TRANSACTION_ID:kotlin.Int) Invalid transaction id. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IPV6_ADDRESS_TRANSFER_FAILED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#IPV6_ADDRESS_TRANSFER_FAILED:kotlin.Int) IPv6 address transfer failed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IPV6_PREFIX_UNAVAILABLE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#IPV6_PREFIX_UNAVAILABLE:kotlin.Int) Device failure to obtain the prefix from the network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IP_ADDRESS_MISMATCH](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#IP_ADDRESS_MISMATCH:kotlin.Int) IP address mismatch. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IP_VERSION_MISMATCH](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#IP_VERSION_MISMATCH:kotlin.Int) New call bring up is rejected since the existing data call IP type doesn't match the requested IP. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IRAT_HANDOVER_FAILED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#IRAT_HANDOVER_FAILED:kotlin.Int) Data call was unsuccessfully transferred during the IRAT handover. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IS707B_MAX_ACCESS_PROBES](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#IS707B_MAX_ACCESS_PROBES:kotlin.Int) Maximum access probes for the IS-707B call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IWLAN_AUTHORIZATION_REJECTED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#IWLAN_AUTHORIZATION_REJECTED:kotlin.Int) The user is barred from using the non-3GPP access or the subscribed APN. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IWLAN_CONGESTION](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#IWLAN_CONGESTION:kotlin.Int) The requested service was rejected because of congestion in the network while accessing the IWLAN ePDG. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IWLAN_DNS_RESOLUTION_NAME_FAILURE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#IWLAN_DNS_RESOLUTION_NAME_FAILURE:kotlin.Int) Unable to resolve FQDN for the ePDG to an IP address |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IWLAN_DNS_RESOLUTION_TIMEOUT](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#IWLAN_DNS_RESOLUTION_TIMEOUT:kotlin.Int) No response received from the DNS Server due to a timeout |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IWLAN_IKEV2_AUTH_FAILURE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#IWLAN_IKEV2_AUTH_FAILURE:kotlin.Int) Sent in the response to an IKE_AUTH message when, for some reason, the authentication failed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IWLAN_IKEV2_CERT_INVALID](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#IWLAN_IKEV2_CERT_INVALID:kotlin.Int) IKE Certification validation failure |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IWLAN_IKEV2_CONFIG_FAILURE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#IWLAN_IKEV2_CONFIG_FAILURE:kotlin.Int) IKE configuration error resulting in failure |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IWLAN_IKEV2_MSG_TIMEOUT](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#IWLAN_IKEV2_MSG_TIMEOUT:kotlin.Int) IKE message timeout, tunnel setup failed due to no response from EPDG |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IWLAN_ILLEGAL_ME](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#IWLAN_ILLEGAL_ME:kotlin.Int) The Mobile Equipment used is not acceptable to the network |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IWLAN_IMEI_NOT_ACCEPTED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#IWLAN_IMEI_NOT_ACCEPTED:kotlin.Int) The network does not accept emergency PDN bringup request using an IMEI |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IWLAN_MAX_CONNECTION_REACHED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#IWLAN_MAX_CONNECTION_REACHED:kotlin.Int) The PDN connection has been rejected. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IWLAN_NETWORK_FAILURE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#IWLAN_NETWORK_FAILURE:kotlin.Int) The network has determined that the requested procedure cannot be completed successfully due to network failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IWLAN_NON_3GPP_ACCESS_TO_EPC_NOT_ALLOWED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#IWLAN_NON_3GPP_ACCESS_TO_EPC_NOT_ALLOWED:kotlin.Int) No non-3GPP subscription is associated with the IMSI. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IWLAN_NO_APN_SUBSCRIPTION](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#IWLAN_NO_APN_SUBSCRIPTION:kotlin.Int) The requested APN is not included in the user's profile, and therefore is not authorized for that user. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IWLAN_PDN_CONNECTION_REJECTION](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#IWLAN_PDN_CONNECTION_REJECTION:kotlin.Int) The PDN connection corresponding to the requested APN has been rejected. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IWLAN_PLMN_NOT_ALLOWED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#IWLAN_PLMN_NOT_ALLOWED:kotlin.Int) The ePDG performs PLMN filtering (based on roaming agreements) and rejects the request from the UE. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IWLAN_RAT_TYPE_NOT_ALLOWED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#IWLAN_RAT_TYPE_NOT_ALLOWED:kotlin.Int) The access type is restricted to the user. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IWLAN_SEMANTIC_ERRORS_IN_PACKET_FILTERS](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#IWLAN_SEMANTIC_ERRORS_IN_PACKET_FILTERS:kotlin.Int) The PDN connection has been rejected due to sematic errors in the packet filter. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IWLAN_SEMANTIC_ERROR_IN_THE_TFT_OPERATION](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#IWLAN_SEMANTIC_ERROR_IN_THE_TFT_OPERATION:kotlin.Int) The PDN connection has been rejected due to a semantic error in TFT operation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IWLAN_SYNTACTICAL_ERRORS_IN_PACKET_FILTERS](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#IWLAN_SYNTACTICAL_ERRORS_IN_PACKET_FILTERS:kotlin.Int) The PDN connection has been rejected due to syntactic errors in the packet filter. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IWLAN_SYNTACTICAL_ERROR_IN_THE_TFT_OPERATION](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#IWLAN_SYNTACTICAL_ERROR_IN_THE_TFT_OPERATION:kotlin.Int) The PDN connection has been rejected due to a syntactic error in TFT operation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IWLAN_TUNNEL_NOT_FOUND](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#IWLAN_TUNNEL_NOT_FOUND:kotlin.Int) Expected to update or bring down an ePDG tunnel, but no tunnel found |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IWLAN_UNAUTHENTICATED_EMERGENCY_NOT_SUPPORTED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#IWLAN_UNAUTHENTICATED_EMERGENCY_NOT_SUPPORTED:kotlin.Int) The ePDG does not support un-authenticated IMSI based emergency PDN bringup \* |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IWLAN_USER_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#IWLAN_USER_UNKNOWN:kotlin.Int) The user identified by the IMSI is unknown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LIMITED_TO_IPV4](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#LIMITED_TO_IPV4:kotlin.Int) IPv6 interface bring up fails because the network provided only the IPv4 address for the upcoming PDN permanent client can reattempt a IPv6 call bring up after the IPv4 interface is also brought down. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LIMITED_TO_IPV6](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#LIMITED_TO_IPV6:kotlin.Int) IPv4 interface bring up fails because the network provided only the IPv6 address for the upcoming PDN permanent client can reattempt a IPv4 call bring up after the IPv6 interface is also brought down. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LLC_SNDCP](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#LLC_SNDCP:kotlin.Int) Logical Link Control (LLC) Sub Network Dependent Convergence Protocol (SNDCP). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCAL_END](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#LOCAL_END:kotlin.Int) Client ended the data call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCATION_AREA_NOT_ALLOWED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#LOCATION_AREA_NOT_ALLOWED:kotlin.Int) MS requests service, or the network initiates a detach request, in a location area where the HPLMN determines that the MS, by subscription, is not allowed to operate. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOST_CONNECTION](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#LOST_CONNECTION:kotlin.Int) Data connection was lost. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOWER_LAYER_REGISTRATION_FAILURE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#LOWER_LAYER_REGISTRATION_FAILURE:kotlin.Int) Lower layer registration failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOW_POWER_MODE_OR_POWERING_DOWN](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#LOW_POWER_MODE_OR_POWERING_DOWN:kotlin.Int) Device is going into lower power mode or powering down. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LTE_NAS_SERVICE_REQUEST_FAILED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#LTE_NAS_SERVICE_REQUEST_FAILED:kotlin.Int) Service request procedure failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LTE_THROTTLING_NOT_REQUIRED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#LTE_THROTTLING_NOT_REQUIRED:kotlin.Int) Throttling is not needed for this service request failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAC_FAILURE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MAC_FAILURE:kotlin.Int) MAC level failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MATCH_ALL_RULE_NOT_ALLOWED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MATCH_ALL_RULE_NOT_ALLOWED:kotlin.Int) No matching rule available for the request, and match-all rule is not allowed for it. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAXIMIUM_NSAPIS_EXCEEDED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MAXIMIUM_NSAPIS_EXCEEDED:kotlin.Int) Maximum NSAPIs have been exceeded during PDP activation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAXINUM_SIZE_OF_L2_MESSAGE_EXCEEDED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MAXINUM_SIZE_OF_L2_MESSAGE_EXCEEDED:kotlin.Int) Maximum size of the L2 message was exceeded. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAX_ACCESS_PROBE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MAX_ACCESS_PROBE:kotlin.Int) Maximum access probes transmitted. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAX_IPV4_CONNECTIONS](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MAX_IPV4_CONNECTIONS:kotlin.Int) IPv4 data call bring up is rejected because the UE already maintains the allotted maximum number of IPv4 data connections. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAX_IPV6_CONNECTIONS](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MAX_IPV6_CONNECTIONS:kotlin.Int) IPv6 data call bring up is rejected because the UE already maintains the allotted maximum number of IPv6 data connections. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAX_PPP_INACTIVITY_TIMER_EXPIRED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MAX_PPP_INACTIVITY_TIMER_EXPIRED:kotlin.Int) Maximum PPP inactivity timer expired. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MESSAGE_INCORRECT_SEMANTIC](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MESSAGE_INCORRECT_SEMANTIC:kotlin.Int) Incorrect message semantic. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MESSAGE_TYPE_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MESSAGE_TYPE_UNSUPPORTED:kotlin.Int) Unsupported message type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIP_CONFIG_FAILURE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MIP_CONFIG_FAILURE:kotlin.Int) UE is in MIP-only configuration but the MIP configuration fails on call bring up due to incorrect provisioning. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIP_FA_ADMIN_PROHIBITED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MIP_FA_ADMIN_PROHIBITED:kotlin.Int) Foreign agent administratively prohibited MIP (Mobile IP) registration. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIP_FA_DELIVERY_STYLE_NOT_SUPPORTED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MIP_FA_DELIVERY_STYLE_NOT_SUPPORTED:kotlin.Int) Foreign agent rejected MIP (Mobile IP) registration because of delivery style was not supported. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIP_FA_ENCAPSULATION_UNAVAILABLE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MIP_FA_ENCAPSULATION_UNAVAILABLE:kotlin.Int) Foreign agent rejected MIP (Mobile IP) registration because of requested encapsulation was unavailable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIP_FA_HOME_AGENT_AUTHENTICATION_FAILURE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MIP_FA_HOME_AGENT_AUTHENTICATION_FAILURE:kotlin.Int) Foreign agent rejected MIP (Mobile IP) registration because of home agent authentication failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIP_FA_INSUFFICIENT_RESOURCES](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MIP_FA_INSUFFICIENT_RESOURCES:kotlin.Int) Foreign agent rejected MIP (Mobile IP) registration because of insufficient resources. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIP_FA_MALFORMED_REPLY](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MIP_FA_MALFORMED_REPLY:kotlin.Int) Foreign agent rejected MIP (Mobile IP) registration because of malformed reply. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIP_FA_MALFORMED_REQUEST](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MIP_FA_MALFORMED_REQUEST:kotlin.Int) Foreign agent rejected MIP (Mobile IP) registration because of malformed request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIP_FA_MISSING_CHALLENGE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MIP_FA_MISSING_CHALLENGE:kotlin.Int) Foreign agent rejected MIP (Mobile IP) registration because of missing challenge. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIP_FA_MISSING_HOME_ADDRESS](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MIP_FA_MISSING_HOME_ADDRESS:kotlin.Int) Foreign agent rejected MIP (Mobile IP) registration because of missing Home Address. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIP_FA_MISSING_HOME_AGENT](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MIP_FA_MISSING_HOME_AGENT:kotlin.Int) Foreign agent rejected MIP (Mobile IP) registration because of missing Home Agent. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIP_FA_MISSING_NAI](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MIP_FA_MISSING_NAI:kotlin.Int) Foreign agent rejected MIP (Mobile IP) registration because of missing NAI (Network Access Identifier). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIP_FA_MOBILE_NODE_AUTHENTICATION_FAILURE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MIP_FA_MOBILE_NODE_AUTHENTICATION_FAILURE:kotlin.Int) Foreign agent rejected MIP (Mobile IP) registration because of MN-AAA authenticator was wrong. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIP_FA_REASON_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MIP_FA_REASON_UNSPECIFIED:kotlin.Int) Reason unspecified for foreign agent rejected MIP (Mobile IP) registration. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIP_FA_REQUESTED_LIFETIME_TOO_LONG](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MIP_FA_REQUESTED_LIFETIME_TOO_LONG:kotlin.Int) Foreign agent rejected MIP (Mobile IP) registration because of requested lifetime was too long. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIP_FA_REVERSE_TUNNEL_IS_MANDATORY](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MIP_FA_REVERSE_TUNNEL_IS_MANDATORY:kotlin.Int) Foreign agent rejected MIP (Mobile IP) registration because of reverse tunnel was mandatory but not requested by device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIP_FA_REVERSE_TUNNEL_UNAVAILABLE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MIP_FA_REVERSE_TUNNEL_UNAVAILABLE:kotlin.Int) Foreign agent rejected MIP (Mobile IP) registration because of reverse tunnel was unavailable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIP_FA_STALE_CHALLENGE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MIP_FA_STALE_CHALLENGE:kotlin.Int) Foreign agent rejected MIP (Mobile IP) registration because of stale challenge. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIP_FA_UNKNOWN_CHALLENGE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MIP_FA_UNKNOWN_CHALLENGE:kotlin.Int) Foreign agent rejected MIP (Mobile IP) registration because of unknown challenge. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIP_FA_VJ_HEADER_COMPRESSION_UNAVAILABLE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MIP_FA_VJ_HEADER_COMPRESSION_UNAVAILABLE:kotlin.Int) Foreign agent rejected MIP (Mobile IP) registration of VJ Header Compression was unavailable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIP_HA_ADMIN_PROHIBITED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MIP_HA_ADMIN_PROHIBITED:kotlin.Int) Home agent administratively prohibited MIP (Mobile IP) registration. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIP_HA_ENCAPSULATION_UNAVAILABLE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MIP_HA_ENCAPSULATION_UNAVAILABLE:kotlin.Int) Home agent rejected MIP (Mobile IP) registration because of encapsulation unavailable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIP_HA_FOREIGN_AGENT_AUTHENTICATION_FAILURE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MIP_HA_FOREIGN_AGENT_AUTHENTICATION_FAILURE:kotlin.Int) Home agent rejected MIP (Mobile IP) registration because of foreign agent authentication failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIP_HA_INSUFFICIENT_RESOURCES](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MIP_HA_INSUFFICIENT_RESOURCES:kotlin.Int) Home agent rejected MIP (Mobile IP) registration because of insufficient resources. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIP_HA_MALFORMED_REQUEST](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MIP_HA_MALFORMED_REQUEST:kotlin.Int) Home agent rejected MIP (Mobile IP) registration because of malformed request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIP_HA_MOBILE_NODE_AUTHENTICATION_FAILURE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MIP_HA_MOBILE_NODE_AUTHENTICATION_FAILURE:kotlin.Int) Home agent rejected MIP (Mobile IP) registration because of MN-HA authenticator was wrong. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIP_HA_REASON_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MIP_HA_REASON_UNSPECIFIED:kotlin.Int) Reason unspecified for home agent rejected MIP (Mobile IP) registration. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIP_HA_REGISTRATION_ID_MISMATCH](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MIP_HA_REGISTRATION_ID_MISMATCH:kotlin.Int) Home agent rejected MIP (Mobile IP) registration because of registration id mismatch. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIP_HA_REVERSE_TUNNEL_IS_MANDATORY](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MIP_HA_REVERSE_TUNNEL_IS_MANDATORY:kotlin.Int) Home agent rejected MIP (Mobile IP) registration because of reverse tunnel is mandatory but not requested by device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIP_HA_REVERSE_TUNNEL_UNAVAILABLE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MIP_HA_REVERSE_TUNNEL_UNAVAILABLE:kotlin.Int) Home agent rejected MIP (Mobile IP) registration because of reverse tunnel was unavailable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIP_HA_UNKNOWN_HOME_AGENT_ADDRESS](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MIP_HA_UNKNOWN_HOME_AGENT_ADDRESS:kotlin.Int) Home agent rejected MIP (Mobile IP) registration because of unknown home agent address. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MISSING_UNKNOWN_APN](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MISSING_UNKNOWN_APN:kotlin.Int) Missing or unknown APN. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODEM_APP_PREEMPTED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MODEM_APP_PREEMPTED:kotlin.Int) Another application in modem preempts the data call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODEM_RESTART](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MODEM_RESTART:kotlin.Int) Modem restart. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MSC_TEMPORARILY_NOT_REACHABLE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MSC_TEMPORARILY_NOT_REACHABLE:kotlin.Int) Mobile switching center is temporarily unreachable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MSG_AND_PROTOCOL_STATE_UNCOMPATIBLE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MSG_AND_PROTOCOL_STATE_UNCOMPATIBLE:kotlin.Int) Message and protocol state uncompatible. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MSG_TYPE_NONCOMPATIBLE_STATE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MSG_TYPE_NONCOMPATIBLE_STATE:kotlin.Int) Message type uncompatible. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MS_IDENTITY_CANNOT_BE_DERIVED_BY_THE_NETWORK](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MS_IDENTITY_CANNOT_BE_DERIVED_BY_THE_NETWORK:kotlin.Int) No matching identity or context could be found in the network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MULTIPLE_PDP_CALL_NOT_ALLOWED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MULTIPLE_PDP_CALL_NOT_ALLOWED:kotlin.Int) Multiple PDP call feature is disabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MULTI_CONN_TO_SAME_PDN_NOT_ALLOWED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#MULTI_CONN_TO_SAME_PDN_NOT_ALLOWED:kotlin.Int) Multiple connections to a same PDN is not allowed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NAS_LAYER_FAILURE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#NAS_LAYER_FAILURE:kotlin.Int) Non-Access Spectrum layer failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NAS_REQUEST_REJECTED_BY_NETWORK](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#NAS_REQUEST_REJECTED_BY_NETWORK:kotlin.Int) Non-access stratum (NAS) request was rejected by the network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NAS_SIGNALLING](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#NAS_SIGNALLING:kotlin.Int) NAS signalling. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NETWORK_FAILURE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#NETWORK_FAILURE:kotlin.Int) Network Failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NETWORK_INITIATED_DETACH_NO_AUTO_REATTACH](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#NETWORK_INITIATED_DETACH_NO_AUTO_REATTACH:kotlin.Int) Network-initiated detach without reattach. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NETWORK_INITIATED_DETACH_WITH_AUTO_REATTACH](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#NETWORK_INITIATED_DETACH_WITH_AUTO_REATTACH:kotlin.Int) Network-initiated detach with reattach. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NETWORK_INITIATED_TERMINATION](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#NETWORK_INITIATED_TERMINATION:kotlin.Int) Brought down by the network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NONE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#NONE:kotlin.Int) There is no failure |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NON_IP_NOT_SUPPORTED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#NON_IP_NOT_SUPPORTED:kotlin.Int) UE is unable to bring up a non-IP data call because the device is not camped on a NB1 cell. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NORMAL_RELEASE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#NORMAL_RELEASE:kotlin.Int) Receiving a release from the base station with no reason. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NO_CDMA_SERVICE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#NO_CDMA_SERVICE:kotlin.Int) Device does not have CDMA service. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NO_COLLOCATED_HDR](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#NO_COLLOCATED_HDR:kotlin.Int) There is no co-located HDR. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NO_EPS_BEARER_CONTEXT_ACTIVATED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#NO_EPS_BEARER_CONTEXT_ACTIVATED:kotlin.Int) No EPS bearer context was activated. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NO_GPRS_CONTEXT](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#NO_GPRS_CONTEXT:kotlin.Int) GPRS context is not available. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NO_HYBRID_HDR_SERVICE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#NO_HYBRID_HDR_SERVICE:kotlin.Int) Device has no hybrid HDR service. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NO_PDP_CONTEXT_ACTIVATED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#NO_PDP_CONTEXT_ACTIVATED:kotlin.Int) MS requests an establishment of the radio access bearers for all active PDP contexts by sending a service request message indicating data to the network, but the SGSN does not have any active PDP context. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NO_RESPONSE_FROM_BASE_STATION](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#NO_RESPONSE_FROM_BASE_STATION:kotlin.Int) There was no response received from the base station. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NO_SERVICE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#NO_SERVICE:kotlin.Int) Device has no service. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NO_SERVICE_ON_GATEWAY](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#NO_SERVICE_ON_GATEWAY:kotlin.Int) No service on the gateway. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NSAPI_IN_USE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#NSAPI_IN_USE:kotlin.Int) The Network Service Access Point Identifier (NSAPI) is in use. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NULL_APN_DISALLOWED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#NULL_APN_DISALLOWED:kotlin.Int) PDN is attempted to be brought up with NULL APN but NULL APN is not supported. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OEM_DCFAILCAUSE_1](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#OEM_DCFAILCAUSE_1:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OEM_DCFAILCAUSE_10](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#OEM_DCFAILCAUSE_10:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OEM_DCFAILCAUSE_11](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#OEM_DCFAILCAUSE_11:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OEM_DCFAILCAUSE_12](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#OEM_DCFAILCAUSE_12:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OEM_DCFAILCAUSE_13](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#OEM_DCFAILCAUSE_13:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OEM_DCFAILCAUSE_14](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#OEM_DCFAILCAUSE_14:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OEM_DCFAILCAUSE_15](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#OEM_DCFAILCAUSE_15:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OEM_DCFAILCAUSE_2](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#OEM_DCFAILCAUSE_2:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OEM_DCFAILCAUSE_3](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#OEM_DCFAILCAUSE_3:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OEM_DCFAILCAUSE_4](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#OEM_DCFAILCAUSE_4:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OEM_DCFAILCAUSE_5](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#OEM_DCFAILCAUSE_5:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OEM_DCFAILCAUSE_6](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#OEM_DCFAILCAUSE_6:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OEM_DCFAILCAUSE_7](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#OEM_DCFAILCAUSE_7:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OEM_DCFAILCAUSE_8](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#OEM_DCFAILCAUSE_8:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OEM_DCFAILCAUSE_9](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#OEM_DCFAILCAUSE_9:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ONLY_IPV4V6_ALLOWED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#ONLY_IPV4V6_ALLOWED:kotlin.Int) Network supports IPv4v6 PDP type only. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ONLY_IPV4_ALLOWED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#ONLY_IPV4_ALLOWED:kotlin.Int) Packet Data Protocol (PDP) type IPv4 only allowed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ONLY_IPV6_ALLOWED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#ONLY_IPV6_ALLOWED:kotlin.Int) Packet Data Protocol (PDP) type IPv6 only allowed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ONLY_NON_IP_ALLOWED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#ONLY_NON_IP_ALLOWED:kotlin.Int) Network supports non-IP PDP type only. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ONLY_SINGLE_BEARER_ALLOWED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#ONLY_SINGLE_BEARER_ALLOWED:kotlin.Int) Single address bearers only allowed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OPERATOR_BARRED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#OPERATOR_BARRED:kotlin.Int) Operator determined barring. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OTASP_COMMIT_IN_PROGRESS](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#OTASP_COMMIT_IN_PROGRESS:kotlin.Int) OTASP commit is in progress. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PDN_CONN_DOES_NOT_EXIST](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#PDN_CONN_DOES_NOT_EXIST:kotlin.Int) PDN connection does not exist. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PDN_INACTIVITY_TIMER_EXPIRED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#PDN_INACTIVITY_TIMER_EXPIRED:kotlin.Int) PDN inactivity timer expired due to no data transmission in a configurable duration of time. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PDN_IPV4_CALL_DISALLOWED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#PDN_IPV4_CALL_DISALLOWED:kotlin.Int) IPV4 PDN is in throttled state due to network providing only IPV6 address during the previous VSNCP bringup (subs_limited_to_v6). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PDN_IPV4_CALL_THROTTLED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#PDN_IPV4_CALL_THROTTLED:kotlin.Int) IPV4 PDN is in throttled state due to previous VSNCP bringup failure(s). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PDN_IPV6_CALL_DISALLOWED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#PDN_IPV6_CALL_DISALLOWED:kotlin.Int) IPV6 PDN is in throttled state due to network providing only IPV4 address during the previous VSNCP bringup (subs_limited_to_v4). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PDN_IPV6_CALL_THROTTLED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#PDN_IPV6_CALL_THROTTLED:kotlin.Int) IPV6 PDN is in throttled state due to previous VSNCP bringup failure(s). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PDN_NON_IP_CALL_DISALLOWED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#PDN_NON_IP_CALL_DISALLOWED:kotlin.Int) Non-IP PDN is in disallowed state due to the network providing only an IP address. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PDN_NON_IP_CALL_THROTTLED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#PDN_NON_IP_CALL_THROTTLED:kotlin.Int) Non-IP PDN is in throttled state due to previous VSNCP bringup failure(s). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PDP_ACTIVATE_MAX_RETRY_FAILED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#PDP_ACTIVATE_MAX_RETRY_FAILED:kotlin.Int) SM attempts PDP activation for a maximum of four attempts. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PDP_DUPLICATE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#PDP_DUPLICATE:kotlin.Int) PDP context already exists. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PDP_ESTABLISH_TIMEOUT_EXPIRED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#PDP_ESTABLISH_TIMEOUT_EXPIRED:kotlin.Int) Expiration of the PDP establish timer with a maximum of five retries. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PDP_INACTIVE_TIMEOUT_EXPIRED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#PDP_INACTIVE_TIMEOUT_EXPIRED:kotlin.Int) Expiration of the PDP deactivate timer with a maximum of four retries. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PDP_LOWERLAYER_ERROR](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#PDP_LOWERLAYER_ERROR:kotlin.Int) PDP activation failed due to RRC_ABORT or a forbidden PLMN. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PDP_MODIFY_COLLISION](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#PDP_MODIFY_COLLISION:kotlin.Int) MO PDP modify collision when the MT PDP is already in progress. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PDP_MODIFY_TIMEOUT_EXPIRED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#PDP_MODIFY_TIMEOUT_EXPIRED:kotlin.Int) Expiration of the PDP modify timer with a maximum of four retries. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PDP_PPP_NOT_SUPPORTED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#PDP_PPP_NOT_SUPPORTED:kotlin.Int) PDP PPP calls are not supported. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PDP_WITHOUT_ACTIVE_TFT](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#PDP_WITHOUT_ACTIVE_TFT:kotlin.Int) Packet Data Protocol (PDP) without active traffic flow template (TFT). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PHONE_IN_USE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#PHONE_IN_USE:kotlin.Int) Device is in use (e.g., voice call). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PHYSICAL_LINK_CLOSE_IN_PROGRESS](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#PHYSICAL_LINK_CLOSE_IN_PROGRESS:kotlin.Int) Physical link is in the process of cleanup. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLMN_NOT_ALLOWED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#PLMN_NOT_ALLOWED:kotlin.Int) UE requests GPRS service, or the network initiates a detach request in a PLMN which does not offer roaming for GPRS services to that MS. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PPP_AUTH_FAILURE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#PPP_AUTH_FAILURE:kotlin.Int) Data call bring up fails in the PPP setup due to an authorization failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PPP_CHAP_FAILURE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#PPP_CHAP_FAILURE:kotlin.Int) Data call bring up fails in the PPP setup due to a CHAP failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PPP_CLOSE_IN_PROGRESS](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#PPP_CLOSE_IN_PROGRESS:kotlin.Int) Data call bring up fails in the PPP setup because the PPP is in the process of cleaning the previous PPP session. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PPP_OPTION_MISMATCH](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#PPP_OPTION_MISMATCH:kotlin.Int) Data call bring up fails in the PPP setup due to an option mismatch. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PPP_PAP_FAILURE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#PPP_PAP_FAILURE:kotlin.Int) Data call bring up fails in the PPP setup due to a PAP failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PPP_TIMEOUT](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#PPP_TIMEOUT:kotlin.Int) Data call bring up fails in the PPP setup due to a timeout. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PREF_RADIO_TECH_CHANGED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#PREF_RADIO_TECH_CHANGED:kotlin.Int) Preferred technology has changed, must retry with parameters appropriate for new technology. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PROFILE_BEARER_INCOMPATIBLE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#PROFILE_BEARER_INCOMPATIBLE:kotlin.Int) APN bearer type in the profile does not match preferred network mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PROTOCOL_ERRORS](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#PROTOCOL_ERRORS:kotlin.Int) Protocol errors. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QOS_NOT_ACCEPTED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#QOS_NOT_ACCEPTED:kotlin.Int) Quality of service (QoS) is not accepted. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RADIO_ACCESS_BEARER_FAILURE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#RADIO_ACCESS_BEARER_FAILURE:kotlin.Int) Radio access bearer failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RADIO_ACCESS_BEARER_SETUP_FAILURE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#RADIO_ACCESS_BEARER_SETUP_FAILURE:kotlin.Int) Radio access bearer is not established by the lower layers during activation, modification, or deactivation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RADIO_NOT_AVAILABLE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#RADIO_NOT_AVAILABLE:kotlin.Int) Data fail due to radio not unavailable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RADIO_POWER_OFF](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#RADIO_POWER_OFF:kotlin.Int) data call was disconnected because radio was resetting, powered off. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REDIRECTION_OR_HANDOFF_IN_PROGRESS](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#REDIRECTION_OR_HANDOFF_IN_PROGRESS:kotlin.Int) Device is in the process of redirecting or handing off to a different target system. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REGISTRATION_FAIL](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#REGISTRATION_FAIL:kotlin.Int) Data fail due to registration failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REGULAR_DEACTIVATION](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#REGULAR_DEACTIVATION:kotlin.Int) Regular deactivation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REJECTED_BY_BASE_STATION](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#REJECTED_BY_BASE_STATION:kotlin.Int) The base station rejecting the call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RRC_CONNECTION_ABORTED_AFTER_HANDOVER](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#RRC_CONNECTION_ABORTED_AFTER_HANDOVER:kotlin.Int) Radio resource control (RRC) connection was aborted by the non-access stratum (NAS) after an IRAT to LTE IRAT handover. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RRC_CONNECTION_ABORTED_AFTER_IRAT_CELL_CHANGE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#RRC_CONNECTION_ABORTED_AFTER_IRAT_CELL_CHANGE:kotlin.Int) Radio resource control (RRC) connection was aborted before deactivating the LTE stack after a successful LTE to GSM/EDGE IRAT cell change order procedure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RRC_CONNECTION_ABORTED_DUE_TO_IRAT_CHANGE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#RRC_CONNECTION_ABORTED_DUE_TO_IRAT_CHANGE:kotlin.Int) Radio resource control (RRC) connection was aborted before deactivating the LTE stack due to a successful LTE to WCDMA/GSM/TD-SCDMA IRAT change. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RRC_CONNECTION_ABORTED_DURING_IRAT_CELL_CHANGE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#RRC_CONNECTION_ABORTED_DURING_IRAT_CELL_CHANGE:kotlin.Int) Radio resource control (RRC) connection was aborted in the middle of a LTE to GSM IRAT cell change order procedure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RRC_CONNECTION_ABORT_REQUEST](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#RRC_CONNECTION_ABORT_REQUEST:kotlin.Int) Connection has been released by the radio resource control (RRC) due to an abort request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RRC_CONNECTION_ACCESS_BARRED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#RRC_CONNECTION_ACCESS_BARRED:kotlin.Int) Radio resource control (RRC) connection establishment failed due to access barrred. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RRC_CONNECTION_ACCESS_STRATUM_FAILURE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#RRC_CONNECTION_ACCESS_STRATUM_FAILURE:kotlin.Int) Radio resource control (RRC) connection failure at access stratum. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RRC_CONNECTION_ANOTHER_PROCEDURE_IN_PROGRESS](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#RRC_CONNECTION_ANOTHER_PROCEDURE_IN_PROGRESS:kotlin.Int) Radio resource control (RRC) connection establishment is aborted due to another procedure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RRC_CONNECTION_CELL_NOT_CAMPED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#RRC_CONNECTION_CELL_NOT_CAMPED:kotlin.Int) Connection establishment failed as the radio resource control (RRC) is not camped on any cell. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RRC_CONNECTION_CELL_RESELECTION](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#RRC_CONNECTION_CELL_RESELECTION:kotlin.Int) Radio resource control (RRC) connection establishment failed due to cell reselection at access stratum. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RRC_CONNECTION_CONFIG_FAILURE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#RRC_CONNECTION_CONFIG_FAILURE:kotlin.Int) Connection establishment failed due to configuration failure at the radio resource control (RRC). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RRC_CONNECTION_INVALID_REQUEST](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#RRC_CONNECTION_INVALID_REQUEST:kotlin.Int) Radio resource control (RRC) connection establishment failure due to an error in the request message. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RRC_CONNECTION_LINK_FAILURE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#RRC_CONNECTION_LINK_FAILURE:kotlin.Int) Connection establishment failed due to a link failure at the radio resource control (RRC). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RRC_CONNECTION_NORMAL_RELEASE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#RRC_CONNECTION_NORMAL_RELEASE:kotlin.Int) Normal radio resource control (RRC) connection release. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RRC_CONNECTION_OUT_OF_SERVICE_DURING_CELL_REGISTER](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#RRC_CONNECTION_OUT_OF_SERVICE_DURING_CELL_REGISTER:kotlin.Int) UE is out of service during the call register. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RRC_CONNECTION_RADIO_LINK_FAILURE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#RRC_CONNECTION_RADIO_LINK_FAILURE:kotlin.Int) Radio resource control (RRC) connection release failed due to radio link failure conditions. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RRC_CONNECTION_REESTABLISHMENT_FAILURE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#RRC_CONNECTION_REESTABLISHMENT_FAILURE:kotlin.Int) Radio resource control (RRC) connection re-establishment failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RRC_CONNECTION_REJECT_BY_NETWORK](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#RRC_CONNECTION_REJECT_BY_NETWORK:kotlin.Int) Radio resource control (RRC) connection establishment failed due to the network rejecting the UE connection request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RRC_CONNECTION_RELEASED_SECURITY_NOT_ACTIVE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#RRC_CONNECTION_RELEASED_SECURITY_NOT_ACTIVE:kotlin.Int) If the UE has an LTE radio link failure before security is established, the radio resource control (RRC) connection must be released and the UE must return to idle. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RRC_CONNECTION_RF_UNAVAILABLE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#RRC_CONNECTION_RF_UNAVAILABLE:kotlin.Int) Radio resource control (RRC) connection establishment failure due to the RF was unavailable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RRC_CONNECTION_SYSTEM_INFORMATION_BLOCK_READ_ERROR](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#RRC_CONNECTION_SYSTEM_INFORMATION_BLOCK_READ_ERROR:kotlin.Int) Radio resource control (RRC) connection released due to a system information block read error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RRC_CONNECTION_SYSTEM_INTERVAL_FAILURE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#RRC_CONNECTION_SYSTEM_INTERVAL_FAILURE:kotlin.Int) Connection establishment failed due to a service interval failure at the radio resource control (RRC). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RRC_CONNECTION_TIMER_EXPIRED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#RRC_CONNECTION_TIMER_EXPIRED:kotlin.Int) Radio resource control (RRC) connection could not be established in the time limit. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RRC_CONNECTION_TRACKING_AREA_ID_CHANGED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#RRC_CONNECTION_TRACKING_AREA_ID_CHANGED:kotlin.Int) Radio resource control (RRC) connection establishment failure due to a change in the tracking area ID. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RRC_UPLINK_CONNECTION_RELEASE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#RRC_UPLINK_CONNECTION_RELEASE:kotlin.Int) Radio resource control (RRC) uplink data delivery failed due to a connection release. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RRC_UPLINK_DATA_TRANSMISSION_FAILURE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#RRC_UPLINK_DATA_TRANSMISSION_FAILURE:kotlin.Int) Transmission failure of radio resource control (RRC) uplink data. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RRC_UPLINK_DELIVERY_FAILED_DUE_TO_HANDOVER](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#RRC_UPLINK_DELIVERY_FAILED_DUE_TO_HANDOVER:kotlin.Int) Radio resource control (RRC) uplink data delivery failed due to a handover. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RRC_UPLINK_ERROR_REQUEST_FROM_NAS](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#RRC_UPLINK_ERROR_REQUEST_FROM_NAS:kotlin.Int) Radio resource control (RRC) is not connected but the non-access stratum (NAS) sends an uplink data request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RRC_UPLINK_RADIO_LINK_FAILURE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#RRC_UPLINK_RADIO_LINK_FAILURE:kotlin.Int) Radio resource control (RRC) uplink data delivery failed due to a radio link failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RUIM_NOT_PRESENT](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#RUIM_NOT_PRESENT:kotlin.Int) RUIM not being present. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_MODE_REJECTED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#SECURITY_MODE_REJECTED:kotlin.Int) Unspecified security mode reject. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SERVICE_NOT_ALLOWED_ON_PLMN](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#SERVICE_NOT_ALLOWED_ON_PLMN:kotlin.Int) Service is not allowed on the requested PLMN. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SERVICE_OPTION_NOT_SUBSCRIBED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#SERVICE_OPTION_NOT_SUBSCRIBED:kotlin.Int) Requested service option not subscribed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SERVICE_OPTION_NOT_SUPPORTED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#SERVICE_OPTION_NOT_SUPPORTED:kotlin.Int) Service option not supported. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SERVICE_OPTION_OUT_OF_ORDER](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#SERVICE_OPTION_OUT_OF_ORDER:kotlin.Int) Service option temporarily out of order. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_LOST](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#SIGNAL_LOST:kotlin.Int) Data call drop due to network/modem disconnect. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIM_CARD_CHANGED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#SIM_CARD_CHANGED:kotlin.Int) Card was refreshed or removed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SLICE_REJECTED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#SLICE_REJECTED:kotlin.Int) Data call fail due to the slice not being allowed for the data call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SYNCHRONIZATION_FAILURE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#SYNCHRONIZATION_FAILURE:kotlin.Int) Synchronization failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TEST_LOOPBACK_REGULAR_DEACTIVATION](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#TEST_LOOPBACK_REGULAR_DEACTIVATION:kotlin.Int) Test loop-back data call has been successfully brought down. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TETHERED_CALL_ACTIVE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#TETHERED_CALL_ACTIVE:kotlin.Int) Data call was disconnected by modem because tethered. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TFT_SEMANTIC_ERROR](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#TFT_SEMANTIC_ERROR:kotlin.Int) Semantic error in the Traffic flow templates (TFT) operation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TFT_SYTAX_ERROR](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#TFT_SYTAX_ERROR:kotlin.Int) Syntactical error in the Traffic flow templates (TFT) operation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [THERMAL_EMERGENCY](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#THERMAL_EMERGENCY:kotlin.Int) Put device in thermal emergency. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [THERMAL_MITIGATION](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#THERMAL_MITIGATION:kotlin.Int) Thermal level increases and causes calls to be torn down when normal mode of operation is not allowed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRAT_SWAP_FAILED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#TRAT_SWAP_FAILED:kotlin.Int) Target RAT swap failed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UE_INITIATED_DETACH_OR_DISCONNECT](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#UE_INITIATED_DETACH_OR_DISCONNECT:kotlin.Int) UE performs a detach or disconnect PDN action based on TE requirements. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UE_IS_ENTERING_POWERSAVE_MODE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#UE_IS_ENTERING_POWERSAVE_MODE:kotlin.Int) UE is entering power save mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UE_RAT_CHANGE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#UE_RAT_CHANGE:kotlin.Int) RAT change on the UE. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UE_SECURITY_CAPABILITIES_MISMATCH](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#UE_SECURITY_CAPABILITIES_MISMATCH:kotlin.Int) UE security capabilities mismatch. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UMTS_HANDOVER_TO_IWLAN](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#UMTS_HANDOVER_TO_IWLAN:kotlin.Int) UMTS interface is brought down due to handover from UMTS to iWLAN. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UMTS_REACTIVATION_REQ](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#UMTS_REACTIVATION_REQ:kotlin.Int) Universal Mobile Telecommunications System (UMTS) reactivation request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNACCEPTABLE_NETWORK_PARAMETER](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#UNACCEPTABLE_NETWORK_PARAMETER:kotlin.Int) Data fail due to unacceptable network parameter. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNACCEPTABLE_NON_EPS_AUTHENTICATION](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#UNACCEPTABLE_NON_EPS_AUTHENTICATION:kotlin.Int) Unacceptable non-EPS authentication. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#UNKNOWN:kotlin.Int) Unknown data failure cause. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNKNOWN_INFO_ELEMENT](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#UNKNOWN_INFO_ELEMENT:kotlin.Int) Unknown info element. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNKNOWN_PDP_ADDRESS_TYPE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#UNKNOWN_PDP_ADDRESS_TYPE:kotlin.Int) Unknown Packet Data Protocol (PDP) address type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNKNOWN_PDP_CONTEXT](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#UNKNOWN_PDP_CONTEXT:kotlin.Int) Unknown Packet Data Protocol (PDP) context. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNPREFERRED_RAT](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#UNPREFERRED_RAT:kotlin.Int) RAT on which the data call is attempted/connected is no longer the preferred RAT. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNSUPPORTED_1X_PREV](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#UNSUPPORTED_1X_PREV:kotlin.Int) P_rev supported by 1 base station is less than 6, which is not supported for a 1X data call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNSUPPORTED_APN_IN_CURRENT_PLMN](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#UNSUPPORTED_APN_IN_CURRENT_PLMN:kotlin.Int) Unsupported APN in current public land mobile network (PLMN). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNSUPPORTED_QCI_VALUE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#UNSUPPORTED_QCI_VALUE:kotlin.Int) QCI (QoS Class Identifier) indicated in the UE request cannot be supported. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USER_AUTHENTICATION](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#USER_AUTHENTICATION:kotlin.Int) User authentication. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VSNCP_ADMINISTRATIVELY_PROHIBITED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#VSNCP_ADMINISTRATIVELY_PROHIBITED:kotlin.Int) Data call bring up fails in the VSNCP phase due to a network rejection of the VSNCP configuration request with the reason of administratively prohibited at the HSGW. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VSNCP_APN_UNAUTHORIZED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#VSNCP_APN_UNAUTHORIZED:kotlin.Int) Data call bring up fails in the VSNCP phase due to a network rejection of the VSNCP configuration request because the requested APN is unauthorized. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VSNCP_GEN_ERROR](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#VSNCP_GEN_ERROR:kotlin.Int) Data call bring up fails in the VSNCP phase due to a general error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VSNCP_INSUFFICIENT_PARAMETERS](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#VSNCP_INSUFFICIENT_PARAMETERS:kotlin.Int) Data call bring up fails in the VSNCP phase due to a network rejection of the VSNCP configuration request with the reason of insufficient parameter. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VSNCP_NO_PDN_GATEWAY_ADDRESS](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#VSNCP_NO_PDN_GATEWAY_ADDRESS:kotlin.Int) Data call bring up fails in the VSNCP phase due to the network rejected the VSNCP configuration request due to no PDN gateway address. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VSNCP_PDN_EXISTS_FOR_THIS_APN](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#VSNCP_PDN_EXISTS_FOR_THIS_APN:kotlin.Int) Data call bring up fails in the VSNCP phase due to a network rejection of the VSNCP configuration request because the PDN exists for this APN. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VSNCP_PDN_GATEWAY_REJECT](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#VSNCP_PDN_GATEWAY_REJECT:kotlin.Int) Data call bring up fails in the VSNCP phase due to a network rejection of the VSNCP configuration request due to a PDN gateway reject. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VSNCP_PDN_GATEWAY_UNREACHABLE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#VSNCP_PDN_GATEWAY_UNREACHABLE:kotlin.Int) Data call bring up fails in the VSNCP phase due to a network rejection of the VSNCP configuration request because the PDN gateway is unreachable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VSNCP_PDN_ID_IN_USE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#VSNCP_PDN_ID_IN_USE:kotlin.Int) Data call bring up fails in the VSNCP phase due to a network rejection of PDN ID in use, or all existing PDNs are brought down with this end reason because one of the PDN bring up was rejected by the network with the reason of PDN ID in use. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VSNCP_PDN_LIMIT_EXCEEDED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#VSNCP_PDN_LIMIT_EXCEEDED:kotlin.Int) Data call bring up fails in the VSNCP phase due to a network rejection of the VSNCP configuration request because the PDN limit has been exceeded. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VSNCP_RECONNECT_NOT_ALLOWED](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#VSNCP_RECONNECT_NOT_ALLOWED:kotlin.Int) Data call bring up fails in the VSNCP phase due to a network rejection of the VSNCP configuration request with reconnect to this PDN not allowed, or an active data call is terminated by the network because reconnection to this PDN is not allowed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VSNCP_RESOURCE_UNAVAILABLE](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#VSNCP_RESOURCE_UNAVAILABLE:kotlin.Int) Data call bring up fails in the VSNCP phase due to a network rejection of the VSNCP configuration request with the reason of resource unavailable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VSNCP_SUBSCRIBER_LIMITATION](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#VSNCP_SUBSCRIBER_LIMITATION:kotlin.Int) Data call bring up fails in the VSNCP phase due to a network rejection of the VSNCP configuration request for the reason of subscriber limitation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VSNCP_TIMEOUT](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause#VSNCP_TIMEOUT:kotlin.Int) Data call bring up fails in the VSNCP phase due to a VSNCP timeout error. |

## Constants

### ACCESS_ATTEMPT_ALREADY_IN_PROGRESS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACCESS_ATTEMPT_ALREADY_IN_PROGRESS: Int
```

Access attempt is already in progress. 

 Value: 2219

### ACCESS_BLOCK

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACCESS_BLOCK: Int
```

Access blocked by the base station. 

 Value: 2087

### ACCESS_BLOCK_ALL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACCESS_BLOCK_ALL: Int
```

Access blocked by the base station for all mobile devices. 

 Value: 2088

### ACCESS_CLASS_DSAC_REJECTION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACCESS_CLASS_DSAC_REJECTION: Int
```

Access class blocking restrictions for the current camped cell. 

 Value: 2108

### ACCESS_CONTROL_LIST_CHECK_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACCESS_CONTROL_LIST_CHECK_FAILURE: Int
```

Access control list check failure at the lower layer. 

 Value: 2128

### ACTIVATION_REJECTED_BCM_VIOLATION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTIVATION_REJECTED_BCM_VIOLATION: Int
```

UE requested to modify QoS parameters or the bearer control mode, which is not compatible with the selected bearer control mode. 

 Value: 48

### ACTIVATION_REJECT_GGSN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTIVATION_REJECT_GGSN: Int
```

Activation rejected by Gateway GPRS Support Node (GGSN), Serving Gateway or PDN Gateway. 

 Value: 30

### ACTIVATION_REJECT_UNSPECIFIED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTIVATION_REJECT_UNSPECIFIED: Int
```

Activation rejected, unspecified. 

 Value: 31

### ACTIVE_PDP_CONTEXT_MAX_NUMBER_REACHED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTIVE_PDP_CONTEXT_MAX_NUMBER_REACHED: Int
```

Max number of Packet Data Protocol (PDP) context reached. 

 Value: 65

### ALL_MATCHING_RULES_FAILED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALL_MATCHING_RULES_FAILED: Int
```

If connection failed for all matching URSP rules. 

 Value: 2254

### APN_DISABLED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APN_DISABLED: Int
```

APN has been disabled. 

 Value: 2045

### APN_DISALLOWED_ON_ROAMING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APN_DISALLOWED_ON_ROAMING: Int
```

PDN connection to the APN is disallowed on the roaming network. 

 Value: 2059

### APN_MISMATCH

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APN_MISMATCH: Int
```

New PDN bring up is rejected during interface selection because the UE has already allotted the available interfaces for other PDNs. 

 Value: 2054

### APN_PARAMETERS_CHANGED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APN_PARAMETERS_CHANGED: Int
```

APN-related parameters are changed. 

 Value: 2060

### APN_PENDING_HANDOVER

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APN_PENDING_HANDOVER: Int
```

Interface bring up is attempted for an APN that is yet to be handed over to target RAT. 

 Value: 2041

### APN_TYPE_CONFLICT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APN_TYPE_CONFLICT: Int
```

APN type conflict. 

 Value: 112

### AUTH_FAILURE_ON_EMERGENCY_CALL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AUTH_FAILURE_ON_EMERGENCY_CALL: Int
```

Authentication failure on emergency call. 

 Value: 122

### BEARER_HANDLING_NOT_SUPPORTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BEARER_HANDLING_NOT_SUPPORTED: Int
```

Procedure requested by the UE was rejected because the bearer handling is not supported. 

 Value: 60

### CALL_DISALLOWED_IN_ROAMING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CALL_DISALLOWED_IN_ROAMING: Int
```

Roaming is disallowed during call bring up. 

 Value: 2068

### CALL_PREEMPT_BY_EMERGENCY_APN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CALL_PREEMPT_BY_EMERGENCY_APN: Int
```

Emergency call bring up on a different ePDG. 

 Value: 127

### CANNOT_ENCODE_OTA_MESSAGE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CANNOT_ENCODE_OTA_MESSAGE: Int
```

Unable to encode the OTA message for MT PDP or deactivate PDP. 

 Value: 2159

### CDMA_ALERT_STOP

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CDMA_ALERT_STOP: Int
```

Received an alert stop from the base station due to incoming only. 

 Value: 2077

### CDMA_INCOMING_CALL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CDMA_INCOMING_CALL: Int
```

Receiving an incoming call from the base station. 

 Value: 2076

### CDMA_INTERCEPT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CDMA_INTERCEPT: Int
```

Received an intercept order from the base station. 

 Value: 2073

### CDMA_LOCK

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CDMA_LOCK: Int
```

Device in CDMA locked state. 

 Value: 2072

### CDMA_RELEASE_DUE_TO_SO_REJECTION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CDMA_RELEASE_DUE_TO_SO_REJECTION: Int
```

Receiving a release from the base station with a SO (Service Option) Reject reason. 

 Value: 2075

### CDMA_REORDER

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CDMA_REORDER: Int
```

Receiving a reorder from the base station. 

 Value: 2074

### CDMA_RETRY_ORDER

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CDMA_RETRY_ORDER: Int
```

Receiving a retry order from the base station. 

 Value: 2086

### CHANNEL_ACQUISITION_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHANNEL_ACQUISITION_FAILURE: Int
```

Channel acquisition failures. This indicates that device has failed acquiring all the channels in the PRL. 

 Value: 2078

### CLOSE_IN_PROGRESS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CLOSE_IN_PROGRESS: Int
```

Tearing down is in progress. 

 Value: 2030

### COLLISION_WITH_NETWORK_INITIATED_REQUEST

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLLISION_WITH_NETWORK_INITIATED_REQUEST: Int
```

Network has already initiated the activation, modification, or deactivation of bearer resources that was requested by the UE. 

 Value: 56

### COMPANION_IFACE_IN_USE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COMPANION_IFACE_IN_USE: Int
```

Companion interface in use. 

 Value: 118

### CONCURRENT_SERVICES_INCOMPATIBLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONCURRENT_SERVICES_INCOMPATIBLE: Int
```

The concurrent services requested were not compatible. 

 Value: 2083

### CONCURRENT_SERVICES_NOT_ALLOWED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONCURRENT_SERVICES_NOT_ALLOWED: Int
```

In favor of a voice call or SMS when concurrent voice and data are not supported. 

 Value: 2091

### CONCURRENT_SERVICE_NOT_SUPPORTED_BY_BASE_STATION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONCURRENT_SERVICE_NOT_SUPPORTED_BY_BASE_STATION: Int
```

Concurrent service is not supported by base station. 

 Value: 2080

### CONDITIONAL_IE_ERROR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONDITIONAL_IE_ERROR: Int
```

Conditional Information Element (IE) error. 

 Value: 100

### CONGESTION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONGESTION: Int
```

Network cannot serve a request from the MS due to congestion. 

 Value: 2106

### CONNECTION_RELEASED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONNECTION_RELEASED: Int
```

Indicate the connection was released. 

 Value: 2113

### CS_DOMAIN_NOT_AVAILABLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CS_DOMAIN_NOT_AVAILABLE: Int
```

CS domain is not available. 

 Value: 2181

### CS_FALLBACK_CALL_ESTABLISHMENT_NOT_ALLOWED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CS_FALLBACK_CALL_ESTABLISHMENT_NOT_ALLOWED: Int
```

CS fallback call establishment is not allowed. 

 Value: 2188

### DATA_PLAN_EXPIRED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA_PLAN_EXPIRED: Int
```

Network initiates a detach on LTE with error cause ""data plan has been replenished or has expired. 

 Value: 2198

### DATA_ROAMING_SETTINGS_DISABLED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA_ROAMING_SETTINGS_DISABLED: Int
```

PDN Connection to a given APN is disallowed because data roaming is disabled from the device user interface settings and the UE is roaming. 

 Value: 2064

### DATA_SETTINGS_DISABLED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA_SETTINGS_DISABLED: Int
```

PDN Connection to a given APN is disallowed because data is disabled from the device user interface settings. 

 Value: 2063

### DBM_OR_SMS_IN_PROGRESS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DBM_OR_SMS_IN_PROGRESS: Int
```

DBM or SMS is in progress. 

 Value: 2211

### DDS_SWITCHED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DDS_SWITCHED: Int
```

DDS (Default data subscription) switch occurs. 

 Value: 2065

### DDS_SWITCH_IN_PROGRESS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DDS_SWITCH_IN_PROGRESS: Int
```

Default data subscription switch is in progress. 

 Value: 2067

### DRB_RELEASED_BY_RRC

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DRB_RELEASED_BY_RRC: Int
```

Data radio bearer is released by the RRC. 

 Value: 2112

### DS_EXPLICIT_DEACTIVATION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DS_EXPLICIT_DEACTIVATION: Int
```

Dedicated bearer will be deactivated regardless of the network response. 

 Value: 2125

### DUAL_SWITCH

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DUAL_SWITCH: Int
```

Dual switch from single standby to dual standby is in progress. 

 Value: 2227

### DUN_CALL_DISALLOWED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DUN_CALL_DISALLOWED: Int
```

Dial up networking (DUN) call bring up is rejected since UE is in eHRPD RAT. 

 Value: 2056

### DUPLICATE_BEARER_ID

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DUPLICATE_BEARER_ID: Int
```

Active dedicated bearer was requested using the same default bearer ID. 

 Value: 2118

### EHRPD_TO_HRPD_FALLBACK

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EHRPD_TO_HRPD_FALLBACK: Int
```

Device falls back from eHRPD to HRPD. 

 Value: 2049

### EMBMS_NOT_ENABLED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EMBMS_NOT_ENABLED: Int
```

Data call has been brought down because EMBMS is not enabled at the RRC layer. 

 Value: 2193

### EMBMS_REGULAR_DEACTIVATION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EMBMS_REGULAR_DEACTIVATION: Int
```

EMBMS data call has been successfully brought down. 

 Value: 2195

### EMERGENCY_IFACE_ONLY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EMERGENCY_IFACE_ONLY: Int
```

Emergency interface only. 

 Value: 116

### EMERGENCY_MODE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EMERGENCY_MODE: Int
```

Device is operating in Emergency mode. 

 Value: 2221

### EMM_ACCESS_BARRED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EMM_ACCESS_BARRED: Int
```

EPS (Evolved Packet System) Mobility Management (EMM) access barred. 

 Value: 115

### EMM_ACCESS_BARRED_INFINITE_RETRY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EMM_ACCESS_BARRED_INFINITE_RETRY: Int
```

EPS (Evolved Packet System) Mobility Management (EMM) access barred infinity retry. \* 

 Value: 121

### EMM_ATTACH_FAILED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EMM_ATTACH_FAILED: Int
```

Attach procedure is rejected by the network. 

 Value: 2115

### EMM_ATTACH_STARTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EMM_ATTACH_STARTED: Int
```

Attach procedure is started for EMC purposes. 

 Value: 2116

### EMM_DETACHED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EMM_DETACHED: Int
```

UE is detached. 

 Value: 2114

### EMM_T3417_EXPIRED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EMM_T3417_EXPIRED: Int
```

T3417 timer expiration of the service request procedure. 

 Value: 2130

### EMM_T3417_EXT_EXPIRED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EMM_T3417_EXT_EXPIRED: Int
```

Extended service request fails due to expiration of the T3417 EXT timer. 

 Value: 2131

### EPS_SERVICES_AND_NON_EPS_SERVICES_NOT_ALLOWED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EPS_SERVICES_AND_NON_EPS_SERVICES_NOT_ALLOWED: Int
```

EPS and non-EPS services are not allowed by the network. 

 Value: 2178

### EPS_SERVICES_NOT_ALLOWED_IN_PLMN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EPS_SERVICES_NOT_ALLOWED_IN_PLMN: Int
```

EPS services are not allowed in the PLMN. 

 Value: 2179

### ERROR_UNSPECIFIED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_UNSPECIFIED: Int
```

Data call fail due to unspecific errors. 

 Value: 65535

### ESM_BAD_OTA_MESSAGE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ESM_BAD_OTA_MESSAGE: Int
```

Bad OTA message is received from the network. 

 Value: 2122

### ESM_BEARER_DEACTIVATED_TO_SYNC_WITH_NETWORK

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ESM_BEARER_DEACTIVATED_TO_SYNC_WITH_NETWORK: Int
```

Bearer must be deactivated to synchronize with the network. 

 Value: 2120

### ESM_COLLISION_SCENARIOS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ESM_COLLISION_SCENARIOS: Int
```

Collision scenarios for the UE and network-initiated procedures. 

 Value: 2119

### ESM_CONTEXT_TRANSFERRED_DUE_TO_IRAT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ESM_CONTEXT_TRANSFERRED_DUE_TO_IRAT: Int
```

PDN was disconnected by the downlaod server due to IRAT. 

 Value: 2124

### ESM_DOWNLOAD_SERVER_REJECTED_THE_CALL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ESM_DOWNLOAD_SERVER_REJECTED_THE_CALL: Int
```

Download server rejected the call. 

 Value: 2123

### ESM_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ESM_FAILURE: Int
```

ESM level failure. 

 Value: 2182

### ESM_INFO_NOT_RECEIVED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ESM_INFO_NOT_RECEIVED: Int
```

EPS Session Management (ESM) information is not received. 

 Value: 53

### ESM_LOCAL_CAUSE_NONE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ESM_LOCAL_CAUSE_NONE: Int
```

No specific local cause is mentioned, usually a valid OTA cause. 

 Value: 2126

### ESM_NW_ACTIVATED_DED_BEARER_WITH_ID_OF_DEF_BEARER

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ESM_NW_ACTIVATED_DED_BEARER_WITH_ID_OF_DEF_BEARER: Int
```

Active dedicated bearer was requested for an existing default bearer. 

 Value: 2121

### ESM_PROCEDURE_TIME_OUT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ESM_PROCEDURE_TIME_OUT: Int
```

ESM procedure maximum attempt timeout failure. 

 Value: 2155

### ESM_UNKNOWN_EPS_BEARER_CONTEXT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ESM_UNKNOWN_EPS_BEARER_CONTEXT: Int
```

Invalid EPS bearer identity in the request. 

 Value: 2111

### EVDO_CONNECTION_DENY_BY_BILLING_OR_AUTHENTICATION_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVDO_CONNECTION_DENY_BY_BILLING_OR_AUTHENTICATION_FAILURE: Int
```

Received a connection deny due to billing or authentication failure on EVDO network. 

 Value: 2201

### EVDO_CONNECTION_DENY_BY_GENERAL_OR_NETWORK_BUSY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVDO_CONNECTION_DENY_BY_GENERAL_OR_NETWORK_BUSY: Int
```

Received a connection deny due to general or network busy on EVDO network. 

 Value: 2200

### EVDO_HDR_CHANGED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVDO_HDR_CHANGED: Int
```

HDR system has been changed due to redirection or the PRL was not preferred. 

 Value: 2202

### EVDO_HDR_CONNECTION_SETUP_TIMEOUT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVDO_HDR_CONNECTION_SETUP_TIMEOUT: Int
```

Connection setup on the HDR system was time out. 

 Value: 2206

### EVDO_HDR_EXITED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVDO_HDR_EXITED: Int
```

Device exited HDR due to redirection or the PRL was not preferred. 

 Value: 2203

### EVDO_HDR_NO_SESSION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVDO_HDR_NO_SESSION: Int
```

Device does not have an HDR session. 

 Value: 2204

### EVDO_USING_GPS_FIX_INSTEAD_OF_HDR_CALL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVDO_USING_GPS_FIX_INSTEAD_OF_HDR_CALL: Int
```

It is ending an HDR call origination in favor of a GPS fix. 

 Value: 2205

### FADE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FADE: Int
```

Device lost the system due to fade. 

 Value: 2217

### FAILED_TO_ACQUIRE_COLOCATED_HDR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FAILED_TO_ACQUIRE_COLOCATED_HDR: Int
```

Device failed to acquire a co-located HDR for origination. 

 Value: 2207

### FEATURE_NOT_SUPP

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE_NOT_SUPP: Int
```

Feature not supported. 

 Value: 40

### FILTER_SEMANTIC_ERROR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FILTER_SEMANTIC_ERROR: Int
```

Semantic errors in packet filter. 

 Value: 44

### FILTER_SYTAX_ERROR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FILTER_SYTAX_ERROR: Int
```

Syntactical errors in packet filter(s). 

 Value: 45

### FORBIDDEN_APN_NAME

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORBIDDEN_APN_NAME: Int
```

PDN being brought up with an APN that is part of forbidden APN Name list. 

 Value: 2066

### GPRS_REGISTRATION_FAIL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GPRS_REGISTRATION_FAIL: Int
```

Data fail due to GPRS registration failure. 

 Value: -2

### GPRS_SERVICES_AND_NON_GPRS_SERVICES_NOT_ALLOWED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GPRS_SERVICES_AND_NON_GPRS_SERVICES_NOT_ALLOWED: Int
```

Not allowed to operate either GPRS or non-GPRS services. 

 Value: 2097

### GPRS_SERVICES_NOT_ALLOWED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GPRS_SERVICES_NOT_ALLOWED: Int
```

MS is not allowed to operate GPRS services. 

 Value: 2098

### GPRS_SERVICES_NOT_ALLOWED_IN_THIS_PLMN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GPRS_SERVICES_NOT_ALLOWED_IN_THIS_PLMN: Int
```

UE requests GPRS service or the network initiates a detach request in a PLMN that does not offer roaming for GPRS services. 

 Value: 2103

### HANDOFF_PREFERENCE_CHANGED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HANDOFF_PREFERENCE_CHANGED: Int
```

System preference change back to SRAT during handoff 

 Value: 2251

### HDR_ACCESS_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HDR_ACCESS_FAILURE: Int
```

HDR system access failure. 

 Value: 2213

### HDR_FADE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HDR_FADE: Int
```

HDR module released the call due to fade. 

 Value: 2212

### HDR_NO_LOCK_GRANTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HDR_NO_LOCK_GRANTED: Int
```

HDR module could not be obtained because of the RF locked. 

 Value: 2210

### IFACE_AND_POL_FAMILY_MISMATCH

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IFACE_AND_POL_FAMILY_MISMATCH: Int
```  

 Value: 120

### IFACE_MISMATCH

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IFACE_MISMATCH: Int
```

Interface mismatch. 

 Value: 117

### ILLEGAL_ME

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ILLEGAL_ME: Int
```

ME could not be authenticated and the ME used is not acceptable to the network. 

 Value: 2096

### ILLEGAL_MS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ILLEGAL_MS: Int
```

Network refuses service to the MS because either an identity of the MS is not acceptable to the network or the MS does not pass the authentication check. 

 Value: 2095

### IMEI_NOT_ACCEPTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IMEI_NOT_ACCEPTED: Int
```

IMEI of the UE is not accepted by the network. 

 Value: 2177

### IMPLICITLY_DETACHED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IMPLICITLY_DETACHED: Int
```

Mobile reachable timer has expired, or the GMM context data related to the subscription does not exist in the SGSN. 

 Value: 2100

### IMSI_UNKNOWN_IN_HOME_SUBSCRIBER_SERVER

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IMSI_UNKNOWN_IN_HOME_SUBSCRIBER_SERVER: Int
```

IMSI present in the UE is unknown in the home subscriber server. 

 Value: 2176

### INCOMING_CALL_REJECTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INCOMING_CALL_REJECTED: Int
```

The other clients rejected incoming call. 

 Value: 2092

### INSUFFICIENT_RESOURCES

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INSUFFICIENT_RESOURCES: Int
```

Insufficient resources. 

 Value: 26

### INTERFACE_IN_USE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INTERFACE_IN_USE: Int
```

The current interface is being in use. 

 Value: 2058

### INTERNAL_CALL_PREEMPT_BY_HIGH_PRIO_APN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INTERNAL_CALL_PREEMPT_BY_HIGH_PRIO_APN: Int
```

Internal data call preempt by high priority APN. 

 Value: 114

### INTERNAL_EPC_NONEPC_TRANSITION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INTERNAL_EPC_NONEPC_TRANSITION: Int
```

Rejected/Brought down since UE is transition between EPC and NONEPC RAT. 

 Value: 2057

### INVALID_CONNECTION_ID

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INVALID_CONNECTION_ID: Int
```

No PDP exists with the given connection ID while modifying or deactivating or activation for an already active PDP. 

 Value: 2156

### INVALID_DNS_ADDR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INVALID_DNS_ADDR: Int
```

Not receiving a DNS address that was mandatory. 

 Value: 123

### INVALID_EMM_STATE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INVALID_EMM_STATE: Int
```

Invalid EMM state. 

 Value: 2190

### INVALID_MANDATORY_INFO

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INVALID_MANDATORY_INFO: Int
```

Invalid mandatory information. 

 Value: 96

### INVALID_MODE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INVALID_MODE: Int
```

Device operational mode is different from the mode requested in the traffic channel bring up. 

 Value: 2223

### INVALID_PCSCF_ADDR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INVALID_PCSCF_ADDR: Int
```

Invalid Proxy-Call Session Control Function (P-CSCF) address. 

 Value: 113

### INVALID_PCSCF_OR_DNS_ADDRESS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INVALID_PCSCF_OR_DNS_ADDRESS: Int
```

Not receiving either a PCSCF or a DNS address, one of them being mandatory. 

 Value: 124

### INVALID_PRIMARY_NSAPI

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INVALID_PRIMARY_NSAPI: Int
```

Primary context for NSAPI does not exist. 

 Value: 2158

### INVALID_SIM_STATE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INVALID_SIM_STATE: Int
```

SIM was marked by the network as invalid for the circuit and/or packet service domain. 

 Value: 2224

### INVALID_TRANSACTION_ID

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INVALID_TRANSACTION_ID: Int
```

Invalid transaction id. 

 Value: 81

### IPV6_ADDRESS_TRANSFER_FAILED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IPV6_ADDRESS_TRANSFER_FAILED: Int
```

IPv6 address transfer failed. 

 Value: 2047

### IPV6_PREFIX_UNAVAILABLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IPV6_PREFIX_UNAVAILABLE: Int
```

Device failure to obtain the prefix from the network. 

 Value: 2250

### IP_ADDRESS_MISMATCH

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IP_ADDRESS_MISMATCH: Int
```

IP address mismatch. 

 Value: 119

### IP_VERSION_MISMATCH

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IP_VERSION_MISMATCH: Int
```

New call bring up is rejected since the existing data call IP type doesn't match the requested IP. 

 Value: 2055

### IRAT_HANDOVER_FAILED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IRAT_HANDOVER_FAILED: Int
```

Data call was unsuccessfully transferred during the IRAT handover. 

 Value: 2194

### IS707B_MAX_ACCESS_PROBES

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IS707B_MAX_ACCESS_PROBES: Int
```

Maximum access probes for the IS-707B call. 

 Value: 2089

### IWLAN_AUTHORIZATION_REJECTED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IWLAN_AUTHORIZATION_REJECTED: Int
```

The user is barred from using the non-3GPP access or the subscribed APN. 

 Value: 9003

### IWLAN_CONGESTION

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IWLAN_CONGESTION: Int
```

The requested service was rejected because of congestion in the network while accessing the IWLAN ePDG. Defined in 3GPP TS 24.502, Section 9.2.4.2. 

 Value: 15500

### IWLAN_DNS_RESOLUTION_NAME_FAILURE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IWLAN_DNS_RESOLUTION_NAME_FAILURE: Int
```

Unable to resolve FQDN for the ePDG to an IP address 

 Value: 16388

### IWLAN_DNS_RESOLUTION_TIMEOUT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IWLAN_DNS_RESOLUTION_TIMEOUT: Int
```

No response received from the DNS Server due to a timeout 

 Value: 16389

### IWLAN_IKEV2_AUTH_FAILURE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IWLAN_IKEV2_AUTH_FAILURE: Int
```

Sent in the response to an IKE_AUTH message when, for some reason, the authentication failed. 

 Value: 16385

### IWLAN_IKEV2_CERT_INVALID

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IWLAN_IKEV2_CERT_INVALID: Int
```

IKE Certification validation failure 

 Value: 16387

### IWLAN_IKEV2_CONFIG_FAILURE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IWLAN_IKEV2_CONFIG_FAILURE: Int
```

IKE configuration error resulting in failure 

 Value: 16384

### IWLAN_IKEV2_MSG_TIMEOUT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IWLAN_IKEV2_MSG_TIMEOUT: Int
```

IKE message timeout, tunnel setup failed due to no response from EPDG 

 Value: 16386

### IWLAN_ILLEGAL_ME

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IWLAN_ILLEGAL_ME: Int
```

The Mobile Equipment used is not acceptable to the network 

 Value: 9006

### IWLAN_IMEI_NOT_ACCEPTED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IWLAN_IMEI_NOT_ACCEPTED: Int
```

The network does not accept emergency PDN bringup request using an IMEI 

 Value: 11005

### IWLAN_MAX_CONNECTION_REACHED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IWLAN_MAX_CONNECTION_REACHED: Int
```

The PDN connection has been rejected. No additional PDN connections can be established for the UE due to the network policies or capabilities. 

 Value: 8193

### IWLAN_NETWORK_FAILURE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IWLAN_NETWORK_FAILURE: Int
```

The network has determined that the requested procedure cannot be completed successfully due to network failure. 

 Value: 10500

### IWLAN_NON_3GPP_ACCESS_TO_EPC_NOT_ALLOWED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IWLAN_NON_3GPP_ACCESS_TO_EPC_NOT_ALLOWED: Int
```

No non-3GPP subscription is associated with the IMSI. The UE is not allowed to use non-3GPP access to EPC. 

 Value: 9000

### IWLAN_NO_APN_SUBSCRIPTION

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IWLAN_NO_APN_SUBSCRIPTION: Int
```

The requested APN is not included in the user's profile, and therefore is not authorized for that user. 

 Value: 9002

### IWLAN_PDN_CONNECTION_REJECTION

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IWLAN_PDN_CONNECTION_REJECTION: Int
```

The PDN connection corresponding to the requested APN has been rejected. 

 Value: 8192

### IWLAN_PLMN_NOT_ALLOWED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IWLAN_PLMN_NOT_ALLOWED: Int
```

The ePDG performs PLMN filtering (based on roaming agreements) and rejects the request from the UE. The UE requests service in a PLMN where the UE is not allowed to operate. 

 Value: 11011

### IWLAN_RAT_TYPE_NOT_ALLOWED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IWLAN_RAT_TYPE_NOT_ALLOWED: Int
```

The access type is restricted to the user. 

 Value: 11001

### IWLAN_SEMANTIC_ERRORS_IN_PACKET_FILTERS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IWLAN_SEMANTIC_ERRORS_IN_PACKET_FILTERS: Int
```

The PDN connection has been rejected due to sematic errors in the packet filter. 

 Value: 8244

### IWLAN_SEMANTIC_ERROR_IN_THE_TFT_OPERATION

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IWLAN_SEMANTIC_ERROR_IN_THE_TFT_OPERATION: Int
```

The PDN connection has been rejected due to a semantic error in TFT operation. 

 Value: 8241

### IWLAN_SYNTACTICAL_ERRORS_IN_PACKET_FILTERS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IWLAN_SYNTACTICAL_ERRORS_IN_PACKET_FILTERS: Int
```

The PDN connection has been rejected due to syntactic errors in the packet filter. 

 Value: 8245

### IWLAN_SYNTACTICAL_ERROR_IN_THE_TFT_OPERATION

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IWLAN_SYNTACTICAL_ERROR_IN_THE_TFT_OPERATION: Int
```

The PDN connection has been rejected due to a syntactic error in TFT operation. 

 Value: 8242

### IWLAN_TUNNEL_NOT_FOUND

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IWLAN_TUNNEL_NOT_FOUND: Int
```

Expected to update or bring down an ePDG tunnel, but no tunnel found 

 Value: 16390

### IWLAN_UNAUTHENTICATED_EMERGENCY_NOT_SUPPORTED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IWLAN_UNAUTHENTICATED_EMERGENCY_NOT_SUPPORTED: Int
```

The ePDG does not support un-authenticated IMSI based emergency PDN bringup \* 

 Value: 11055

### IWLAN_USER_UNKNOWN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IWLAN_USER_UNKNOWN: Int
```

The user identified by the IMSI is unknown. 

 Value: 9001

### LIMITED_TO_IPV4

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LIMITED_TO_IPV4: Int
```

IPv6 interface bring up fails because the network provided only the IPv4 address for the upcoming PDN permanent client can reattempt a IPv6 call bring up after the IPv4 interface is also brought down. However, there is no guarantee that the network will provide a IPv6 address. 

 Value: 2234

### LIMITED_TO_IPV6

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LIMITED_TO_IPV6: Int
```

IPv4 interface bring up fails because the network provided only the IPv6 address for the upcoming PDN permanent client can reattempt a IPv4 call bring up after the IPv6 interface is also brought down. However there is no guarantee that the network will provide a IPv4 address. 

 Value: 2235

### LLC_SNDCP

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LLC_SNDCP: Int
```

Logical Link Control (LLC) Sub Network Dependent Convergence Protocol (SNDCP). 

 Value: 25

### LOCAL_END

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCAL_END: Int
```

Client ended the data call. 

 Value: 2215

### LOCATION_AREA_NOT_ALLOWED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCATION_AREA_NOT_ALLOWED: Int
```

MS requests service, or the network initiates a detach request, in a location area where the HPLMN determines that the MS, by subscription, is not allowed to operate. 

 Value: 2102

### LOST_CONNECTION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOST_CONNECTION: Int
```

Data connection was lost. 

 Value: 65540

### LOWER_LAYER_REGISTRATION_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOWER_LAYER_REGISTRATION_FAILURE: Int
```

Lower layer registration failure. 

 Value: 2197

### LOW_POWER_MODE_OR_POWERING_DOWN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOW_POWER_MODE_OR_POWERING_DOWN: Int
```

Device is going into lower power mode or powering down. 

 Value: 2044

### LTE_NAS_SERVICE_REQUEST_FAILED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LTE_NAS_SERVICE_REQUEST_FAILED: Int
```

Service request procedure failure. 

 Value: 2117

### LTE_THROTTLING_NOT_REQUIRED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LTE_THROTTLING_NOT_REQUIRED: Int
```

Throttling is not needed for this service request failure. 

 Value: 2127

### MAC_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAC_FAILURE: Int
```

MAC level failure. 

 Value: 2183

### MATCH_ALL_RULE_NOT_ALLOWED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MATCH_ALL_RULE_NOT_ALLOWED: Int
```

No matching rule available for the request, and match-all rule is not allowed for it. 

 Value: 2253

### MAXIMIUM_NSAPIS_EXCEEDED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAXIMIUM_NSAPIS_EXCEEDED: Int
```

Maximum NSAPIs have been exceeded during PDP activation. 

 Value: 2157

### MAXINUM_SIZE_OF_L2_MESSAGE_EXCEEDED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAXINUM_SIZE_OF_L2_MESSAGE_EXCEEDED: Int
```

Maximum size of the L2 message was exceeded. 

 Value: 2166

### MAX_ACCESS_PROBE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX_ACCESS_PROBE: Int
```

Maximum access probes transmitted. 

 Value: 2079

### MAX_IPV4_CONNECTIONS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX_IPV4_CONNECTIONS: Int
```

IPv4 data call bring up is rejected because the UE already maintains the allotted maximum number of IPv4 data connections. 

 Value: 2052

### MAX_IPV6_CONNECTIONS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX_IPV6_CONNECTIONS: Int
```

IPv6 data call bring up is rejected because the UE already maintains the allotted maximum number of IPv6 data connections. 

 Value: 2053

### MAX_PPP_INACTIVITY_TIMER_EXPIRED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX_PPP_INACTIVITY_TIMER_EXPIRED: Int
```

Maximum PPP inactivity timer expired. 

 Value: 2046

### MESSAGE_INCORRECT_SEMANTIC

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MESSAGE_INCORRECT_SEMANTIC: Int
```

Incorrect message semantic. 

 Value: 95

### MESSAGE_TYPE_UNSUPPORTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MESSAGE_TYPE_UNSUPPORTED: Int
```

Unsupported message type. 

 Value: 97

### MIP_CONFIG_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIP_CONFIG_FAILURE: Int
```

UE is in MIP-only configuration but the MIP configuration fails on call bring up due to incorrect provisioning. 

 Value: 2050

### MIP_FA_ADMIN_PROHIBITED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIP_FA_ADMIN_PROHIBITED: Int
```

Foreign agent administratively prohibited MIP (Mobile IP) registration. 

 Value: 2001

### MIP_FA_DELIVERY_STYLE_NOT_SUPPORTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIP_FA_DELIVERY_STYLE_NOT_SUPPORTED: Int
```

Foreign agent rejected MIP (Mobile IP) registration because of delivery style was not supported. 

 Value: 2012

### MIP_FA_ENCAPSULATION_UNAVAILABLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIP_FA_ENCAPSULATION_UNAVAILABLE: Int
```

Foreign agent rejected MIP (Mobile IP) registration because of requested encapsulation was unavailable. 

 Value: 2008

### MIP_FA_HOME_AGENT_AUTHENTICATION_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIP_FA_HOME_AGENT_AUTHENTICATION_FAILURE: Int
```

Foreign agent rejected MIP (Mobile IP) registration because of home agent authentication failure. 

 Value: 2004

### MIP_FA_INSUFFICIENT_RESOURCES

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIP_FA_INSUFFICIENT_RESOURCES: Int
```

Foreign agent rejected MIP (Mobile IP) registration because of insufficient resources. 

 Value: 2002

### MIP_FA_MALFORMED_REPLY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIP_FA_MALFORMED_REPLY: Int
```

Foreign agent rejected MIP (Mobile IP) registration because of malformed reply. 

 Value: 2007

### MIP_FA_MALFORMED_REQUEST

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIP_FA_MALFORMED_REQUEST: Int
```

Foreign agent rejected MIP (Mobile IP) registration because of malformed request. 

 Value: 2006

### MIP_FA_MISSING_CHALLENGE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIP_FA_MISSING_CHALLENGE: Int
```

Foreign agent rejected MIP (Mobile IP) registration because of missing challenge. 

 Value: 2017

### MIP_FA_MISSING_HOME_ADDRESS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIP_FA_MISSING_HOME_ADDRESS: Int
```

Foreign agent rejected MIP (Mobile IP) registration because of missing Home Address. 

 Value: 2015

### MIP_FA_MISSING_HOME_AGENT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIP_FA_MISSING_HOME_AGENT: Int
```

Foreign agent rejected MIP (Mobile IP) registration because of missing Home Agent. 

 Value: 2014

### MIP_FA_MISSING_NAI

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIP_FA_MISSING_NAI: Int
```

Foreign agent rejected MIP (Mobile IP) registration because of missing NAI (Network Access Identifier). 

 Value: 2013

### MIP_FA_MOBILE_NODE_AUTHENTICATION_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIP_FA_MOBILE_NODE_AUTHENTICATION_FAILURE: Int
```

Foreign agent rejected MIP (Mobile IP) registration because of MN-AAA authenticator was wrong. 

 Value: 2003

### MIP_FA_REASON_UNSPECIFIED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIP_FA_REASON_UNSPECIFIED: Int
```

Reason unspecified for foreign agent rejected MIP (Mobile IP) registration. 

 Value: 2000

### MIP_FA_REQUESTED_LIFETIME_TOO_LONG

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIP_FA_REQUESTED_LIFETIME_TOO_LONG: Int
```

Foreign agent rejected MIP (Mobile IP) registration because of requested lifetime was too long. 

 Value: 2005

### MIP_FA_REVERSE_TUNNEL_IS_MANDATORY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIP_FA_REVERSE_TUNNEL_IS_MANDATORY: Int
```

Foreign agent rejected MIP (Mobile IP) registration because of reverse tunnel was mandatory but not requested by device. 

 Value: 2011

### MIP_FA_REVERSE_TUNNEL_UNAVAILABLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIP_FA_REVERSE_TUNNEL_UNAVAILABLE: Int
```

Foreign agent rejected MIP (Mobile IP) registration because of reverse tunnel was unavailable. 

 Value: 2010

### MIP_FA_STALE_CHALLENGE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIP_FA_STALE_CHALLENGE: Int
```

Foreign agent rejected MIP (Mobile IP) registration because of stale challenge. 

 Value: 2018

### MIP_FA_UNKNOWN_CHALLENGE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIP_FA_UNKNOWN_CHALLENGE: Int
```

Foreign agent rejected MIP (Mobile IP) registration because of unknown challenge. 

 Value: 2016

### MIP_FA_VJ_HEADER_COMPRESSION_UNAVAILABLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIP_FA_VJ_HEADER_COMPRESSION_UNAVAILABLE: Int
```

Foreign agent rejected MIP (Mobile IP) registration of VJ Header Compression was unavailable. 

 Value: 2009

### MIP_HA_ADMIN_PROHIBITED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIP_HA_ADMIN_PROHIBITED: Int
```

Home agent administratively prohibited MIP (Mobile IP) registration. 

 Value: 2020

### MIP_HA_ENCAPSULATION_UNAVAILABLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIP_HA_ENCAPSULATION_UNAVAILABLE: Int
```

Home agent rejected MIP (Mobile IP) registration because of encapsulation unavailable. 

 Value: 2029

### MIP_HA_FOREIGN_AGENT_AUTHENTICATION_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIP_HA_FOREIGN_AGENT_AUTHENTICATION_FAILURE: Int
```

Home agent rejected MIP (Mobile IP) registration because of foreign agent authentication failure. 

 Value: 2023

### MIP_HA_INSUFFICIENT_RESOURCES

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIP_HA_INSUFFICIENT_RESOURCES: Int
```

Home agent rejected MIP (Mobile IP) registration because of insufficient resources. 

 Value: 2021

### MIP_HA_MALFORMED_REQUEST

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIP_HA_MALFORMED_REQUEST: Int
```

Home agent rejected MIP (Mobile IP) registration because of malformed request. 

 Value: 2025

### MIP_HA_MOBILE_NODE_AUTHENTICATION_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIP_HA_MOBILE_NODE_AUTHENTICATION_FAILURE: Int
```

Home agent rejected MIP (Mobile IP) registration because of MN-HA authenticator was wrong. 

 Value: 2022

### MIP_HA_REASON_UNSPECIFIED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIP_HA_REASON_UNSPECIFIED: Int
```

Reason unspecified for home agent rejected MIP (Mobile IP) registration. 

 Value: 2019

### MIP_HA_REGISTRATION_ID_MISMATCH

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIP_HA_REGISTRATION_ID_MISMATCH: Int
```

Home agent rejected MIP (Mobile IP) registration because of registration id mismatch. 

 Value: 2024

### MIP_HA_REVERSE_TUNNEL_IS_MANDATORY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIP_HA_REVERSE_TUNNEL_IS_MANDATORY: Int
```

Home agent rejected MIP (Mobile IP) registration because of reverse tunnel is mandatory but not requested by device. 

 Value: 2028

### MIP_HA_REVERSE_TUNNEL_UNAVAILABLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIP_HA_REVERSE_TUNNEL_UNAVAILABLE: Int
```

Home agent rejected MIP (Mobile IP) registration because of reverse tunnel was unavailable. 

 Value: 2027

### MIP_HA_UNKNOWN_HOME_AGENT_ADDRESS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIP_HA_UNKNOWN_HOME_AGENT_ADDRESS: Int
```

Home agent rejected MIP (Mobile IP) registration because of unknown home agent address. 

 Value: 2026

### MISSING_UNKNOWN_APN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MISSING_UNKNOWN_APN: Int
```

Missing or unknown APN. 

 Value: 27

### MODEM_APP_PREEMPTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODEM_APP_PREEMPTED: Int
```

Another application in modem preempts the data call. 

 Value: 2032

### MODEM_RESTART

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODEM_RESTART: Int
```

Modem restart. 

 Value: 2037

### MSC_TEMPORARILY_NOT_REACHABLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MSC_TEMPORARILY_NOT_REACHABLE: Int
```

Mobile switching center is temporarily unreachable. 

 Value: 2180

### MSG_AND_PROTOCOL_STATE_UNCOMPATIBLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MSG_AND_PROTOCOL_STATE_UNCOMPATIBLE: Int
```

Message and protocol state uncompatible. 

 Value: 101

### MSG_TYPE_NONCOMPATIBLE_STATE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MSG_TYPE_NONCOMPATIBLE_STATE: Int
```

Message type uncompatible. 

 Value: 98

### MS_IDENTITY_CANNOT_BE_DERIVED_BY_THE_NETWORK

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MS_IDENTITY_CANNOT_BE_DERIVED_BY_THE_NETWORK: Int
```

No matching identity or context could be found in the network. 

 Value: 2099

### MULTIPLE_PDP_CALL_NOT_ALLOWED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MULTIPLE_PDP_CALL_NOT_ALLOWED: Int
```

Multiple PDP call feature is disabled. 

 Value: 2192

### MULTI_CONN_TO_SAME_PDN_NOT_ALLOWED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MULTI_CONN_TO_SAME_PDN_NOT_ALLOWED: Int
```

Multiple connections to a same PDN is not allowed. 

 Value: 55

### NAS_LAYER_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAS_LAYER_FAILURE: Int
```

Non-Access Spectrum layer failure. 

 Value: 2191

### NAS_REQUEST_REJECTED_BY_NETWORK

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAS_REQUEST_REJECTED_BY_NETWORK: Int
```

Non-access stratum (NAS) request was rejected by the network. 

 Value: 2167

### NAS_SIGNALLING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAS_SIGNALLING: Int
```

NAS signalling. 

 Value: 14

### NETWORK_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NETWORK_FAILURE: Int
```

Network Failure. 

 Value: 38

### NETWORK_INITIATED_DETACH_NO_AUTO_REATTACH

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NETWORK_INITIATED_DETACH_NO_AUTO_REATTACH: Int
```

Network-initiated detach without reattach. 

 Value: 2154

### NETWORK_INITIATED_DETACH_WITH_AUTO_REATTACH

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NETWORK_INITIATED_DETACH_WITH_AUTO_REATTACH: Int
```

Network-initiated detach with reattach. 

 Value: 2153

### NETWORK_INITIATED_TERMINATION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NETWORK_INITIATED_TERMINATION: Int
```

Brought down by the network. 

 Value: 2031

### NONE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NONE: Int
```

There is no failure 

 Value: 0

### NON_IP_NOT_SUPPORTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NON_IP_NOT_SUPPORTED: Int
```

UE is unable to bring up a non-IP data call because the device is not camped on a NB1 cell. 

 Value: 2069

### NORMAL_RELEASE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NORMAL_RELEASE: Int
```

Receiving a release from the base station with no reason. 

 Value: 2218

### NO_CDMA_SERVICE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NO_CDMA_SERVICE: Int
```

Device does not have CDMA service. 

 Value: 2084

### NO_COLLOCATED_HDR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NO_COLLOCATED_HDR: Int
```

There is no co-located HDR. 

 Value: 2225

### NO_EPS_BEARER_CONTEXT_ACTIVATED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NO_EPS_BEARER_CONTEXT_ACTIVATED: Int
```

No EPS bearer context was activated. 

 Value: 2189

### NO_GPRS_CONTEXT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NO_GPRS_CONTEXT: Int
```

GPRS context is not available. 

 Value: 2094

### NO_HYBRID_HDR_SERVICE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NO_HYBRID_HDR_SERVICE: Int
```

Device has no hybrid HDR service. 

 Value: 2209

### NO_PDP_CONTEXT_ACTIVATED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NO_PDP_CONTEXT_ACTIVATED: Int
```

MS requests an establishment of the radio access bearers for all active PDP contexts by sending a service request message indicating data to the network, but the SGSN does not have any active PDP context. 

 Value: 2107

### NO_RESPONSE_FROM_BASE_STATION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NO_RESPONSE_FROM_BASE_STATION: Int
```

There was no response received from the base station. 

 Value: 2081

### NO_SERVICE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NO_SERVICE: Int
```

Device has no service. 

 Value: 2216

### NO_SERVICE_ON_GATEWAY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NO_SERVICE_ON_GATEWAY: Int
```

No service on the gateway. 

 Value: 2093

### NSAPI_IN_USE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NSAPI_IN_USE: Int
```

The Network Service Access Point Identifier (NSAPI) is in use. 

 Value: 35

### NULL_APN_DISALLOWED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NULL_APN_DISALLOWED: Int
```

PDN is attempted to be brought up with NULL APN but NULL APN is not supported. 

 Value: 2061

### OEM_DCFAILCAUSE_1

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OEM_DCFAILCAUSE_1: Int
```  

 Value: 4097

### OEM_DCFAILCAUSE_10

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OEM_DCFAILCAUSE_10: Int
```  

 Value: 4106

### OEM_DCFAILCAUSE_11

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OEM_DCFAILCAUSE_11: Int
```  

 Value: 4107

### OEM_DCFAILCAUSE_12

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OEM_DCFAILCAUSE_12: Int
```  

 Value: 4108

### OEM_DCFAILCAUSE_13

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OEM_DCFAILCAUSE_13: Int
```  

 Value: 4109

### OEM_DCFAILCAUSE_14

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OEM_DCFAILCAUSE_14: Int
```  

 Value: 4110

### OEM_DCFAILCAUSE_15

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OEM_DCFAILCAUSE_15: Int
```  

 Value: 4111

### OEM_DCFAILCAUSE_2

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OEM_DCFAILCAUSE_2: Int
```  

 Value: 4098

### OEM_DCFAILCAUSE_3

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OEM_DCFAILCAUSE_3: Int
```  

 Value: 4099

### OEM_DCFAILCAUSE_4

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OEM_DCFAILCAUSE_4: Int
```  

 Value: 4100

### OEM_DCFAILCAUSE_5

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OEM_DCFAILCAUSE_5: Int
```  

 Value: 4101

### OEM_DCFAILCAUSE_6

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OEM_DCFAILCAUSE_6: Int
```  

 Value: 4102

### OEM_DCFAILCAUSE_7

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OEM_DCFAILCAUSE_7: Int
```  

 Value: 4103

### OEM_DCFAILCAUSE_8

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OEM_DCFAILCAUSE_8: Int
```  

 Value: 4104

### OEM_DCFAILCAUSE_9

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OEM_DCFAILCAUSE_9: Int
```  

 Value: 4105

### ONLY_IPV4V6_ALLOWED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ONLY_IPV4V6_ALLOWED: Int
```

Network supports IPv4v6 PDP type only. Non-IP type is not allowed. In LTE mode of operation, this is a PDN throttling cause code, meaning the UE may throttle further requests to the same APN. 

 Value: 57

### ONLY_IPV4_ALLOWED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ONLY_IPV4_ALLOWED: Int
```

Packet Data Protocol (PDP) type IPv4 only allowed. 

 Value: 50

### ONLY_IPV6_ALLOWED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ONLY_IPV6_ALLOWED: Int
```

Packet Data Protocol (PDP) type IPv6 only allowed. 

 Value: 51

### ONLY_NON_IP_ALLOWED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ONLY_NON_IP_ALLOWED: Int
```

Network supports non-IP PDP type only. IPv4, IPv6 and IPv4v6 is not allowed. In LTE mode of operation, this is a PDN throttling cause code, meaning the UE can throttle further requests to the same APN. 

 Value: 58

### ONLY_SINGLE_BEARER_ALLOWED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ONLY_SINGLE_BEARER_ALLOWED: Int
```

Single address bearers only allowed. 

 Value: 52

### OPERATOR_BARRED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OPERATOR_BARRED: Int
```

Operator determined barring. (no retry) 

 Value: 8

### OTASP_COMMIT_IN_PROGRESS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OTASP_COMMIT_IN_PROGRESS: Int
```

OTASP commit is in progress. 

 Value: 2208

### PDN_CONN_DOES_NOT_EXIST

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PDN_CONN_DOES_NOT_EXIST: Int
```

PDN connection does not exist. 

 Value: 54

### PDN_INACTIVITY_TIMER_EXPIRED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PDN_INACTIVITY_TIMER_EXPIRED: Int
```

PDN inactivity timer expired due to no data transmission in a configurable duration of time. 

 Value: 2051

### PDN_IPV4_CALL_DISALLOWED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PDN_IPV4_CALL_DISALLOWED: Int
```

IPV4 PDN is in throttled state due to network providing only IPV6 address during the previous VSNCP bringup (subs_limited_to_v6). 

 Value: 2033

### PDN_IPV4_CALL_THROTTLED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PDN_IPV4_CALL_THROTTLED: Int
```

IPV4 PDN is in throttled state due to previous VSNCP bringup failure(s). 

 Value: 2034

### PDN_IPV6_CALL_DISALLOWED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PDN_IPV6_CALL_DISALLOWED: Int
```

IPV6 PDN is in throttled state due to network providing only IPV4 address during the previous VSNCP bringup (subs_limited_to_v4). 

 Value: 2035

### PDN_IPV6_CALL_THROTTLED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PDN_IPV6_CALL_THROTTLED: Int
```

IPV6 PDN is in throttled state due to previous VSNCP bringup failure(s). 

 Value: 2036

### PDN_NON_IP_CALL_DISALLOWED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PDN_NON_IP_CALL_DISALLOWED: Int
```

Non-IP PDN is in disallowed state due to the network providing only an IP address. 

 Value: 2071

### PDN_NON_IP_CALL_THROTTLED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PDN_NON_IP_CALL_THROTTLED: Int
```

Non-IP PDN is in throttled state due to previous VSNCP bringup failure(s). 

 Value: 2070

### PDP_ACTIVATE_MAX_RETRY_FAILED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PDP_ACTIVATE_MAX_RETRY_FAILED: Int
```

SM attempts PDP activation for a maximum of four attempts. 

 Value: 2109

### PDP_DUPLICATE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PDP_DUPLICATE: Int
```

PDP context already exists. 

 Value: 2104

### PDP_ESTABLISH_TIMEOUT_EXPIRED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PDP_ESTABLISH_TIMEOUT_EXPIRED: Int
```

Expiration of the PDP establish timer with a maximum of five retries. 

 Value: 2161

### PDP_INACTIVE_TIMEOUT_EXPIRED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PDP_INACTIVE_TIMEOUT_EXPIRED: Int
```

Expiration of the PDP deactivate timer with a maximum of four retries. 

 Value: 2163

### PDP_LOWERLAYER_ERROR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PDP_LOWERLAYER_ERROR: Int
```

PDP activation failed due to RRC_ABORT or a forbidden PLMN. 

 Value: 2164

### PDP_MODIFY_COLLISION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PDP_MODIFY_COLLISION: Int
```

MO PDP modify collision when the MT PDP is already in progress. 

 Value: 2165

### PDP_MODIFY_TIMEOUT_EXPIRED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PDP_MODIFY_TIMEOUT_EXPIRED: Int
```

Expiration of the PDP modify timer with a maximum of four retries. 

 Value: 2162

### PDP_PPP_NOT_SUPPORTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PDP_PPP_NOT_SUPPORTED: Int
```

PDP PPP calls are not supported. 

 Value: 2038

### PDP_WITHOUT_ACTIVE_TFT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PDP_WITHOUT_ACTIVE_TFT: Int
```

Packet Data Protocol (PDP) without active traffic flow template (TFT). 

 Value: 46

### PHONE_IN_USE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PHONE_IN_USE: Int
```

Device is in use (e.g., voice call). 

 Value: 2222

### PHYSICAL_LINK_CLOSE_IN_PROGRESS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PHYSICAL_LINK_CLOSE_IN_PROGRESS: Int
```

Physical link is in the process of cleanup. 

 Value: 2040

### PLMN_NOT_ALLOWED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PLMN_NOT_ALLOWED: Int
```

UE requests GPRS service, or the network initiates a detach request in a PLMN which does not offer roaming for GPRS services to that MS. 

 Value: 2101

### PPP_AUTH_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PPP_AUTH_FAILURE: Int
```

Data call bring up fails in the PPP setup due to an authorization failure. (e.g., authorization is required, but not negotiated with the network during an LCP phase) 

 Value: 2229

### PPP_CHAP_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PPP_CHAP_FAILURE: Int
```

Data call bring up fails in the PPP setup due to a CHAP failure. 

 Value: 2232

### PPP_CLOSE_IN_PROGRESS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PPP_CLOSE_IN_PROGRESS: Int
```

Data call bring up fails in the PPP setup because the PPP is in the process of cleaning the previous PPP session. 

 Value: 2233

### PPP_OPTION_MISMATCH

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PPP_OPTION_MISMATCH: Int
```

Data call bring up fails in the PPP setup due to an option mismatch. 

 Value: 2230

### PPP_PAP_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PPP_PAP_FAILURE: Int
```

Data call bring up fails in the PPP setup due to a PAP failure. 

 Value: 2231

### PPP_TIMEOUT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PPP_TIMEOUT: Int
```

Data call bring up fails in the PPP setup due to a timeout. (e.g., an LCP conf ack was not received from the network) 

 Value: 2228

### PREF_RADIO_TECH_CHANGED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PREF_RADIO_TECH_CHANGED: Int
```

Preferred technology has changed, must retry with parameters appropriate for new technology. 

 Value: -4

### PROFILE_BEARER_INCOMPATIBLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROFILE_BEARER_INCOMPATIBLE: Int
```

APN bearer type in the profile does not match preferred network mode. 

 Value: 2042

### PROTOCOL_ERRORS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROTOCOL_ERRORS: Int
```

Protocol errors. 

 Value: 111

### QOS_NOT_ACCEPTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QOS_NOT_ACCEPTED: Int
```

Quality of service (QoS) is not accepted. 

 Value: 37

### RADIO_ACCESS_BEARER_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RADIO_ACCESS_BEARER_FAILURE: Int
```

Radio access bearer failure. 

 Value: 2110

### RADIO_ACCESS_BEARER_SETUP_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RADIO_ACCESS_BEARER_SETUP_FAILURE: Int
```

Radio access bearer is not established by the lower layers during activation, modification, or deactivation. 

 Value: 2160

### RADIO_NOT_AVAILABLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RADIO_NOT_AVAILABLE: Int
```

Data fail due to radio not unavailable. 

 Value: 65537

### RADIO_POWER_OFF

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RADIO_POWER_OFF: Int
```

data call was disconnected because radio was resetting, powered off. 

 Value: -5

### REDIRECTION_OR_HANDOFF_IN_PROGRESS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REDIRECTION_OR_HANDOFF_IN_PROGRESS: Int
```

Device is in the process of redirecting or handing off to a different target system. 

 Value: 2220

### REGISTRATION_FAIL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REGISTRATION_FAIL: Int
```

Data fail due to registration failure. 

 Value: -1

### REGULAR_DEACTIVATION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REGULAR_DEACTIVATION: Int
```

Regular deactivation. 

 Value: 36

### REJECTED_BY_BASE_STATION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REJECTED_BY_BASE_STATION: Int
```

The base station rejecting the call. 

 Value: 2082

### RRC_CONNECTION_ABORTED_AFTER_HANDOVER

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RRC_CONNECTION_ABORTED_AFTER_HANDOVER: Int
```

Radio resource control (RRC) connection was aborted by the non-access stratum (NAS) after an IRAT to LTE IRAT handover. 

 Value: 2173

### RRC_CONNECTION_ABORTED_AFTER_IRAT_CELL_CHANGE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RRC_CONNECTION_ABORTED_AFTER_IRAT_CELL_CHANGE: Int
```

Radio resource control (RRC) connection was aborted before deactivating the LTE stack after a successful LTE to GSM/EDGE IRAT cell change order procedure. 

 Value: 2174

### RRC_CONNECTION_ABORTED_DUE_TO_IRAT_CHANGE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RRC_CONNECTION_ABORTED_DUE_TO_IRAT_CHANGE: Int
```

Radio resource control (RRC) connection was aborted before deactivating the LTE stack due to a successful LTE to WCDMA/GSM/TD-SCDMA IRAT change. 

 Value: 2171

### RRC_CONNECTION_ABORTED_DURING_IRAT_CELL_CHANGE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RRC_CONNECTION_ABORTED_DURING_IRAT_CELL_CHANGE: Int
```

Radio resource control (RRC) connection was aborted in the middle of a LTE to GSM IRAT cell change order procedure. 

 Value: 2175

### RRC_CONNECTION_ABORT_REQUEST

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RRC_CONNECTION_ABORT_REQUEST: Int
```

Connection has been released by the radio resource control (RRC) due to an abort request. 

 Value: 2151

### RRC_CONNECTION_ACCESS_BARRED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RRC_CONNECTION_ACCESS_BARRED: Int
```

Radio resource control (RRC) connection establishment failed due to access barrred. 

 Value: 2139

### RRC_CONNECTION_ACCESS_STRATUM_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RRC_CONNECTION_ACCESS_STRATUM_FAILURE: Int
```

Radio resource control (RRC) connection failure at access stratum. 

 Value: 2137

### RRC_CONNECTION_ANOTHER_PROCEDURE_IN_PROGRESS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RRC_CONNECTION_ANOTHER_PROCEDURE_IN_PROGRESS: Int
```

Radio resource control (RRC) connection establishment is aborted due to another procedure. 

 Value: 2138

### RRC_CONNECTION_CELL_NOT_CAMPED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RRC_CONNECTION_CELL_NOT_CAMPED: Int
```

Connection establishment failed as the radio resource control (RRC) is not camped on any cell. 

 Value: 2144

### RRC_CONNECTION_CELL_RESELECTION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RRC_CONNECTION_CELL_RESELECTION: Int
```

Radio resource control (RRC) connection establishment failed due to cell reselection at access stratum. 

 Value: 2140

### RRC_CONNECTION_CONFIG_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RRC_CONNECTION_CONFIG_FAILURE: Int
```

Connection establishment failed due to configuration failure at the radio resource control (RRC). 

 Value: 2141

### RRC_CONNECTION_INVALID_REQUEST

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RRC_CONNECTION_INVALID_REQUEST: Int
```

Radio resource control (RRC) connection establishment failure due to an error in the request message. 

 Value: 2168

### RRC_CONNECTION_LINK_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RRC_CONNECTION_LINK_FAILURE: Int
```

Connection establishment failed due to a link failure at the radio resource control (RRC). 

 Value: 2143

### RRC_CONNECTION_NORMAL_RELEASE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RRC_CONNECTION_NORMAL_RELEASE: Int
```

Normal radio resource control (RRC) connection release. 

 Value: 2147

### RRC_CONNECTION_OUT_OF_SERVICE_DURING_CELL_REGISTER

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RRC_CONNECTION_OUT_OF_SERVICE_DURING_CELL_REGISTER: Int
```

UE is out of service during the call register. 

 Value: 2150

### RRC_CONNECTION_RADIO_LINK_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RRC_CONNECTION_RADIO_LINK_FAILURE: Int
```

Radio resource control (RRC) connection release failed due to radio link failure conditions. 

 Value: 2148

### RRC_CONNECTION_REESTABLISHMENT_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RRC_CONNECTION_REESTABLISHMENT_FAILURE: Int
```

Radio resource control (RRC) connection re-establishment failure. 

 Value: 2149

### RRC_CONNECTION_REJECT_BY_NETWORK

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RRC_CONNECTION_REJECT_BY_NETWORK: Int
```

Radio resource control (RRC) connection establishment failed due to the network rejecting the UE connection request. 

 Value: 2146

### RRC_CONNECTION_RELEASED_SECURITY_NOT_ACTIVE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RRC_CONNECTION_RELEASED_SECURITY_NOT_ACTIVE: Int
```

If the UE has an LTE radio link failure before security is established, the radio resource control (RRC) connection must be released and the UE must return to idle. 

 Value: 2172

### RRC_CONNECTION_RF_UNAVAILABLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RRC_CONNECTION_RF_UNAVAILABLE: Int
```

Radio resource control (RRC) connection establishment failure due to the RF was unavailable. 

 Value: 2170

### RRC_CONNECTION_SYSTEM_INFORMATION_BLOCK_READ_ERROR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RRC_CONNECTION_SYSTEM_INFORMATION_BLOCK_READ_ERROR: Int
```

Radio resource control (RRC) connection released due to a system information block read error. 

 Value: 2152

### RRC_CONNECTION_SYSTEM_INTERVAL_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RRC_CONNECTION_SYSTEM_INTERVAL_FAILURE: Int
```

Connection establishment failed due to a service interval failure at the radio resource control (RRC). 

 Value: 2145

### RRC_CONNECTION_TIMER_EXPIRED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RRC_CONNECTION_TIMER_EXPIRED: Int
```

Radio resource control (RRC) connection could not be established in the time limit. 

 Value: 2142

### RRC_CONNECTION_TRACKING_AREA_ID_CHANGED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RRC_CONNECTION_TRACKING_AREA_ID_CHANGED: Int
```

Radio resource control (RRC) connection establishment failure due to a change in the tracking area ID. 

 Value: 2169

### RRC_UPLINK_CONNECTION_RELEASE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RRC_UPLINK_CONNECTION_RELEASE: Int
```

Radio resource control (RRC) uplink data delivery failed due to a connection release. 

 Value: 2134

### RRC_UPLINK_DATA_TRANSMISSION_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RRC_UPLINK_DATA_TRANSMISSION_FAILURE: Int
```

Transmission failure of radio resource control (RRC) uplink data. 

 Value: 2132

### RRC_UPLINK_DELIVERY_FAILED_DUE_TO_HANDOVER

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RRC_UPLINK_DELIVERY_FAILED_DUE_TO_HANDOVER: Int
```

Radio resource control (RRC) uplink data delivery failed due to a handover. 

 Value: 2133

### RRC_UPLINK_ERROR_REQUEST_FROM_NAS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RRC_UPLINK_ERROR_REQUEST_FROM_NAS: Int
```

Radio resource control (RRC) is not connected but the non-access stratum (NAS) sends an uplink data request. 

 Value: 2136

### RRC_UPLINK_RADIO_LINK_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RRC_UPLINK_RADIO_LINK_FAILURE: Int
```

Radio resource control (RRC) uplink data delivery failed due to a radio link failure. 

 Value: 2135

### RUIM_NOT_PRESENT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RUIM_NOT_PRESENT: Int
```

RUIM not being present. 

 Value: 2085

### SECURITY_MODE_REJECTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_MODE_REJECTED: Int
```

Unspecified security mode reject. 

 Value: 2186

### SERVICE_NOT_ALLOWED_ON_PLMN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SERVICE_NOT_ALLOWED_ON_PLMN: Int
```

Service is not allowed on the requested PLMN. 

 Value: 2129

### SERVICE_OPTION_NOT_SUBSCRIBED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SERVICE_OPTION_NOT_SUBSCRIBED: Int
```

Requested service option not subscribed. 

 Value: 33

### SERVICE_OPTION_NOT_SUPPORTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SERVICE_OPTION_NOT_SUPPORTED: Int
```

Service option not supported. 

 Value: 32

### SERVICE_OPTION_OUT_OF_ORDER

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SERVICE_OPTION_OUT_OF_ORDER: Int
```

Service option temporarily out of order. 

 Value: 34

### SIGNAL_LOST

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIGNAL_LOST: Int
```

Data call drop due to network/modem disconnect. 

 Value: -3

### SIM_CARD_CHANGED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIM_CARD_CHANGED: Int
```

Card was refreshed or removed. 

 Value: 2043

### SLICE_REJECTED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SLICE_REJECTED: Int
```

Data call fail due to the slice not being allowed for the data call. 

 Value: 2252

### SYNCHRONIZATION_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNCHRONIZATION_FAILURE: Int
```

Synchronization failure. 

 Value: 2184

### TEST_LOOPBACK_REGULAR_DEACTIVATION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TEST_LOOPBACK_REGULAR_DEACTIVATION: Int
```

Test loop-back data call has been successfully brought down. 

 Value: 2196

### TETHERED_CALL_ACTIVE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TETHERED_CALL_ACTIVE: Int
```

Data call was disconnected by modem because tethered. 

 Value: -6

### TFT_SEMANTIC_ERROR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TFT_SEMANTIC_ERROR: Int
```

Semantic error in the Traffic flow templates (TFT) operation. 

 Value: 41

### TFT_SYTAX_ERROR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TFT_SYTAX_ERROR: Int
```

Syntactical error in the Traffic flow templates (TFT) operation. 

 Value: 42

### THERMAL_EMERGENCY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val THERMAL_EMERGENCY: Int
```

Put device in thermal emergency. 

 Value: 2090

### THERMAL_MITIGATION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val THERMAL_MITIGATION: Int
```

Thermal level increases and causes calls to be torn down when normal mode of operation is not allowed. 

 Value: 2062

### TRAT_SWAP_FAILED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRAT_SWAP_FAILED: Int
```

Target RAT swap failed. 

 Value: 2048

### UE_INITIATED_DETACH_OR_DISCONNECT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UE_INITIATED_DETACH_OR_DISCONNECT: Int
```

UE performs a detach or disconnect PDN action based on TE requirements. 

 Value: 128

### UE_IS_ENTERING_POWERSAVE_MODE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UE_IS_ENTERING_POWERSAVE_MODE: Int
```

UE is entering power save mode. 

 Value: 2226

### UE_RAT_CHANGE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UE_RAT_CHANGE: Int
```

RAT change on the UE. 

 Value: 2105

### UE_SECURITY_CAPABILITIES_MISMATCH

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UE_SECURITY_CAPABILITIES_MISMATCH: Int
```

UE security capabilities mismatch. 

 Value: 2185

### UMTS_HANDOVER_TO_IWLAN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UMTS_HANDOVER_TO_IWLAN: Int
```

UMTS interface is brought down due to handover from UMTS to iWLAN. 

 Value: 2199

### UMTS_REACTIVATION_REQ

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UMTS_REACTIVATION_REQ: Int
```

Universal Mobile Telecommunications System (UMTS) reactivation request. 

 Value: 39

### UNACCEPTABLE_NETWORK_PARAMETER

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNACCEPTABLE_NETWORK_PARAMETER: Int
```

Data fail due to unacceptable network parameter. 

 Value: 65538

### UNACCEPTABLE_NON_EPS_AUTHENTICATION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNACCEPTABLE_NON_EPS_AUTHENTICATION: Int
```

Unacceptable non-EPS authentication. 

 Value: 2187

### UNKNOWN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNKNOWN: Int
```

Unknown data failure cause. 

 Value: 65536

### UNKNOWN_INFO_ELEMENT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNKNOWN_INFO_ELEMENT: Int
```

Unknown info element. 

 Value: 99

### UNKNOWN_PDP_ADDRESS_TYPE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNKNOWN_PDP_ADDRESS_TYPE: Int
```

Unknown Packet Data Protocol (PDP) address type. 

 Value: 28

### UNKNOWN_PDP_CONTEXT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNKNOWN_PDP_CONTEXT: Int
```

Unknown Packet Data Protocol (PDP) context. 

 Value: 43

### UNPREFERRED_RAT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNPREFERRED_RAT: Int
```

RAT on which the data call is attempted/connected is no longer the preferred RAT. 

 Value: 2039

### UNSUPPORTED_1X_PREV

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNSUPPORTED_1X_PREV: Int
```

P_rev supported by 1 base station is less than 6, which is not supported for a 1X data call. The UE must be in the footprint of BS which has p_rev \>= 6 to support this SO33 call. 

 Value: 2214

### UNSUPPORTED_APN_IN_CURRENT_PLMN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNSUPPORTED_APN_IN_CURRENT_PLMN: Int
```

Unsupported APN in current public land mobile network (PLMN). 

 Value: 66

### UNSUPPORTED_QCI_VALUE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNSUPPORTED_QCI_VALUE: Int
```

QCI (QoS Class Identifier) indicated in the UE request cannot be supported. 

 Value: 59

### USER_AUTHENTICATION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USER_AUTHENTICATION: Int
```

User authentication. 

 Value: 29

### VSNCP_ADMINISTRATIVELY_PROHIBITED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VSNCP_ADMINISTRATIVELY_PROHIBITED: Int
```

Data call bring up fails in the VSNCP phase due to a network rejection of the VSNCP configuration request with the reason of administratively prohibited at the HSGW. 

 Value: 2245

### VSNCP_APN_UNAUTHORIZED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VSNCP_APN_UNAUTHORIZED: Int
```

Data call bring up fails in the VSNCP phase due to a network rejection of the VSNCP configuration request because the requested APN is unauthorized. 

 Value: 2238

### VSNCP_GEN_ERROR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VSNCP_GEN_ERROR: Int
```

Data call bring up fails in the VSNCP phase due to a general error. It's used when there is no other specific error code available to report the failure. 

 Value: 2237

### VSNCP_INSUFFICIENT_PARAMETERS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VSNCP_INSUFFICIENT_PARAMETERS: Int
```

Data call bring up fails in the VSNCP phase due to a network rejection of the VSNCP configuration request with the reason of insufficient parameter. 

 Value: 2243

### VSNCP_NO_PDN_GATEWAY_ADDRESS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VSNCP_NO_PDN_GATEWAY_ADDRESS: Int
```

Data call bring up fails in the VSNCP phase due to the network rejected the VSNCP configuration request due to no PDN gateway address. 

 Value: 2240

### VSNCP_PDN_EXISTS_FOR_THIS_APN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VSNCP_PDN_EXISTS_FOR_THIS_APN: Int
```

Data call bring up fails in the VSNCP phase due to a network rejection of the VSNCP configuration request because the PDN exists for this APN. 

 Value: 2248

### VSNCP_PDN_GATEWAY_REJECT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VSNCP_PDN_GATEWAY_REJECT: Int
```

Data call bring up fails in the VSNCP phase due to a network rejection of the VSNCP configuration request due to a PDN gateway reject. 

 Value: 2242

### VSNCP_PDN_GATEWAY_UNREACHABLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VSNCP_PDN_GATEWAY_UNREACHABLE: Int
```

Data call bring up fails in the VSNCP phase due to a network rejection of the VSNCP configuration request because the PDN gateway is unreachable. 

 Value: 2241

### VSNCP_PDN_ID_IN_USE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VSNCP_PDN_ID_IN_USE: Int
```

Data call bring up fails in the VSNCP phase due to a network rejection of PDN ID in use, or all existing PDNs are brought down with this end reason because one of the PDN bring up was rejected by the network with the reason of PDN ID in use. 

 Value: 2246

### VSNCP_PDN_LIMIT_EXCEEDED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VSNCP_PDN_LIMIT_EXCEEDED: Int
```

Data call bring up fails in the VSNCP phase due to a network rejection of the VSNCP configuration request because the PDN limit has been exceeded. 

 Value: 2239

### VSNCP_RECONNECT_NOT_ALLOWED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VSNCP_RECONNECT_NOT_ALLOWED: Int
```

Data call bring up fails in the VSNCP phase due to a network rejection of the VSNCP configuration request with reconnect to this PDN not allowed, or an active data call is terminated by the network because reconnection to this PDN is not allowed. Upon receiving this error code from the network, the modem infinitely throttles the PDN until the next power cycle. 

 Value: 2249

### VSNCP_RESOURCE_UNAVAILABLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VSNCP_RESOURCE_UNAVAILABLE: Int
```

Data call bring up fails in the VSNCP phase due to a network rejection of the VSNCP configuration request with the reason of resource unavailable. 

 Value: 2244

### VSNCP_SUBSCRIBER_LIMITATION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VSNCP_SUBSCRIBER_LIMITATION: Int
```

Data call bring up fails in the VSNCP phase due to a network rejection of the VSNCP configuration request for the reason of subscriber limitation. 

 Value: 2247

### VSNCP_TIMEOUT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VSNCP_TIMEOUT: Int
```

Data call bring up fails in the VSNCP phase due to a VSNCP timeout error. 

 Value: 2236
