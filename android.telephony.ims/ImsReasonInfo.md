Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ImsReasonInfo

Kotlin | [Java](https://developer.android.com/reference/android/telephony/ims/ImsReasonInfo "View this page in Java")

```
class ImsReasonInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.telephony.ims.ImsReasonInfo](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#) |

Provides details on why an IMS call failed. Applications can use the methods in this class to get local or network fault behind an IMS services failure. For example, if the code is CODE_CALL_BARRED, then the call was blocked by network call barring configuration and it is not the device's bug and the user can retry the call when network lift the barring. Typical use case includes call backs when IMS call state changed with this class as a param containing details on why IMS call changed state/failed.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_ACCESS_CLASS_BLOCKED:kotlin.Int` Call failed because of access class barring |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_ANSWERED_ELSEWHERE:kotlin.Int` MT call has ended due to a release from the network because the call was answered elsewhere. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_BLACKLISTED_CALL_ID:kotlin.Int` Device declined a call due to a denylisted caller ID. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_CALL_BARRED:kotlin.Int` The call was blocked by call barring configuration. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_CALL_DROP_IWLAN_TO_LTE_UNAVAILABLE:kotlin.Int` CALL DROP error code for the case when a device is ePDG capable and when the user is on an active wifi call and at the edge of coverage and there is no qualified LTE network available to handover the call to. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_CALL_END_CAUSE_CALL_PULL:kotlin.Int` For MultiEndpoint - Call has been pulled from primary to secondary. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_CALL_PULL_OUT_OF_SYNC:kotlin.Int` For MultiEndpoint - Call Pull request has failed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_DATA_DISABLED:kotlin.Int` Indicates the call was disconnected due to the user disabling cellular data. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_DATA_LIMIT_REACHED:kotlin.Int` Indicates the call was disconnected due to the user reaching their data limit. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_DIAL_MODIFIED_TO_DIAL:kotlin.Int` Stk Call Control modified DIAL request to DIAL with modified data. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_DIAL_MODIFIED_TO_DIAL_VIDEO:kotlin.Int` Stk Call Control modified DIAL request to Video DIAL request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_DIAL_MODIFIED_TO_SS:kotlin.Int` Stk Call Control modified DIAL request to SS request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_DIAL_MODIFIED_TO_USSD:kotlin.Int` Stk Call Control modified DIAL request to USSD request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_DIAL_VIDEO_MODIFIED_TO_DIAL:kotlin.Int` Stk Call Control modified Video DIAL request to DIAL request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_DIAL_VIDEO_MODIFIED_TO_DIAL_VIDEO:kotlin.Int` Stk Call Control modified Video DIAL request to Video DIAL request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_DIAL_VIDEO_MODIFIED_TO_SS:kotlin.Int` Stk Call Control modified Video DIAL request to SS request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_DIAL_VIDEO_MODIFIED_TO_USSD:kotlin.Int` Stk Call Control modified Video DIAL request to USSD request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_ECBM_NOT_SUPPORTED:kotlin.Int` Emergency callback mode is not supported. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_EMERGENCY_PERM_FAILURE:kotlin.Int` Emergency call failed in the modem with a permanent fail cause and should not be redialed on this slot. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_EMERGENCY_TEMP_FAILURE:kotlin.Int` Emergency call failed in the modem with a temporary fail cause and should be redialed on this slot. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_EPDG_TUNNEL_ESTABLISH_FAILURE:kotlin.Int` Establishment of the ePDG Tunnel Failed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_EPDG_TUNNEL_LOST_CONNECTION:kotlin.Int` Connection to the packet gateway is lost. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_EPDG_TUNNEL_REKEY_FAILURE:kotlin.Int` Re-keying of the ePDG Tunnel Failed; may not always result in teardown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_FDN_BLOCKED:kotlin.Int` The operation is restricted to fixed dialing numbers only. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_IKEV2_AUTH_FAILURE:kotlin.Int` Indicates the registration attempt on IWLAN failed due to IKEv2 authetication failure during tunnel establishment. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_IMEI_NOT_ACCEPTED:kotlin.Int` Network rejected the emergency call request because IMEI was used as identification and this capability is not supported by the network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_IWLAN_DPD_FAILURE:kotlin.Int` DPD Procedure received no response or send failed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_CALL_BUSY:kotlin.Int` The call is busy. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_CALL_CS_RETRY_REQUIRED:kotlin.Int` VoLTE service can't be provided by the network or remote end, retry the call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_CALL_DECLINE:kotlin.Int` The Call has been declined locally on this device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_CALL_EXCEEDED:kotlin.Int` Maximum number of simultaneous calls exceeded |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_CALL_RESOURCE_RESERVATION_FAILED:kotlin.Int` Can not complete call; resource reservation is failed (QoS precondition) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_CALL_TERMINATED:kotlin.Int` IMS call is already terminated (in TERMINATED state). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_CALL_VCC_ON_PROGRESSING:kotlin.Int` Can not complete call; an SRVCC is in progress. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_CALL_VOLTE_RETRY_REQUIRED:kotlin.Int` VoLTE service can't be provided by the network temporarily, retry the call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_ENDED_BY_CONFERENCE_MERGE:kotlin.Int` IMS Call ended during conference merge process |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_HO_NOT_FEASIBLE:kotlin.Int` Call was disconnected because a handover is not feasible due to network conditions. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_ILLEGAL_ARGUMENT:kotlin.Int` The passed argument is invalid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_ILLEGAL_STATE:kotlin.Int` The operation was invoked while in an invalid call state. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_IMS_SERVICE_DOWN:kotlin.Int` ImsService has crashed (service connection is lost). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_INTERNAL_ERROR:kotlin.Int` IMS service internal error |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_LOW_BATTERY:kotlin.Int` Service unavailable; low battery |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_NETWORK_IP_CHANGED:kotlin.Int` Service unavailable; IP changed |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_NETWORK_NO_LTE_COVERAGE:kotlin.Int` Service unavailable; no LTE coverage (VoLTE is not supported even though IMS is registered) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_NETWORK_NO_SERVICE:kotlin.Int` Service unavailable; out of service (data service state) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_NETWORK_ROAMING:kotlin.Int` Service unavailable; located in roaming area |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_NOT_REGISTERED:kotlin.Int` Service unavailable; IMS is not registered |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_NO_PENDING_CALL:kotlin.Int` No pending incoming call exists |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_POWER_OFF:kotlin.Int` Service unavailable; radio power off |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_SERVICE_UNAVAILABLE:kotlin.Int` Service unavailable; for an unspecified reason |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOW_BATTERY:kotlin.Int` Device declined/ended a call due to a low battery condition. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_MAXIMUM_NUMBER_OF_CALLS_REACHED:kotlin.Int` The maximum number of calls allowed has been reached. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_MEDIA_INIT_FAILED:kotlin.Int` Media resource initialization failed |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_MEDIA_NOT_ACCEPTABLE:kotlin.Int` Media is not supported; so dropped the call |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_MEDIA_NO_DATA:kotlin.Int` RTP timeout (no audio / video traffic in the session) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_MEDIA_UNSPECIFIED:kotlin.Int` Unspecified media related error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_MULTIENDPOINT_NOT_SUPPORTED:kotlin.Int` Fail code used to indicate that Multi-endpoint is not supported by the IMS framework. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_NETWORK_CONGESTION:kotlin.Int` Call failed because of network congestion, resource is not available, or no circuit or channel available, etc. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_NETWORK_DETACH:kotlin.Int` Call/IMS registration is failed/dropped because of a network detach |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_NETWORK_REJECT:kotlin.Int` The failure is due to explicit reject from network |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_NETWORK_RESP_TIMEOUT:kotlin.Int` The failure is due to UE timer expired while waiting for a response from network |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_NO_CSFB_IN_CS_ROAM:kotlin.Int` Call failed because WiFi call could not complete and circuit switch silent redial is not allowed while roaming on another network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_NO_VALID_SIM:kotlin.Int` The call cannot be established because of no valid SIM |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_1:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_10:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_11:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_12:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_13:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_14:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_15:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_2:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_3:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_4:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_5:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_6:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_7:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_8:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_9:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_RADIO_ACCESS_FAILURE:kotlin.Int` The failure is due to radio access failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_RADIO_INTERNAL_ERROR:kotlin.Int` The failure is due internal error at modem |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_RADIO_LINK_FAILURE:kotlin.Int` Call/IMS registration failed/dropped because of a RLF |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_RADIO_LINK_LOST:kotlin.Int` Call/IMS registration failed/dropped because of radio link lost |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_RADIO_OFF:kotlin.Int` The call cannot be established because RADIO is OFF |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_RADIO_RELEASE_ABNORMAL:kotlin.Int` Call failed/dropped because of RRC abnormally released by modem/network |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_RADIO_RELEASE_NORMAL:kotlin.Int` Call failed/dropped because of RRC connection release from NW |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_RADIO_SETUP_FAILURE:kotlin.Int` Call failed because of a RRC connection setup failure |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_RADIO_UPLINK_FAILURE:kotlin.Int` The call Call/IMS registration failed because of a radio uplink issue |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REGISTRATION_ERROR:kotlin.Int` IMS Registration error code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECTED_ELSEWHERE:kotlin.Int` For MultiEndPoint - Call was rejected elsewhere |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_1X_COLLISION:kotlin.Int` CDMA call collision. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_CALL_ON_OTHER_SUB:kotlin.Int` A call is ongoing on another sub. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_CALL_TYPE_NOT_ALLOWED:kotlin.Int` The call type is not allowed on the current RAT. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_CONFERENCE_TTY_NOT_ALLOWED:kotlin.Int` Call from conference server, when TTY mode is ON. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_INTERNAL_ERROR:kotlin.Int` An internal error occured while processing the call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_MAX_CALL_LIMIT_REACHED:kotlin.Int` Maximum number of allowed calls are already in progress. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_ONGOING_CALL_SETUP:kotlin.Int` Another call is in the process of being establilshed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_ONGOING_CALL_TRANSFER:kotlin.Int` A call transfer is in progress. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_ONGOING_CALL_UPGRADE:kotlin.Int` A call upgrade is in progress. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_ONGOING_CALL_WAITING_DISABLED:kotlin.Int` Ongoing call, and call waiting is disabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_ONGOING_CONFERENCE_CALL:kotlin.Int` A conference call is ongoing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_ONGOING_CS_CALL:kotlin.Int` A CS call is ongoing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_ONGOING_E911_CALL:kotlin.Int` And emergency call is ongoing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_ONGOING_ENCRYPTED_CALL:kotlin.Int` And encrypted call is ongoing; other calls not supported. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_ONGOING_HANDOVER:kotlin.Int` A call handover is in progress. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_QOS_FAILURE:kotlin.Int` Call failure due to lack of dedicated bearer. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_SERVICE_NOT_REGISTERED:kotlin.Int` IMS is not registered for service yet. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_UNKNOWN:kotlin.Int` The rejection cause is not known. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_UNSUPPORTED_SDP_HEADERS:kotlin.Int` Invalid/unsupported SDP headers received. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_UNSUPPORTED_SIP_HEADERS:kotlin.Int` Invalid/unsupported SIP headers received. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_VT_AVPF_NOT_ALLOWED:kotlin.Int` A video call with AVPF is not supported. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_VT_TTY_NOT_ALLOWED:kotlin.Int` Video calling not supported with TTY. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REMOTE_CALL_DECLINE:kotlin.Int` Similar to `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_CALL_DECLINE:kotlin.Int`, except indicates that a remote device has declined the call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SESSION_MODIFICATION_FAILED:kotlin.Int` UPGRADE DOWNGRADE operation failed This can happen due to failure from SIP/RTP/SDP generation or a Call end is triggered/received while Reinvite is in progress. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_ALTERNATE_EMERGENCY_CALL:kotlin.Int` Call failed due to SIP code 380 (Alternative Service response) while dialing an "undetected emergency number". |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_AMBIGUOUS:kotlin.Int` SIP Response : 485 Request-URI is ambiguous |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_BAD_ADDRESS:kotlin.Int` SIP response 484 : Address Incomplete |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_BAD_REQUEST:kotlin.Int` Sip 400 response : Bad Request |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_BUSY:kotlin.Int` Returned a busy response, may be one of the following: SIP response 486 : Busy Here, SIP response 600 : Busy Everywhere |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_CALL_OR_TRANS_DOES_NOT_EXIST:kotlin.Int` SIP Response : 481 Request received by the server does not match any dialog or transaction |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_CLIENT_ERROR:kotlin.Int` Received another unspecified error SIP response from the client. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_EXTENSION_REQUIRED:kotlin.Int` SIP Response : 421 Specific extension is required, which is not present in the HEADER |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_FORBIDDEN:kotlin.Int` Sip 403 response : Forbidden |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_GLOBAL_ERROR:kotlin.Int` Unspecified 6xx error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_INTERVAL_TOO_BRIEF:kotlin.Int` SIP Response : 422 The session expiration field too small |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_LOOP_DETECTED:kotlin.Int` SIP Response : 482 Server has detected a loop |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_METHOD_NOT_ALLOWED:kotlin.Int` SIP Response : 405 Method not allowed for the address in the Request URI |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_NOT_ACCEPTABLE:kotlin.Int` Received a not acceptable response, will be one of the following: SIP response 406 : Not Acceptable SIP response 488 : Not Acceptable Here SIP response 606 : Not Acceptable |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_NOT_FOUND:kotlin.Int` Sip 404 response : Not Found |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_NOT_REACHABLE:kotlin.Int` Received a not acceptable response, will be one of the following: SIP response 410 : Gone SIP response 604 : Does Not Exist Anywhere |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_NOT_SUPPORTED:kotlin.Int` Not supported, because of one of the following: SIP response 415 : Unsupported Media Type, SIP response 416 : Unsupported URI Scheme, SIP response 420 : Bad Extension |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_PROXY_AUTHENTICATION_REQUIRED:kotlin.Int` SIP Response : 407 The request requires user authentication |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_REDIRECTED:kotlin.Int` SIP 3xx response: SIP request is redirected |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_REQUEST_CANCELLED:kotlin.Int` SIP response 487 : Request Terminated |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_REQUEST_ENTITY_TOO_LARGE:kotlin.Int` SIP Response : 413 Request body too large |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_REQUEST_PENDING:kotlin.Int` SIP Response : 491 Server has pending request for same dialog |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_REQUEST_TIMEOUT:kotlin.Int` SIP response 408 : Request Timeout. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_REQUEST_URI_TOO_LARGE:kotlin.Int` SIP Response : 414 Request-URI too large |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_SERVER_ERROR:kotlin.Int` Received an unspecified SIP server error response. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_SERVER_INTERNAL_ERROR:kotlin.Int` SIP response 501 : Server Internal Error |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_SERVER_TIMEOUT:kotlin.Int` SIP response 504 : Server Time-out |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_SERVICE_UNAVAILABLE:kotlin.Int` SIP response 503 : Service Unavailable |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_TEMPRARILY_UNAVAILABLE:kotlin.Int` SIP response 480 : Temporarily Unavailable |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_TOO_MANY_HOPS:kotlin.Int` SIP Response : 483 Max-Forwards value reached |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_TRANSACTION_DOES_NOT_EXIST:kotlin.Int` SIP response 481: Transaction Does Not Exist |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_UNDECIPHERABLE:kotlin.Int` SIP Response : 493 The request cannot be decrypted by recipient |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_USER_MARKED_UNWANTED:kotlin.Int` Call failure code during hangup/reject if user marked the call as unwanted. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_USER_REJECTED:kotlin.Int` 603 : Decline |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SUPP_SVC_CANCELLED:kotlin.Int` Supplementary Services (HOLD/RESUME) - the command was cancelled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SUPP_SVC_FAILED:kotlin.Int` Supplementary Services (HOLD/RESUME) - the command failed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SUPP_SVC_REINVITE_COLLISION:kotlin.Int` Supplementary Services (HOLD/RESUME) - the command resulted in a re-invite collision. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_TIMEOUT_1XX_WAITING:kotlin.Int` 1xx waiting timer is expired after sending INVITE request (MO calls only) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_TIMEOUT_NO_ANSWER:kotlin.Int` User didn't answer during call setup operation (MO/MT) MO : 200 OK to INVITE request is not received, MT : No action from user after alerting the call |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_TIMEOUT_NO_ANSWER_CALL_UPDATE:kotlin.Int` User no answer during call update operation (MO/MT) MO : 200 OK to re-INVITE request is not received, MT : No action from user after alerting the call |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_UNSPECIFIED:kotlin.Int` The Reason is unspecified. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_USER_CANCELLED_SESSION_MODIFICATION:kotlin.Int` Upgrade Downgrade request cancelled by the user who initiated it |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_USER_DECLINE:kotlin.Int` User declined an incoming call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_USER_IGNORE:kotlin.Int` User ignored an incoming call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_USER_NOANSWER:kotlin.Int` No action was taken while an incoming call was ringing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_USER_REJECTED_SESSION_MODIFICATION:kotlin.Int` Upgrade Downgrade request rejected by Remote user if the request is MO initiated Local user if the request is MT initiated |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_USER_TERMINATED:kotlin.Int` User triggers the call to be terminated. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_USER_TERMINATED_BY_REMOTE:kotlin.Int` The call has been terminated by the network or remote user. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_UT_CB_PASSWORD_MISMATCH:kotlin.Int` The password entered for UT operations does not match the stored password. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_UT_NETWORK_ERROR:kotlin.Int` The UT request resulted in a network error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_UT_NOT_SUPPORTED:kotlin.Int` UT is currently not supported on this device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_UT_OPERATION_NOT_ALLOWED:kotlin.Int` The requested UT operation is not allowed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_UT_SERVICE_UNAVAILABLE:kotlin.Int` UT services are currently not available on this device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_UT_SS_MODIFIED_TO_DIAL:kotlin.Int` Sim Toolkit Call Control modified the UT operation to a dial command. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_UT_SS_MODIFIED_TO_DIAL_VIDEO:kotlin.Int` Sim Toolkit Call Control modified the UT operation to a video call dial command. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_UT_SS_MODIFIED_TO_SS:kotlin.Int` Sim Toolkit Call Control modified the UT operation to another supplementary service command. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_UT_SS_MODIFIED_TO_USSD:kotlin.Int` Sim Toolkit Call Control modified the UT operation to a USSD command. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_WIFI_LOST:kotlin.Int` Indicates a call was disconnected due to loss of wifi signal. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#EXTRA_CODE_CALL_RETRY_BY_SETTINGS:kotlin.Int` An extra that may be populated when the `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_CALL_CS_RETRY_REQUIRED:kotlin.Int` result has been returned. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#EXTRA_CODE_CALL_RETRY_EMERGENCY:kotlin.Int` An extra that may be populated when the `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_CALL_CS_RETRY_REQUIRED:kotlin.Int` result has been returned. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#EXTRA_CODE_CALL_RETRY_NORMAL:kotlin.Int` An extra that may be populated when the `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_CALL_CS_RETRY_REQUIRED:kotlin.Int` result has been returned. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#EXTRA_CODE_CALL_RETRY_SILENT_REDIAL:kotlin.Int` An extra that may be populated when the `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_CALL_CS_RETRY_REQUIRED:kotlin.Int` result has been returned. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#ImsReasonInfo(kotlin.Int,%20kotlin.Int,%20kotlin.String)(code: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, extraCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, extraMessage: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` <br /> |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#getCode()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#getExtraCode()()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#getExtraMessage()()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#toString()()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#writeToParcel(android.os.Parcel,%20kotlin.Int)(out: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [ImsReasonInfo](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#)!\> | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### CODE_ACCESS_CLASS_BLOCKED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_ACCESS_CLASS_BLOCKED: Int
```

Call failed because of access class barring

 Value: 1512

### CODE_ANSWERED_ELSEWHERE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_ANSWERED_ELSEWHERE: Int
```

MT call has ended due to a release from the network because the call was answered elsewhere.

 Value: 1014

### CODE_BLACKLISTED_CALL_ID

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_BLACKLISTED_CALL_ID: Int
```

Device declined a call due to a denylisted caller ID.

 Value: 506

### CODE_CALL_BARRED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_CALL_BARRED: Int
```

The call was blocked by call barring configuration.

 Value: 240

### CODE_CALL_DROP_IWLAN_TO_LTE_UNAVAILABLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_CALL_DROP_IWLAN_TO_LTE_UNAVAILABLE: Int
```

CALL DROP error code for the case when a device is ePDG capable and when the user is on an active wifi call and at the edge of coverage and there is no qualified LTE network available to handover the call to. We get a handover NOT_TRIGERRED message from the modem. This error code is received as part of the handover message.

 Value: 1100

### CODE_CALL_END_CAUSE_CALL_PULL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_CALL_END_CAUSE_CALL_PULL: Int
```

For MultiEndpoint - Call has been pulled from primary to secondary.

 Value: 1016

### CODE_CALL_PULL_OUT_OF_SYNC

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_CALL_PULL_OUT_OF_SYNC: Int
```

For MultiEndpoint - Call Pull request has failed.

 Value: 1015

### CODE_DATA_DISABLED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_DATA_DISABLED: Int
```

Indicates the call was disconnected due to the user disabling cellular data.

 Value: 1406

### CODE_DATA_LIMIT_REACHED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_DATA_LIMIT_REACHED: Int
```

Indicates the call was disconnected due to the user reaching their data limit.

 Value: 1405

### CODE_DIAL_MODIFIED_TO_DIAL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_DIAL_MODIFIED_TO_DIAL: Int
```

Stk Call Control modified DIAL request to DIAL with modified data.

 Value: 246

### CODE_DIAL_MODIFIED_TO_DIAL_VIDEO

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_DIAL_MODIFIED_TO_DIAL_VIDEO: Int
```

Stk Call Control modified DIAL request to Video DIAL request.

 Value: 247

### CODE_DIAL_MODIFIED_TO_SS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_DIAL_MODIFIED_TO_SS: Int
```

Stk Call Control modified DIAL request to SS request.

 Value: 245

### CODE_DIAL_MODIFIED_TO_USSD

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_DIAL_MODIFIED_TO_USSD: Int
```

Stk Call Control modified DIAL request to USSD request.

 Value: 244

### CODE_DIAL_VIDEO_MODIFIED_TO_DIAL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_DIAL_VIDEO_MODIFIED_TO_DIAL: Int
```

Stk Call Control modified Video DIAL request to DIAL request.

 Value: 248

### CODE_DIAL_VIDEO_MODIFIED_TO_DIAL_VIDEO

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_DIAL_VIDEO_MODIFIED_TO_DIAL_VIDEO: Int
```

Stk Call Control modified Video DIAL request to Video DIAL request.

 Value: 249

### CODE_DIAL_VIDEO_MODIFIED_TO_SS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_DIAL_VIDEO_MODIFIED_TO_SS: Int
```

Stk Call Control modified Video DIAL request to SS request.

 Value: 250

### CODE_DIAL_VIDEO_MODIFIED_TO_USSD

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_DIAL_VIDEO_MODIFIED_TO_USSD: Int
```

Stk Call Control modified Video DIAL request to USSD request.

 Value: 251

### CODE_ECBM_NOT_SUPPORTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_ECBM_NOT_SUPPORTED: Int
```

Emergency callback mode is not supported.

 Value: 901

### CODE_EMERGENCY_PERM_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_EMERGENCY_PERM_FAILURE: Int
```

Emergency call failed in the modem with a permanent fail cause and should not be redialed on this slot. If there are any other slots available for emergency calling, try those.

 Value: 364

### CODE_EMERGENCY_TEMP_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_EMERGENCY_TEMP_FAILURE: Int
```

Emergency call failed in the modem with a temporary fail cause and should be redialed on this slot.

 Value: 363

### CODE_EPDG_TUNNEL_ESTABLISH_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_EPDG_TUNNEL_ESTABLISH_FAILURE: Int
```

Establishment of the ePDG Tunnel Failed.

 Value: 1400

### CODE_EPDG_TUNNEL_LOST_CONNECTION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_EPDG_TUNNEL_LOST_CONNECTION: Int
```

Connection to the packet gateway is lost.

 Value: 1402

### CODE_EPDG_TUNNEL_REKEY_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_EPDG_TUNNEL_REKEY_FAILURE: Int
```

Re-keying of the ePDG Tunnel Failed; may not always result in teardown.

 Value: 1401

### CODE_FDN_BLOCKED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_FDN_BLOCKED: Int
```

The operation is restricted to fixed dialing numbers only.

 Value: 241

### CODE_IKEV2_AUTH_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_IKEV2_AUTH_FAILURE: Int
```

Indicates the registration attempt on IWLAN failed due to IKEv2 authetication failure during tunnel establishment.

 Value: 1408

### CODE_IMEI_NOT_ACCEPTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_IMEI_NOT_ACCEPTED: Int
```

Network rejected the emergency call request because IMEI was used as identification and this capability is not supported by the network.

 Value: 243

### CODE_IWLAN_DPD_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_IWLAN_DPD_FAILURE: Int
```

DPD Procedure received no response or send failed.

 Value: 1300

### CODE_LOCAL_CALL_BUSY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_LOCAL_CALL_BUSY: Int
```

The call is busy.

 Value: 142

### CODE_LOCAL_CALL_CS_RETRY_REQUIRED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_LOCAL_CALL_CS_RETRY_REQUIRED: Int
```

VoLTE service can't be provided by the network or remote end, retry the call. Resolve the extra code provided in (EXTRA_CODE_CALL_RETRY_\*) if the below code is set

 Value: 146

### CODE_LOCAL_CALL_DECLINE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_LOCAL_CALL_DECLINE: Int
```

The Call has been declined locally on this device.

 Value: 143

### CODE_LOCAL_CALL_EXCEEDED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_LOCAL_CALL_EXCEEDED: Int
```

Maximum number of simultaneous calls exceeded

 Value: 141

### CODE_LOCAL_CALL_RESOURCE_RESERVATION_FAILED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_LOCAL_CALL_RESOURCE_RESERVATION_FAILED: Int
```

Can not complete call; resource reservation is failed (QoS precondition)

 Value: 145

### CODE_LOCAL_CALL_TERMINATED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_LOCAL_CALL_TERMINATED: Int
```

IMS call is already terminated (in TERMINATED state).

 Value: 148

### CODE_LOCAL_CALL_VCC_ON_PROGRESSING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_LOCAL_CALL_VCC_ON_PROGRESSING: Int
```

Can not complete call; an SRVCC is in progress.

 Value: 144

### CODE_LOCAL_CALL_VOLTE_RETRY_REQUIRED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_LOCAL_CALL_VOLTE_RETRY_REQUIRED: Int
```

VoLTE service can't be provided by the network temporarily, retry the call.

 Value: 147

### CODE_LOCAL_ENDED_BY_CONFERENCE_MERGE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_LOCAL_ENDED_BY_CONFERENCE_MERGE: Int
```

IMS Call ended during conference merge process

 Value: 108

### CODE_LOCAL_HO_NOT_FEASIBLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_LOCAL_HO_NOT_FEASIBLE: Int
```

Call was disconnected because a handover is not feasible due to network conditions.

 Value: 149

### CODE_LOCAL_ILLEGAL_ARGUMENT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_LOCAL_ILLEGAL_ARGUMENT: Int
```

The passed argument is invalid.

 Value: 101

### CODE_LOCAL_ILLEGAL_STATE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_LOCAL_ILLEGAL_STATE: Int
```

The operation was invoked while in an invalid call state.

 Value: 102

### CODE_LOCAL_IMS_SERVICE_DOWN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_LOCAL_IMS_SERVICE_DOWN: Int
```

ImsService has crashed (service connection is lost).

 Value: 106

### CODE_LOCAL_INTERNAL_ERROR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_LOCAL_INTERNAL_ERROR: Int
```

IMS service internal error

 Value: 103

### CODE_LOCAL_LOW_BATTERY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_LOCAL_LOW_BATTERY: Int
```

Service unavailable; low battery

 Value: 112

### CODE_LOCAL_NETWORK_IP_CHANGED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_LOCAL_NETWORK_IP_CHANGED: Int
```

Service unavailable; IP changed

 Value: 124

### CODE_LOCAL_NETWORK_NO_LTE_COVERAGE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_LOCAL_NETWORK_NO_LTE_COVERAGE: Int
```

Service unavailable; no LTE coverage (VoLTE is not supported even though IMS is registered)

 Value: 122

### CODE_LOCAL_NETWORK_NO_SERVICE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_LOCAL_NETWORK_NO_SERVICE: Int
```

Service unavailable; out of service (data service state)

 Value: 121

### CODE_LOCAL_NETWORK_ROAMING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_LOCAL_NETWORK_ROAMING: Int
```

Service unavailable; located in roaming area

 Value: 123

### CODE_LOCAL_NOT_REGISTERED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_LOCAL_NOT_REGISTERED: Int
```

Service unavailable; IMS is not registered

 Value: 132

### CODE_LOCAL_NO_PENDING_CALL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_LOCAL_NO_PENDING_CALL: Int
```

No pending incoming call exists

 Value: 107

### CODE_LOCAL_POWER_OFF

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_LOCAL_POWER_OFF: Int
```

Service unavailable; radio power off

 Value: 111

### CODE_LOCAL_SERVICE_UNAVAILABLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_LOCAL_SERVICE_UNAVAILABLE: Int
```

Service unavailable; for an unspecified reason

 Value: 131

### CODE_LOW_BATTERY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_LOW_BATTERY: Int
```

Device declined/ended a call due to a low battery condition.

 Value: 505

### CODE_MAXIMUM_NUMBER_OF_CALLS_REACHED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_MAXIMUM_NUMBER_OF_CALLS_REACHED: Int
```

The maximum number of calls allowed has been reached. Used in a multi-endpoint scenario where the number of calls across all connected devices has reached the maximum.

 Value: 1403

### CODE_MEDIA_INIT_FAILED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_MEDIA_INIT_FAILED: Int
```

Media resource initialization failed

 Value: 401

### CODE_MEDIA_NOT_ACCEPTABLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_MEDIA_NOT_ACCEPTABLE: Int
```

Media is not supported; so dropped the call

 Value: 403

### CODE_MEDIA_NO_DATA

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_MEDIA_NO_DATA: Int
```

RTP timeout (no audio / video traffic in the session)

 Value: 402

### CODE_MEDIA_UNSPECIFIED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_MEDIA_UNSPECIFIED: Int
```

Unspecified media related error.

 Value: 404

### CODE_MULTIENDPOINT_NOT_SUPPORTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_MULTIENDPOINT_NOT_SUPPORTED: Int
```

Fail code used to indicate that Multi-endpoint is not supported by the IMS framework.

 Value: 902

### CODE_NETWORK_CONGESTION

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_NETWORK_CONGESTION: Int
```

Call failed because of network congestion, resource is not available, or no circuit or channel available, etc.

 Value: 1624

### CODE_NETWORK_DETACH

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_NETWORK_DETACH: Int
```

Call/IMS registration is failed/dropped because of a network detach

 Value: 1513

### CODE_NETWORK_REJECT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_NETWORK_REJECT: Int
```

The failure is due to explicit reject from network

 Value: 1504

### CODE_NETWORK_RESP_TIMEOUT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_NETWORK_RESP_TIMEOUT: Int
```

The failure is due to UE timer expired while waiting for a response from network

 Value: 1503

### CODE_NO_CSFB_IN_CS_ROAM

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_NO_CSFB_IN_CS_ROAM: Int
```

Call failed because WiFi call could not complete and circuit switch silent redial is not allowed while roaming on another network.

 Value: 1516

### CODE_NO_VALID_SIM

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_NO_VALID_SIM: Int
```

The call cannot be established because of no valid SIM

 Value: 1501

### CODE_OEM_CAUSE_1

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_OEM_CAUSE_1: Int
```

 Value: 61441

### CODE_OEM_CAUSE_10

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_OEM_CAUSE_10: Int
```

 Value: 61450

### CODE_OEM_CAUSE_11

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_OEM_CAUSE_11: Int
```

 Value: 61451

### CODE_OEM_CAUSE_12

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_OEM_CAUSE_12: Int
```

 Value: 61452

### CODE_OEM_CAUSE_13

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_OEM_CAUSE_13: Int
```

 Value: 61453

### CODE_OEM_CAUSE_14

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_OEM_CAUSE_14: Int
```

 Value: 61454

### CODE_OEM_CAUSE_15

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_OEM_CAUSE_15: Int
```

 Value: 61455

### CODE_OEM_CAUSE_2

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_OEM_CAUSE_2: Int
```

 Value: 61442

### CODE_OEM_CAUSE_3

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_OEM_CAUSE_3: Int
```

 Value: 61443

### CODE_OEM_CAUSE_4

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_OEM_CAUSE_4: Int
```

 Value: 61444

### CODE_OEM_CAUSE_5

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_OEM_CAUSE_5: Int
```

 Value: 61445

### CODE_OEM_CAUSE_6

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_OEM_CAUSE_6: Int
```

 Value: 61446

### CODE_OEM_CAUSE_7

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_OEM_CAUSE_7: Int
```

 Value: 61447

### CODE_OEM_CAUSE_8

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_OEM_CAUSE_8: Int
```

 Value: 61448

### CODE_OEM_CAUSE_9

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_OEM_CAUSE_9: Int
```

 Value: 61449

### CODE_RADIO_ACCESS_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_RADIO_ACCESS_FAILURE: Int
```

The failure is due to radio access failure. ex. RACH failure

 Value: 1505

### CODE_RADIO_INTERNAL_ERROR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_RADIO_INTERNAL_ERROR: Int
```

The failure is due internal error at modem

 Value: 1502

### CODE_RADIO_LINK_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_RADIO_LINK_FAILURE: Int
```

Call/IMS registration failed/dropped because of a RLF

 Value: 1506

### CODE_RADIO_LINK_LOST

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_RADIO_LINK_LOST: Int
```

Call/IMS registration failed/dropped because of radio link lost

 Value: 1507

### CODE_RADIO_OFF

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_RADIO_OFF: Int
```

The call cannot be established because RADIO is OFF

 Value: 1500

### CODE_RADIO_RELEASE_ABNORMAL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_RADIO_RELEASE_ABNORMAL: Int
```

Call failed/dropped because of RRC abnormally released by modem/network

 Value: 1511

### CODE_RADIO_RELEASE_NORMAL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_RADIO_RELEASE_NORMAL: Int
```

Call failed/dropped because of RRC connection release from NW

 Value: 1510

### CODE_RADIO_SETUP_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_RADIO_SETUP_FAILURE: Int
```

Call failed because of a RRC connection setup failure

 Value: 1509

### CODE_RADIO_UPLINK_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_RADIO_UPLINK_FAILURE: Int
```

The call Call/IMS registration failed because of a radio uplink issue

 Value: 1508

### CODE_REGISTRATION_ERROR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_REGISTRATION_ERROR: Int
```

IMS Registration error code

 Value: 1000

### CODE_REJECTED_ELSEWHERE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_REJECTED_ELSEWHERE: Int
```

For MultiEndPoint - Call was rejected elsewhere

 Value: 1017

### CODE_REJECT_1X_COLLISION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_REJECT_1X_COLLISION: Int
```

CDMA call collision.

Used with implicit call rejection.

 Value: 1603

### CODE_REJECT_CALL_ON_OTHER_SUB

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_REJECT_CALL_ON_OTHER_SUB: Int
```

A call is ongoing on another sub.

Used with implicit call rejection.

 Value: 1602

### CODE_REJECT_CALL_TYPE_NOT_ALLOWED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_REJECT_CALL_TYPE_NOT_ALLOWED: Int
```

The call type is not allowed on the current RAT.

Used with implicit call rejection.

 Value: 1605

### CODE_REJECT_CONFERENCE_TTY_NOT_ALLOWED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_REJECT_CONFERENCE_TTY_NOT_ALLOWED: Int
```

Call from conference server, when TTY mode is ON.

Used with implicit call rejection.

 Value: 1617

### CODE_REJECT_INTERNAL_ERROR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_REJECT_INTERNAL_ERROR: Int
```

An internal error occured while processing the call.

Used with implicit call rejection.

 Value: 1612

### CODE_REJECT_MAX_CALL_LIMIT_REACHED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_REJECT_MAX_CALL_LIMIT_REACHED: Int
```

Maximum number of allowed calls are already in progress.

Used with implicit call rejection.

 Value: 1608

### CODE_REJECT_ONGOING_CALL_SETUP

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_REJECT_ONGOING_CALL_SETUP: Int
```

Another call is in the process of being establilshed.

Used with implicit call rejection.

 Value: 1607

### CODE_REJECT_ONGOING_CALL_TRANSFER

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_REJECT_ONGOING_CALL_TRANSFER: Int
```

A call transfer is in progress.

Used with implicit call rejection.

 Value: 1611

### CODE_REJECT_ONGOING_CALL_UPGRADE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_REJECT_ONGOING_CALL_UPGRADE: Int
```

A call upgrade is in progress.

Used with implicit call rejection.

 Value: 1616

### CODE_REJECT_ONGOING_CALL_WAITING_DISABLED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_REJECT_ONGOING_CALL_WAITING_DISABLED: Int
```

Ongoing call, and call waiting is disabled.

Used with implicit call rejection.

 Value: 1601

### CODE_REJECT_ONGOING_CONFERENCE_CALL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_REJECT_ONGOING_CONFERENCE_CALL: Int
```

A conference call is ongoing.

Used with implicit call rejection.

 Value: 1618

### CODE_REJECT_ONGOING_CS_CALL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_REJECT_ONGOING_CS_CALL: Int
```

A CS call is ongoing.

Used with implicit call rejection.

 Value: 1621

### CODE_REJECT_ONGOING_E911_CALL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_REJECT_ONGOING_E911_CALL: Int
```

And emergency call is ongoing.

Used with implicit call rejection.

 Value: 1606

### CODE_REJECT_ONGOING_ENCRYPTED_CALL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_REJECT_ONGOING_ENCRYPTED_CALL: Int
```

And encrypted call is ongoing; other calls not supported.

Used with implicit call rejection.

 Value: 1620

### CODE_REJECT_ONGOING_HANDOVER

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_REJECT_ONGOING_HANDOVER: Int
```

A call handover is in progress.

Used with implicit call rejection.

 Value: 1614

### CODE_REJECT_QOS_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_REJECT_QOS_FAILURE: Int
```

Call failure due to lack of dedicated bearer.

Used with implicit call rejection.

 Value: 1613

### CODE_REJECT_SERVICE_NOT_REGISTERED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_REJECT_SERVICE_NOT_REGISTERED: Int
```

IMS is not registered for service yet.

Used with implicit call rejection.

 Value: 1604

### CODE_REJECT_UNKNOWN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_REJECT_UNKNOWN: Int
```

The rejection cause is not known.

Used with implicit call rejection.

 Value: 1600

### CODE_REJECT_UNSUPPORTED_SDP_HEADERS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_REJECT_UNSUPPORTED_SDP_HEADERS: Int
```

Invalid/unsupported SDP headers received.

Used with implicit call rejection.

 Value: 1610

### CODE_REJECT_UNSUPPORTED_SIP_HEADERS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_REJECT_UNSUPPORTED_SIP_HEADERS: Int
```

Invalid/unsupported SIP headers received.

Used with implicit call rejection.

 Value: 1609

### CODE_REJECT_VT_AVPF_NOT_ALLOWED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_REJECT_VT_AVPF_NOT_ALLOWED: Int
```

A video call with AVPF is not supported.

Used with implicit call rejection.

 Value: 1619

### CODE_REJECT_VT_TTY_NOT_ALLOWED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_REJECT_VT_TTY_NOT_ALLOWED: Int
```

Video calling not supported with TTY.

Used with implicit call rejection.

 Value: 1615

### CODE_REMOTE_CALL_DECLINE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_REMOTE_CALL_DECLINE: Int
```

Similar to `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_CALL_DECLINE:kotlin.Int`, except indicates that a remote device has declined the call. Used in a multi-endpoint scenario where a remote device declined an incoming call.

 Value: 1404

### CODE_SESSION_MODIFICATION_FAILED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SESSION_MODIFICATION_FAILED: Int
```

UPGRADE DOWNGRADE operation failed This can happen due to failure from SIP/RTP/SDP generation or a Call end is triggered/received while Reinvite is in progress.

 Value: 1517

### CODE_SIP_ALTERNATE_EMERGENCY_CALL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SIP_ALTERNATE_EMERGENCY_CALL: Int
```

Call failed due to SIP code 380 (Alternative Service response) while dialing an "undetected emergency number". This scenario is important in some regions where the carrier network will identify other non-emergency help numbers (e.g. mountain rescue) when attempting to dial.

 Value: 1514

### CODE_SIP_AMBIGUOUS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SIP_AMBIGUOUS: Int
```

SIP Response : 485 Request-URI is ambiguous

 Value: 376

### CODE_SIP_BAD_ADDRESS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SIP_BAD_ADDRESS: Int
```

SIP response 484 : Address Incomplete

 Value: 337

### CODE_SIP_BAD_REQUEST

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SIP_BAD_REQUEST: Int
```

Sip 400 response : Bad Request

 Value: 331

### CODE_SIP_BUSY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SIP_BUSY: Int
```

Returned a busy response, may be one of the following: SIP response 486 : Busy Here, SIP response 600 : Busy Everywhere

 Value: 338

### CODE_SIP_CALL_OR_TRANS_DOES_NOT_EXIST

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SIP_CALL_OR_TRANS_DOES_NOT_EXIST: Int
```

SIP Response : 481 Request received by the server does not match any dialog or transaction

 Value: 372

### CODE_SIP_CLIENT_ERROR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SIP_CLIENT_ERROR: Int
```

Received another unspecified error SIP response from the client.

 Value: 342

### CODE_SIP_EXTENSION_REQUIRED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SIP_EXTENSION_REQUIRED: Int
```

SIP Response : 421 Specific extension is required, which is not present in the HEADER

 Value: 370

### CODE_SIP_FORBIDDEN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SIP_FORBIDDEN: Int
```

Sip 403 response : Forbidden

 Value: 332

### CODE_SIP_GLOBAL_ERROR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SIP_GLOBAL_ERROR: Int
```

Unspecified 6xx error.

 Value: 362

### CODE_SIP_INTERVAL_TOO_BRIEF

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SIP_INTERVAL_TOO_BRIEF: Int
```

SIP Response : 422 The session expiration field too small

 Value: 371

### CODE_SIP_LOOP_DETECTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SIP_LOOP_DETECTED: Int
```

SIP Response : 482 Server has detected a loop

 Value: 373

### CODE_SIP_METHOD_NOT_ALLOWED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SIP_METHOD_NOT_ALLOWED: Int
```

SIP Response : 405 Method not allowed for the address in the Request URI

 Value: 366

### CODE_SIP_NOT_ACCEPTABLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SIP_NOT_ACCEPTABLE: Int
```

Received a not acceptable response, will be one of the following: SIP response 406 : Not Acceptable SIP response 488 : Not Acceptable Here SIP response 606 : Not Acceptable

 Value: 340

### CODE_SIP_NOT_FOUND

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SIP_NOT_FOUND: Int
```

Sip 404 response : Not Found

 Value: 333

### CODE_SIP_NOT_REACHABLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SIP_NOT_REACHABLE: Int
```

Received a not acceptable response, will be one of the following: SIP response 410 : Gone SIP response 604 : Does Not Exist Anywhere

 Value: 341

### CODE_SIP_NOT_SUPPORTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SIP_NOT_SUPPORTED: Int
```

Not supported, because of one of the following: SIP response 415 : Unsupported Media Type, SIP response 416 : Unsupported URI Scheme, SIP response 420 : Bad Extension

 Value: 334

### CODE_SIP_PROXY_AUTHENTICATION_REQUIRED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SIP_PROXY_AUTHENTICATION_REQUIRED: Int
```

SIP Response : 407 The request requires user authentication

 Value: 367

### CODE_SIP_REDIRECTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SIP_REDIRECTED: Int
```

SIP 3xx response: SIP request is redirected

 Value: 321

### CODE_SIP_REQUEST_CANCELLED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SIP_REQUEST_CANCELLED: Int
```

SIP response 487 : Request Terminated

 Value: 339

### CODE_SIP_REQUEST_ENTITY_TOO_LARGE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SIP_REQUEST_ENTITY_TOO_LARGE: Int
```

SIP Response : 413 Request body too large

 Value: 368

### CODE_SIP_REQUEST_PENDING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SIP_REQUEST_PENDING: Int
```

SIP Response : 491 Server has pending request for same dialog

 Value: 377

### CODE_SIP_REQUEST_TIMEOUT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SIP_REQUEST_TIMEOUT: Int
```

SIP response 408 : Request Timeout.

 Value: 335

### CODE_SIP_REQUEST_URI_TOO_LARGE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SIP_REQUEST_URI_TOO_LARGE: Int
```

SIP Response : 414 Request-URI too large

 Value: 369

### CODE_SIP_SERVER_ERROR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SIP_SERVER_ERROR: Int
```

Received an unspecified SIP server error response.

 Value: 354

### CODE_SIP_SERVER_INTERNAL_ERROR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SIP_SERVER_INTERNAL_ERROR: Int
```

SIP response 501 : Server Internal Error

 Value: 351

### CODE_SIP_SERVER_TIMEOUT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SIP_SERVER_TIMEOUT: Int
```

SIP response 504 : Server Time-out

 Value: 353

### CODE_SIP_SERVICE_UNAVAILABLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SIP_SERVICE_UNAVAILABLE: Int
```

SIP response 503 : Service Unavailable

 Value: 352

### CODE_SIP_TEMPRARILY_UNAVAILABLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SIP_TEMPRARILY_UNAVAILABLE: Int
```

SIP response 480 : Temporarily Unavailable

 Value: 336

### CODE_SIP_TOO_MANY_HOPS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SIP_TOO_MANY_HOPS: Int
```

SIP Response : 483 Max-Forwards value reached

 Value: 374

### CODE_SIP_TRANSACTION_DOES_NOT_EXIST

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SIP_TRANSACTION_DOES_NOT_EXIST: Int
```

SIP response 481: Transaction Does Not Exist

 Value: 343

### CODE_SIP_UNDECIPHERABLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SIP_UNDECIPHERABLE: Int
```

SIP Response : 493 The request cannot be decrypted by recipient

 Value: 378

### CODE_SIP_USER_MARKED_UNWANTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SIP_USER_MARKED_UNWANTED: Int
```

Call failure code during hangup/reject if user marked the call as unwanted. Android Telephony will receive information whether ROBO call feature is supported by the network from modem and propagate the same to AOSP as new ImsCallProfile members. OEMs can check this information and provide an option to the user to mark the call as unwanted.

 Value: 365

### CODE_SIP_USER_REJECTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SIP_USER_REJECTED: Int
```

603 : Decline

 Value: 361

### CODE_SUPP_SVC_CANCELLED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SUPP_SVC_CANCELLED: Int
```

Supplementary Services (HOLD/RESUME) - the command was cancelled.

 Value: 1202

### CODE_SUPP_SVC_FAILED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SUPP_SVC_FAILED: Int
```

Supplementary Services (HOLD/RESUME) - the command failed.

 Value: 1201

### CODE_SUPP_SVC_REINVITE_COLLISION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_SUPP_SVC_REINVITE_COLLISION: Int
```

Supplementary Services (HOLD/RESUME) - the command resulted in a re-invite collision.

 Value: 1203

### CODE_TIMEOUT_1XX_WAITING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_TIMEOUT_1XX_WAITING: Int
```

1xx waiting timer is expired after sending INVITE request (MO calls only)

 Value: 201

### CODE_TIMEOUT_NO_ANSWER

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_TIMEOUT_NO_ANSWER: Int
```

User didn't answer during call setup operation (MO/MT) MO : 200 OK to INVITE request is not received, MT : No action from user after alerting the call

 Value: 202

### CODE_TIMEOUT_NO_ANSWER_CALL_UPDATE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_TIMEOUT_NO_ANSWER_CALL_UPDATE: Int
```

User no answer during call update operation (MO/MT) MO : 200 OK to re-INVITE request is not received, MT : No action from user after alerting the call

 Value: 203

### CODE_UNSPECIFIED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_UNSPECIFIED: Int
```

The Reason is unspecified.

 Value: 0

### CODE_USER_CANCELLED_SESSION_MODIFICATION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_USER_CANCELLED_SESSION_MODIFICATION: Int
```

Upgrade Downgrade request cancelled by the user who initiated it

 Value: 512

### CODE_USER_DECLINE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_USER_DECLINE: Int
```

User declined an incoming call.

 Value: 504

### CODE_USER_IGNORE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_USER_IGNORE: Int
```

User ignored an incoming call.

 Value: 503

### CODE_USER_NOANSWER

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_USER_NOANSWER: Int
```

No action was taken while an incoming call was ringing.

 Value: 502

### CODE_USER_REJECTED_SESSION_MODIFICATION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_USER_REJECTED_SESSION_MODIFICATION: Int
```

Upgrade Downgrade request rejected by Remote user if the request is MO initiated Local user if the request is MT initiated

 Value: 511

### CODE_USER_TERMINATED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_USER_TERMINATED: Int
```

User triggers the call to be terminated.

 Value: 501

### CODE_USER_TERMINATED_BY_REMOTE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_USER_TERMINATED_BY_REMOTE: Int
```

The call has been terminated by the network or remote user.

 Value: 510

### CODE_UT_CB_PASSWORD_MISMATCH

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_UT_CB_PASSWORD_MISMATCH: Int
```

The password entered for UT operations does not match the stored password.

 Value: 821

### CODE_UT_NETWORK_ERROR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_UT_NETWORK_ERROR: Int
```

The UT request resulted in a network error.

 Value: 804

### CODE_UT_NOT_SUPPORTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_UT_NOT_SUPPORTED: Int
```

UT is currently not supported on this device.

 Value: 801

### CODE_UT_OPERATION_NOT_ALLOWED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_UT_OPERATION_NOT_ALLOWED: Int
```

The requested UT operation is not allowed.

 Value: 803

### CODE_UT_SERVICE_UNAVAILABLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_UT_SERVICE_UNAVAILABLE: Int
```

UT services are currently not available on this device.

 Value: 802

### CODE_UT_SS_MODIFIED_TO_DIAL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_UT_SS_MODIFIED_TO_DIAL: Int
```

Sim Toolkit Call Control modified the UT operation to a dial command.

 Value: 822

### CODE_UT_SS_MODIFIED_TO_DIAL_VIDEO

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_UT_SS_MODIFIED_TO_DIAL_VIDEO: Int
```

Sim Toolkit Call Control modified the UT operation to a video call dial command.

 Value: 825

### CODE_UT_SS_MODIFIED_TO_SS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_UT_SS_MODIFIED_TO_SS: Int
```

Sim Toolkit Call Control modified the UT operation to another supplementary service command.

 Value: 824

### CODE_UT_SS_MODIFIED_TO_USSD

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_UT_SS_MODIFIED_TO_USSD: Int
```

Sim Toolkit Call Control modified the UT operation to a USSD command.

 Value: 823

### CODE_WIFI_LOST

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_WIFI_LOST: Int
```

Indicates a call was disconnected due to loss of wifi signal.

 Value: 1407

### EXTRA_CODE_CALL_RETRY_BY_SETTINGS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CODE_CALL_RETRY_BY_SETTINGS: Int
```

An extra that may be populated when the `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_CALL_CS_RETRY_REQUIRED:kotlin.Int` result has been returned.

Try to connect the call using CS by using the settings.

 Value: 3

### EXTRA_CODE_CALL_RETRY_EMERGENCY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CODE_CALL_RETRY_EMERGENCY: Int
```

An extra that may be populated when the `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_CALL_CS_RETRY_REQUIRED:kotlin.Int` result has been returned.

Try to connect the call using CS as emergency

 Value: 4

### EXTRA_CODE_CALL_RETRY_NORMAL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CODE_CALL_RETRY_NORMAL: Int
```

An extra that may be populated when the `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_CALL_CS_RETRY_REQUIRED:kotlin.Int` result has been returned.

Try to connect the call using CS

 Value: 1

### EXTRA_CODE_CALL_RETRY_SILENT_REDIAL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CODE_CALL_RETRY_SILENT_REDIAL: Int
```

An extra that may be populated when the `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_CALL_CS_RETRY_REQUIRED:kotlin.Int` result has been returned.

Try to connect the call using CS and do not notify the user.

 Value: 2

## Public constructors

### ImsReasonInfo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ImsReasonInfo(
    code: Int, 
    extraCode: Int, 
    extraMessage: String?)
```

| Parameters ||
|---|---|
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_UNSPECIFIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_ILLEGAL_ARGUMENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_ILLEGAL_STATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_INTERNAL_ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_IMS_SERVICE_DOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_NO_PENDING_CALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_ENDED_BY_CONFERENCE_MERGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_POWER_OFF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_LOW_BATTERY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_NETWORK_NO_SERVICE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_NETWORK_NO_LTE_COVERAGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_NETWORK_ROAMING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_NETWORK_IP_CHANGED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_SERVICE_UNAVAILABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_NOT_REGISTERED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_CALL_EXCEEDED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_CALL_BUSY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_CALL_DECLINE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_CALL_VCC_ON_PROGRESSING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_CALL_RESOURCE_RESERVATION_FAILED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_CALL_CS_RETRY_REQUIRED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_CALL_VOLTE_RETRY_REQUIRED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_CALL_TERMINATED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_HO_NOT_FEASIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_TIMEOUT_1XX_WAITING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_TIMEOUT_NO_ANSWER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_TIMEOUT_NO_ANSWER_CALL_UPDATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_CALL_BARRED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_FDN_BLOCKED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_IMEI_NOT_ACCEPTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_DIAL_MODIFIED_TO_USSD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_DIAL_MODIFIED_TO_SS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_DIAL_MODIFIED_TO_DIAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_DIAL_MODIFIED_TO_DIAL_VIDEO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_DIAL_VIDEO_MODIFIED_TO_DIAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_DIAL_VIDEO_MODIFIED_TO_DIAL_VIDEO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_DIAL_VIDEO_MODIFIED_TO_SS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_DIAL_VIDEO_MODIFIED_TO_USSD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_REDIRECTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_BAD_REQUEST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_FORBIDDEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_NOT_FOUND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_NOT_SUPPORTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_REQUEST_TIMEOUT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_TEMPRARILY_UNAVAILABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_BAD_ADDRESS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_BUSY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_REQUEST_CANCELLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_NOT_ACCEPTABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_NOT_REACHABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_CLIENT_ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_TRANSACTION_DOES_NOT_EXIST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_SERVER_INTERNAL_ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_SERVICE_UNAVAILABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_SERVER_TIMEOUT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_SERVER_ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_USER_REJECTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_GLOBAL_ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_EMERGENCY_TEMP_FAILURE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_EMERGENCY_PERM_FAILURE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_USER_MARKED_UNWANTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_METHOD_NOT_ALLOWED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_PROXY_AUTHENTICATION_REQUIRED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_REQUEST_ENTITY_TOO_LARGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_REQUEST_URI_TOO_LARGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_EXTENSION_REQUIRED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_INTERVAL_TOO_BRIEF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_CALL_OR_TRANS_DOES_NOT_EXIST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_LOOP_DETECTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_TOO_MANY_HOPS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_AMBIGUOUS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_REQUEST_PENDING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_UNDECIPHERABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_MEDIA_INIT_FAILED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_MEDIA_NO_DATA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_MEDIA_NOT_ACCEPTABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_MEDIA_UNSPECIFIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_USER_TERMINATED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_USER_NOANSWER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_USER_IGNORE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_USER_DECLINE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOW_BATTERY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_BLACKLISTED_CALL_ID:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_USER_TERMINATED_BY_REMOTE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_USER_REJECTED_SESSION_MODIFICATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_USER_CANCELLED_SESSION_MODIFICATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SESSION_MODIFICATION_FAILED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_UT_NOT_SUPPORTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_UT_SERVICE_UNAVAILABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_UT_OPERATION_NOT_ALLOWED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_UT_NETWORK_ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_UT_CB_PASSWORD_MISMATCH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_UT_SS_MODIFIED_TO_DIAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_UT_SS_MODIFIED_TO_USSD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_UT_SS_MODIFIED_TO_SS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_UT_SS_MODIFIED_TO_DIAL_VIDEO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_ECBM_NOT_SUPPORTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_MULTIENDPOINT_NOT_SUPPORTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REGISTRATION_ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_ANSWERED_ELSEWHERE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_CALL_PULL_OUT_OF_SYNC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_CALL_END_CAUSE_CALL_PULL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_CALL_DROP_IWLAN_TO_LTE_UNAVAILABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECTED_ELSEWHERE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SUPP_SVC_FAILED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SUPP_SVC_CANCELLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SUPP_SVC_REINVITE_COLLISION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_IWLAN_DPD_FAILURE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_EPDG_TUNNEL_ESTABLISH_FAILURE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_EPDG_TUNNEL_REKEY_FAILURE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_EPDG_TUNNEL_LOST_CONNECTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_MAXIMUM_NUMBER_OF_CALLS_REACHED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REMOTE_CALL_DECLINE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_DATA_LIMIT_REACHED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_DATA_DISABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_WIFI_LOST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_IKEV2_AUTH_FAILURE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_RADIO_OFF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_NO_VALID_SIM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_RADIO_INTERNAL_ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_NETWORK_RESP_TIMEOUT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_NETWORK_REJECT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_RADIO_ACCESS_FAILURE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_RADIO_LINK_FAILURE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_RADIO_LINK_LOST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_RADIO_UPLINK_FAILURE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_RADIO_SETUP_FAILURE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_RADIO_RELEASE_NORMAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_RADIO_RELEASE_ABNORMAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_ACCESS_CLASS_BLOCKED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_NETWORK_DETACH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_ALTERNATE_EMERGENCY_CALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_NO_CSFB_IN_CS_ROAM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_ONGOING_CALL_WAITING_DISABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_CALL_ON_OTHER_SUB:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_1X_COLLISION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_SERVICE_NOT_REGISTERED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_CALL_TYPE_NOT_ALLOWED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_ONGOING_E911_CALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_ONGOING_CALL_SETUP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_MAX_CALL_LIMIT_REACHED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_UNSUPPORTED_SIP_HEADERS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_UNSUPPORTED_SDP_HEADERS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_ONGOING_CALL_TRANSFER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_INTERNAL_ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_QOS_FAILURE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_ONGOING_HANDOVER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_VT_TTY_NOT_ALLOWED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_ONGOING_CALL_UPGRADE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_CONFERENCE_TTY_NOT_ALLOWED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_ONGOING_CONFERENCE_CALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_VT_AVPF_NOT_ALLOWED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_ONGOING_ENCRYPTED_CALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_ONGOING_CS_CALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_NETWORK_CONGESTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_1:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_2:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_4:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_5:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_6:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_7:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_8:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_9:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_10:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_11:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_12:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_13:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_14:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_15:kotlin.Int` |
| `extraMessage` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |

## Public methods

### describeContents

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getCode

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCode(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | an integer representing more information about the completion of an operation. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_UNSPECIFIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_ILLEGAL_ARGUMENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_ILLEGAL_STATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_INTERNAL_ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_IMS_SERVICE_DOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_NO_PENDING_CALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_ENDED_BY_CONFERENCE_MERGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_POWER_OFF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_LOW_BATTERY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_NETWORK_NO_SERVICE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_NETWORK_NO_LTE_COVERAGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_NETWORK_ROAMING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_NETWORK_IP_CHANGED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_SERVICE_UNAVAILABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_NOT_REGISTERED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_CALL_EXCEEDED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_CALL_BUSY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_CALL_DECLINE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_CALL_VCC_ON_PROGRESSING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_CALL_RESOURCE_RESERVATION_FAILED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_CALL_CS_RETRY_REQUIRED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_CALL_VOLTE_RETRY_REQUIRED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_CALL_TERMINATED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOCAL_HO_NOT_FEASIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_TIMEOUT_1XX_WAITING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_TIMEOUT_NO_ANSWER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_TIMEOUT_NO_ANSWER_CALL_UPDATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_CALL_BARRED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_FDN_BLOCKED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_IMEI_NOT_ACCEPTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_DIAL_MODIFIED_TO_USSD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_DIAL_MODIFIED_TO_SS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_DIAL_MODIFIED_TO_DIAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_DIAL_MODIFIED_TO_DIAL_VIDEO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_DIAL_VIDEO_MODIFIED_TO_DIAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_DIAL_VIDEO_MODIFIED_TO_DIAL_VIDEO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_DIAL_VIDEO_MODIFIED_TO_SS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_DIAL_VIDEO_MODIFIED_TO_USSD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_REDIRECTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_BAD_REQUEST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_FORBIDDEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_NOT_FOUND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_NOT_SUPPORTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_REQUEST_TIMEOUT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_TEMPRARILY_UNAVAILABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_BAD_ADDRESS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_BUSY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_REQUEST_CANCELLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_NOT_ACCEPTABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_NOT_REACHABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_CLIENT_ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_TRANSACTION_DOES_NOT_EXIST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_SERVER_INTERNAL_ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_SERVICE_UNAVAILABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_SERVER_TIMEOUT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_SERVER_ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_USER_REJECTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_GLOBAL_ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_EMERGENCY_TEMP_FAILURE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_EMERGENCY_PERM_FAILURE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_USER_MARKED_UNWANTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_METHOD_NOT_ALLOWED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_PROXY_AUTHENTICATION_REQUIRED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_REQUEST_ENTITY_TOO_LARGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_REQUEST_URI_TOO_LARGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_EXTENSION_REQUIRED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_INTERVAL_TOO_BRIEF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_CALL_OR_TRANS_DOES_NOT_EXIST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_LOOP_DETECTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_TOO_MANY_HOPS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_AMBIGUOUS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_REQUEST_PENDING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_UNDECIPHERABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_MEDIA_INIT_FAILED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_MEDIA_NO_DATA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_MEDIA_NOT_ACCEPTABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_MEDIA_UNSPECIFIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_USER_TERMINATED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_USER_NOANSWER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_USER_IGNORE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_USER_DECLINE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_LOW_BATTERY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_BLACKLISTED_CALL_ID:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_USER_TERMINATED_BY_REMOTE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_USER_REJECTED_SESSION_MODIFICATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_USER_CANCELLED_SESSION_MODIFICATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SESSION_MODIFICATION_FAILED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_UT_NOT_SUPPORTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_UT_SERVICE_UNAVAILABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_UT_OPERATION_NOT_ALLOWED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_UT_NETWORK_ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_UT_CB_PASSWORD_MISMATCH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_UT_SS_MODIFIED_TO_DIAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_UT_SS_MODIFIED_TO_USSD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_UT_SS_MODIFIED_TO_SS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_UT_SS_MODIFIED_TO_DIAL_VIDEO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_ECBM_NOT_SUPPORTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_MULTIENDPOINT_NOT_SUPPORTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REGISTRATION_ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_ANSWERED_ELSEWHERE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_CALL_PULL_OUT_OF_SYNC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_CALL_END_CAUSE_CALL_PULL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_CALL_DROP_IWLAN_TO_LTE_UNAVAILABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECTED_ELSEWHERE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SUPP_SVC_FAILED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SUPP_SVC_CANCELLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SUPP_SVC_REINVITE_COLLISION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_IWLAN_DPD_FAILURE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_EPDG_TUNNEL_ESTABLISH_FAILURE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_EPDG_TUNNEL_REKEY_FAILURE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_EPDG_TUNNEL_LOST_CONNECTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_MAXIMUM_NUMBER_OF_CALLS_REACHED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REMOTE_CALL_DECLINE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_DATA_LIMIT_REACHED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_DATA_DISABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_WIFI_LOST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_IKEV2_AUTH_FAILURE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_RADIO_OFF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_NO_VALID_SIM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_RADIO_INTERNAL_ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_NETWORK_RESP_TIMEOUT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_NETWORK_REJECT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_RADIO_ACCESS_FAILURE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_RADIO_LINK_FAILURE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_RADIO_LINK_LOST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_RADIO_UPLINK_FAILURE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_RADIO_SETUP_FAILURE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_RADIO_RELEASE_NORMAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_RADIO_RELEASE_ABNORMAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_ACCESS_CLASS_BLOCKED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_NETWORK_DETACH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_SIP_ALTERNATE_EMERGENCY_CALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_NO_CSFB_IN_CS_ROAM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_ONGOING_CALL_WAITING_DISABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_CALL_ON_OTHER_SUB:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_1X_COLLISION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_SERVICE_NOT_REGISTERED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_CALL_TYPE_NOT_ALLOWED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_ONGOING_E911_CALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_ONGOING_CALL_SETUP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_MAX_CALL_LIMIT_REACHED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_UNSUPPORTED_SIP_HEADERS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_UNSUPPORTED_SDP_HEADERS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_ONGOING_CALL_TRANSFER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_INTERNAL_ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_QOS_FAILURE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_ONGOING_HANDOVER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_VT_TTY_NOT_ALLOWED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_ONGOING_CALL_UPGRADE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_CONFERENCE_TTY_NOT_ALLOWED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_ONGOING_CONFERENCE_CALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_VT_AVPF_NOT_ALLOWED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_ONGOING_ENCRYPTED_CALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_REJECT_ONGOING_CS_CALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_NETWORK_CONGESTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_1:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_2:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_4:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_5:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_6:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_7:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_8:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_9:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_10:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_11:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_12:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_13:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_14:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#CODE_OEM_CAUSE_15:kotlin.Int` |

### getExtraCode

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getExtraCode(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | an optional OEM specified code that provides extra information. |

### getExtraMessage

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getExtraMessage(): String?
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | an optional OEM specified string that provides extra information about the operation result. This value may be `null`. |

### toString

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the string format of `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo#` This value cannot be `null`. |

### writeToParcel

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |
| `out` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): This value cannot be `null`. |

## Properties

### CREATOR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<ImsReasonInfo!>
```
