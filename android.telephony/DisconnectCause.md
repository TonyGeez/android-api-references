Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DisconnectCause

```
class DisconnectCause
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.telephony.DisconnectCause](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#) |

Describes the cause of a disconnected call. Those disconnect causes can be converted into a more generic `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause.html#` object. Used in `https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onCallDisconnectCauseChanged(kotlin.Int,%20kotlin.Int)`.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#ALREADY_DIALING:kotlin.Int` Indicates that a new outgoing call cannot be placed because there is already an outgoing call dialing out. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#ANSWERED_ELSEWHERE:kotlin.Int` The call was terminated because it was answered on another device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#BUSY:kotlin.Int` Outgoing call to busy line |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#CALLING_DISABLED:kotlin.Int` Indicates that a new outgoing call cannot be placed because calling has been disabled using the ro. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#CALL_BARRED:kotlin.Int` Call was blocked by call barring |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#CALL_PULLED:kotlin.Int` The call was terminated because it was pulled to another device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#CANT_CALL_WHILE_RINGING:kotlin.Int` Indicates that a new outgoing call cannot be placed while there is a ringing call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#CDMA_ACCESS_BLOCKED:kotlin.Int` Access Blocked by CDMA network |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#CDMA_ACCESS_FAILURE:kotlin.Int` Unable to obtain access to the CDMA system |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#CDMA_ALREADY_ACTIVATED:kotlin.Int` The call was terminated because CDMA phone service and roaming have already been activated. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#CDMA_DROP:kotlin.Int` Drop call |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#CDMA_INTERCEPT:kotlin.Int` INTERCEPT order received, MS state idle entered |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#CDMA_LOCKED_UNTIL_POWER_CYCLE:kotlin.Int` MS is locked until next power cycle |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#CDMA_NOT_EMERGENCY:kotlin.Int` Not an emergency call |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#CDMA_PREEMPTED:kotlin.Int` Not a preempted call |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#CDMA_REORDER:kotlin.Int` MS has been redirected, call is cancelled |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#CDMA_RETRY_ORDER:kotlin.Int` Requested service is rejected, retry delay is set |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#CDMA_SO_REJECT:kotlin.Int` Service option rejection |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#CONGESTION:kotlin.Int` Outgoing call to congested network |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#CS_RESTRICTED:kotlin.Int` Call was blocked by restricted all voice access |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#CS_RESTRICTED_EMERGENCY:kotlin.Int` Call was blocked by restricted emergency voice access |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#CS_RESTRICTED_NORMAL:kotlin.Int` Call was blocked by restricted normal voice access |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#DATA_DISABLED:kotlin.Int` The call was terminated because cellular data has been disabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#DATA_LIMIT_REACHED:kotlin.Int` The call was terminated because the data policy has disabled cellular data. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#DIALED_CALL_FORWARDING_WHILE_ROAMING:kotlin.Int` The call being placed was detected as a call forwarding number and was being dialed while roaming on a carrier that does not allow this. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#DIALED_MMI:kotlin.Int` Our initial phone number was actually an MMI sequence. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#DIAL_LOW_BATTERY:kotlin.Int` A call was not dialed because the device's battery is too low. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#DIAL_MODIFIED_TO_DIAL:kotlin.Int` Stk Call Control modified DIAL request to DIAL with modified data. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#DIAL_MODIFIED_TO_DIAL_VIDEO:kotlin.Int` Stk Call Control modified DIAL request to video DIAL request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#DIAL_MODIFIED_TO_SS:kotlin.Int` Stk Call Control modified DIAL request to SS request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#DIAL_MODIFIED_TO_USSD:kotlin.Int` Stk Call Control modified DIAL request to USSD request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#DIAL_VIDEO_MODIFIED_TO_DIAL:kotlin.Int` Stk Call Control modified Video DIAL request to DIAL request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#DIAL_VIDEO_MODIFIED_TO_DIAL_VIDEO:kotlin.Int` Stk Call Control modified Video DIAL request to Video DIAL request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#DIAL_VIDEO_MODIFIED_TO_SS:kotlin.Int` Stk Call Control modified Video DIAL request to SS request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#DIAL_VIDEO_MODIFIED_TO_USSD:kotlin.Int` Stk Call Control modified Video DIAL request to USSD request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#EMERGENCY_CALL_OVER_WFC_NOT_AVAILABLE:kotlin.Int` Indicates that an emergency call cannot be placed over WFC because the service is not available in the current location. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#EMERGENCY_PERM_FAILURE:kotlin.Int` Emergency call failed with a permanent fail cause and should not be redialed on this slot. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#EMERGENCY_TEMP_FAILURE:kotlin.Int` Emergency call failed with a temporary fail cause and can be redialed on this slot. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#ERROR_UNSPECIFIED:kotlin.Int` Unknown error or not specified |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#FDN_BLOCKED:kotlin.Int` Call was blocked by fixed dial number |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#ICC_ERROR:kotlin.Int` No ICC, ICC locked, or other ICC error |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#IMEI_NOT_ACCEPTED:kotlin.Int` The network does not accept the emergency call request because IMEI was used as identification and this cability is not supported by the network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#IMS_ACCESS_BLOCKED:kotlin.Int` The call has failed because of access class barring. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#IMS_MERGED_SUCCESSFULLY:kotlin.Int` The call, which was an IMS call, disconnected because it merged with another call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#IMS_SIP_ALTERNATE_EMERGENCY_CALL:kotlin.Int` The network has reported that an alternative emergency number has been dialed, but the user must exit airplane mode to place the call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#INCOMING_AUTO_REJECTED:kotlin.Int` Indicates that incoming call was rejected by the modem before the call went in ringing |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#INCOMING_MISSED:kotlin.Int` An incoming call that was missed and never answered |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#INCOMING_REJECTED:kotlin.Int` An incoming call that was rejected |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#INVALID_CREDENTIALS:kotlin.Int` Invalid credentials |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#INVALID_NUMBER:kotlin.Int` Invalid dial string |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#LIMIT_EXCEEDED:kotlin.Int` GSM or CDMA ACM limit exceeded |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#LOCAL:kotlin.Int` Normal; Local hangup |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#LOST_SIGNAL:kotlin.Int` Client went out of network range |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#LOW_BATTERY:kotlin.Int` The call has ended (mid-call) because the device's battery is too low. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#MAXIMUM_NUMBER_OF_CALLS_REACHED:kotlin.Int` The call was terminated because the maximum allowable number of calls has been reached. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#MEDIA_TIMEOUT:kotlin.Int` Indicates that the call is dropped due to RTCP inactivity, primarily due to media path disruption. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#MMI:kotlin.Int` Not presently used |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#NORMAL:kotlin.Int` Normal; Remote hangup |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#NORMAL_UNSPECIFIED:kotlin.Int` This cause is used to report a normal event only when no other cause in the normal class applies. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#NOT_DISCONNECTED:kotlin.Int` Has not yet disconnected |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#NOT_VALID:kotlin.Int` The disconnect cause is not valid (Not received a disconnect cause) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#NO_PHONE_NUMBER_SUPPLIED:kotlin.Int` The supplied CALL Intent didn't contain a valid phone number. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#NUMBER_UNREACHABLE:kotlin.Int` Cannot reach the peer |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#OTASP_PROVISIONING_IN_PROCESS:kotlin.Int` Indicates that a new outgoing call cannot be placed because OTASP provisioning is currently in process. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#OUTGOING_CANCELED:kotlin.Int` The outgoing call was canceled by the `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService.html#`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#OUTGOING_EMERGENCY_CALL_PLACED:kotlin.Int` Indicates that an emergency call was placed, which caused the existing connection to be hung up. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#OUTGOING_FAILURE:kotlin.Int` The outgoing call failed with an unknown cause. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#OUT_OF_NETWORK:kotlin.Int` Calling from out of network is not allowed |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#OUT_OF_SERVICE:kotlin.Int` Out of service |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#POWER_OFF:kotlin.Int` Radio is turned off explicitly |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#SATELLITE_ENABLED:kotlin.Int` Indicates that the call was unable to be made because the satellite modem is enabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#SERVER_ERROR:kotlin.Int` Server error |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#SERVER_UNREACHABLE:kotlin.Int` Cannot reach the server |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#TIMED_OUT:kotlin.Int` Client timed out |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#TOO_MANY_ONGOING_CALLS:kotlin.Int` Indicates that a new outgoing call cannot be placed because there is currently an ongoing foreground and background call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#UNOBTAINABLE_NUMBER:kotlin.Int` Unassigned number |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#UNWANTED:kotlin.Int` The call was missed or rejected because it was marked as unwanted. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#VIDEO_CALL_NOT_ALLOWED_WHILE_TTY_ENABLED:kotlin.Int` The call was terminated because it is not possible to place a video call while TTY is enabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#VOICEMAIL_NUMBER_MISSING:kotlin.Int` We tried to call a voicemail: URI but the device has no voicemail number configured. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#WFC_SERVICE_NOT_AVAILABLE_IN_THIS_LOCATION:kotlin.Int` Indicates that WiFi calling service is not available in the current location. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#WIFI_LOST:kotlin.Int` A call over WIFI was disconnected because the WIFI signal was lost or became too degraded to continue the call. |

## Constants

### ALREADY_DIALING

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ALREADY_DIALING: Int
```

Indicates that a new outgoing call cannot be placed because there is already an outgoing call dialing out.

 Value: 72

### ANSWERED_ELSEWHERE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ANSWERED_ELSEWHERE: Int
```

The call was terminated because it was answered on another device.

 Value: 52

### BUSY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BUSY: Int
```

Outgoing call to busy line

 Value: 4

### CALLING_DISABLED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CALLING_DISABLED: Int
```

Indicates that a new outgoing call cannot be placed because calling has been disabled using the ro.telephony.disable-call system property.

 Value: 74

### CALL_BARRED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CALL_BARRED: Int
```

Call was blocked by call barring

 Value: 20

### CALL_PULLED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CALL_PULLED: Int
```

The call was terminated because it was pulled to another device.

 Value: 51

### CANT_CALL_WHILE_RINGING

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CANT_CALL_WHILE_RINGING: Int
```

Indicates that a new outgoing call cannot be placed while there is a ringing call.

 Value: 73

### CDMA_ACCESS_BLOCKED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CDMA_ACCESS_BLOCKED: Int
```

Access Blocked by CDMA network

 Value: 35

### CDMA_ACCESS_FAILURE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CDMA_ACCESS_FAILURE: Int
```

Unable to obtain access to the CDMA system

 Value: 32

### CDMA_ALREADY_ACTIVATED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CDMA_ALREADY_ACTIVATED: Int
```

The call was terminated because CDMA phone service and roaming have already been activated.

 Value: 49

### CDMA_DROP

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CDMA_DROP: Int
```

Drop call

 Value: 27

### CDMA_INTERCEPT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CDMA_INTERCEPT: Int
```

INTERCEPT order received, MS state idle entered

 Value: 28

### CDMA_LOCKED_UNTIL_POWER_CYCLE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CDMA_LOCKED_UNTIL_POWER_CYCLE: Int
```

MS is locked until next power cycle

 Value: 26

### CDMA_NOT_EMERGENCY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CDMA_NOT_EMERGENCY: Int
```

Not an emergency call

 Value: 34

### CDMA_PREEMPTED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CDMA_PREEMPTED: Int
```

Not a preempted call

 Value: 33

### CDMA_REORDER

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CDMA_REORDER: Int
```

MS has been redirected, call is cancelled

 Value: 29

### CDMA_RETRY_ORDER

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CDMA_RETRY_ORDER: Int
```

Requested service is rejected, retry delay is set

 Value: 31

### CDMA_SO_REJECT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CDMA_SO_REJECT: Int
```

Service option rejection

 Value: 30

### CONGESTION

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONGESTION: Int
```

Outgoing call to congested network

 Value: 5

### CS_RESTRICTED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CS_RESTRICTED: Int
```

Call was blocked by restricted all voice access

 Value: 22

### CS_RESTRICTED_EMERGENCY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CS_RESTRICTED_EMERGENCY: Int
```

Call was blocked by restricted emergency voice access

 Value: 24

### CS_RESTRICTED_NORMAL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CS_RESTRICTED_NORMAL: Int
```

Call was blocked by restricted normal voice access

 Value: 23

### DATA_DISABLED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_DISABLED: Int
```

The call was terminated because cellular data has been disabled. Used when in a video call and the user disables cellular data via the settings.

 Value: 54

### DATA_LIMIT_REACHED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_LIMIT_REACHED: Int
```

The call was terminated because the data policy has disabled cellular data. Used when in a video call and the user has exceeded the device data limit.

 Value: 55

### DIALED_CALL_FORWARDING_WHILE_ROAMING

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIALED_CALL_FORWARDING_WHILE_ROAMING: Int
```

The call being placed was detected as a call forwarding number and was being dialed while roaming on a carrier that does not allow this.

 Value: 57

### DIALED_MMI

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIALED_MMI: Int
```

Our initial phone number was actually an MMI sequence.

 Value: 39

### DIAL_LOW_BATTERY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIAL_LOW_BATTERY: Int
```

A call was not dialed because the device's battery is too low.

 Value: 62

### DIAL_MODIFIED_TO_DIAL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIAL_MODIFIED_TO_DIAL: Int
```

Stk Call Control modified DIAL request to DIAL with modified data.

 Value: 48

### DIAL_MODIFIED_TO_DIAL_VIDEO

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIAL_MODIFIED_TO_DIAL_VIDEO: Int
```

Stk Call Control modified DIAL request to video DIAL request.

 Value: 66

### DIAL_MODIFIED_TO_SS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIAL_MODIFIED_TO_SS: Int
```

Stk Call Control modified DIAL request to SS request.

 Value: 47

### DIAL_MODIFIED_TO_USSD

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIAL_MODIFIED_TO_USSD: Int
```

Stk Call Control modified DIAL request to USSD request.

 Value: 46

### DIAL_VIDEO_MODIFIED_TO_DIAL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIAL_VIDEO_MODIFIED_TO_DIAL: Int
```

Stk Call Control modified Video DIAL request to DIAL request.

 Value: 69

### DIAL_VIDEO_MODIFIED_TO_DIAL_VIDEO

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIAL_VIDEO_MODIFIED_TO_DIAL_VIDEO: Int
```

Stk Call Control modified Video DIAL request to Video DIAL request.

 Value: 70

### DIAL_VIDEO_MODIFIED_TO_SS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIAL_VIDEO_MODIFIED_TO_SS: Int
```

Stk Call Control modified Video DIAL request to SS request.

 Value: 67

### DIAL_VIDEO_MODIFIED_TO_USSD

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIAL_VIDEO_MODIFIED_TO_USSD: Int
```

Stk Call Control modified Video DIAL request to USSD request.

 Value: 68

### EMERGENCY_CALL_OVER_WFC_NOT_AVAILABLE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EMERGENCY_CALL_OVER_WFC_NOT_AVAILABLE: Int
```

Indicates that an emergency call cannot be placed over WFC because the service is not available in the current location.

 Value: 78

### EMERGENCY_PERM_FAILURE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EMERGENCY_PERM_FAILURE: Int
```

Emergency call failed with a permanent fail cause and should not be redialed on this slot.

 Value: 64

### EMERGENCY_TEMP_FAILURE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EMERGENCY_TEMP_FAILURE: Int
```

Emergency call failed with a temporary fail cause and can be redialed on this slot.

 Value: 63

### ERROR_UNSPECIFIED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_UNSPECIFIED: Int
```

Unknown error or not specified

 Value: 36

### FDN_BLOCKED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FDN_BLOCKED: Int
```

Call was blocked by fixed dial number

 Value: 21

### ICC_ERROR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ICC_ERROR: Int
```

No ICC, ICC locked, or other ICC error

 Value: 19

### IMEI_NOT_ACCEPTED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IMEI_NOT_ACCEPTED: Int
```

The network does not accept the emergency call request because IMEI was used as identification and this cability is not supported by the network.

 Value: 58

### IMS_ACCESS_BLOCKED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IMS_ACCESS_BLOCKED: Int
```

The call has failed because of access class barring.

 Value: 60

### IMS_MERGED_SUCCESSFULLY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IMS_MERGED_SUCCESSFULLY: Int
```

The call, which was an IMS call, disconnected because it merged with another call.

 Value: 45

### IMS_SIP_ALTERNATE_EMERGENCY_CALL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IMS_SIP_ALTERNATE_EMERGENCY_CALL: Int
```

The network has reported that an alternative emergency number has been dialed, but the user must exit airplane mode to place the call.

 Value: 71

### INCOMING_AUTO_REJECTED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INCOMING_AUTO_REJECTED: Int
```

Indicates that incoming call was rejected by the modem before the call went in ringing

 Value: 81

### INCOMING_MISSED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INCOMING_MISSED: Int
```

An incoming call that was missed and never answered

 Value: 1

### INCOMING_REJECTED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INCOMING_REJECTED: Int
```

An incoming call that was rejected

 Value: 16

### INVALID_CREDENTIALS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INVALID_CREDENTIALS: Int
```

Invalid credentials

 Value: 10

### INVALID_NUMBER

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INVALID_NUMBER: Int
```

Invalid dial string

 Value: 7

### LIMIT_EXCEEDED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LIMIT_EXCEEDED: Int
```

GSM or CDMA ACM limit exceeded

 Value: 15

### LOCAL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LOCAL: Int
```

Normal; Local hangup

 Value: 3

### LOST_SIGNAL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LOST_SIGNAL: Int
```

Client went out of network range

 Value: 14

### LOW_BATTERY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LOW_BATTERY: Int
```

The call has ended (mid-call) because the device's battery is too low.

 Value: 61

### MAXIMUM_NUMBER_OF_CALLS_REACHED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MAXIMUM_NUMBER_OF_CALLS_REACHED: Int
```

The call was terminated because the maximum allowable number of calls has been reached.

 Value: 53

### MEDIA_TIMEOUT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MEDIA_TIMEOUT: Int
```

Indicates that the call is dropped due to RTCP inactivity, primarily due to media path disruption.

 Value: 77

### MMI

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMI: Int
```

Not presently used

 Value: 6

### NORMAL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NORMAL: Int
```

Normal; Remote hangup

 Value: 2

### NORMAL_UNSPECIFIED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NORMAL_UNSPECIFIED: Int
```

This cause is used to report a normal event only when no other cause in the normal class applies.

 Value: 65

### NOT_DISCONNECTED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NOT_DISCONNECTED: Int
```

Has not yet disconnected

 Value: 0

### NOT_VALID

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NOT_VALID: Int
```

The disconnect cause is not valid (Not received a disconnect cause)

 Value: -1

### NO_PHONE_NUMBER_SUPPLIED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NO_PHONE_NUMBER_SUPPLIED: Int
```

The supplied CALL Intent didn't contain a valid phone number.

 Value: 38

### NUMBER_UNREACHABLE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NUMBER_UNREACHABLE: Int
```

Cannot reach the peer

 Value: 8

### OTASP_PROVISIONING_IN_PROCESS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OTASP_PROVISIONING_IN_PROCESS: Int
```

Indicates that a new outgoing call cannot be placed because OTASP provisioning is currently in process.

 Value: 76

### OUTGOING_CANCELED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OUTGOING_CANCELED: Int
```

The outgoing call was canceled by the `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService.html#`.

 Value: 44

### OUTGOING_EMERGENCY_CALL_PLACED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OUTGOING_EMERGENCY_CALL_PLACED: Int
```

Indicates that an emergency call was placed, which caused the existing connection to be hung up.

 Value: 80

### OUTGOING_FAILURE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OUTGOING_FAILURE: Int
```

The outgoing call failed with an unknown cause.

 Value: 43

### OUT_OF_NETWORK

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OUT_OF_NETWORK: Int
```

Calling from out of network is not allowed

 Value: 11

### OUT_OF_SERVICE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OUT_OF_SERVICE: Int
```

Out of service

 Value: 18

### POWER_OFF

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val POWER_OFF: Int
```

Radio is turned off explicitly

 Value: 17

### SATELLITE_ENABLED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SATELLITE_ENABLED: Int
```

Indicates that the call was unable to be made because the satellite modem is enabled.

 Value: 82

### SERVER_ERROR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SERVER_ERROR: Int
```

Server error

 Value: 12

### SERVER_UNREACHABLE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SERVER_UNREACHABLE: Int
```

Cannot reach the server

 Value: 9

### TIMED_OUT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TIMED_OUT: Int
```

Client timed out

 Value: 13

### TOO_MANY_ONGOING_CALLS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TOO_MANY_ONGOING_CALLS: Int
```

Indicates that a new outgoing call cannot be placed because there is currently an ongoing foreground and background call.

 Value: 75

### UNOBTAINABLE_NUMBER

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNOBTAINABLE_NUMBER: Int
```

Unassigned number

 Value: 25

### UNWANTED

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNWANTED: Int
```

The call was missed or rejected because it was marked as unwanted.

 Value: 83

### VIDEO_CALL_NOT_ALLOWED_WHILE_TTY_ENABLED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VIDEO_CALL_NOT_ALLOWED_WHILE_TTY_ENABLED: Int
```

The call was terminated because it is not possible to place a video call while TTY is enabled.

 Value: 50

### VOICEMAIL_NUMBER_MISSING

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VOICEMAIL_NUMBER_MISSING: Int
```

We tried to call a voicemail: URI but the device has no voicemail number configured.

 Value: 40

### WFC_SERVICE_NOT_AVAILABLE_IN_THIS_LOCATION

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WFC_SERVICE_NOT_AVAILABLE_IN_THIS_LOCATION: Int
```

Indicates that WiFi calling service is not available in the current location.

 Value: 79

### WIFI_LOST

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_LOST: Int
```

A call over WIFI was disconnected because the WIFI signal was lost or became too degraded to continue the call.

 Value: 59
