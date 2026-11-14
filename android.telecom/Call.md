# Call

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Call

Kotlin| [Java](../android/telecom/Call.md) 
| --- | --- |

```
class Call
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telecom.Call](../android/telecom/Call.md) |

Represents an ongoing phone call that the in-call app should present to the user.

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Callback](../android/telecom/Call.Callback.md) Defines callbacks which inform the [InCallService](../android/telecom/InCallService.md) of changes to a [Call](../android/telecom/Call.md). |
| | [Details](../android/telecom/Call.Details.md) <br /> |
| | [RttCall](../android/telecom/Call.RttCall.md) A class that holds the state that describes the state of the RTT channel to the remote party, if it is active. |
| --- | --- |

| Constants ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [AVAILABLE_PHONE_ACCOUNTS](../android/telecom/Call.md) The key to retrieve the optional`PhoneAccount`s Telecom can bundle with its Call extras. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EVENT_CLEAR_DIAGNOSTIC_MESSAGE](../android/telecom/Call.md) Event reported from the telecom framework when a diagnostic message previously raised with [EVENT_DISPLAY_DIAGNOSTIC_MESSAGE](../android/telecom/Call.md) has cleared and is no longer pertinent. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EVENT_DISPLAY_DIAGNOSTIC_MESSAGE](../android/telecom/Call.md) Event reported from the Telecom stack to report an in-call diagnostic message which the dialer app may opt to display to the user. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_ASSERTED_DISPLAY_NAME](../android/telecom/Call.md) String value indicating the asserted display name reported via ImsCallProfile#EXTRA_ASSERTED_DISPLAY_NAME. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_DIAGNOSTIC_MESSAGE](../android/telecom/Call.md) [CharSequence](../java/lang/CharSequence.md) extra used with [EVENT_DISPLAY_DIAGNOSTIC_MESSAGE](../android/telecom/Call.md). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_DIAGNOSTIC_MESSAGE_ID](../android/telecom/Call.md) Integer extra representing a message ID for a message posted via [EVENT_DISPLAY_DIAGNOSTIC_MESSAGE](../android/telecom/Call.md). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_IS_BUSINESS_CALL](../android/telecom/Call.md) Boolean indicating that the call is a verified business call. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_IS_SUPPRESSED_BY_DO_NOT_DISTURB](../android/telecom/Call.md) Extra key intended for [InCallService](../android/telecom/InCallService.md) s that notify the user of an incoming call. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_LAST_EMERGENCY_CALLBACK_TIME_MILLIS](../android/telecom/Call.md) Extra key used to indicate the time (in milliseconds since midnight, January 1, 1970 UTC) when the last outgoing emergency call was made. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_SILENT_RINGING_REQUESTED](../android/telecom/Call.md) Extra key used to indicate whether a [CallScreeningService](../android/telecom/CallScreeningService.md) has requested to silence the ringtone for a call. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_SUGGESTED_PHONE_ACCOUNTS](../android/telecom/Call.md) Key for extra used to pass along a list of [PhoneAccountSuggestion](../android/telecom/PhoneAccountSuggestion.md) s to the in-call UI when a call enters the [STATE_SELECT_PHONE_ACCOUNT](../android/telecom/Call.md) state. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REJECT_REASON_DECLINED](../android/telecom/Call.md) Reject reason used with [reject(int)](../android/telecom/Call.md))to indicate that the user is rejecting this call because they have declined to answer it. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REJECT_REASON_UNWANTED](../android/telecom/Call.md) Reject reason used with [reject(int)](../android/telecom/Call.md))to indicate that the user is rejecting this call because it is an unwanted call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_ACTIVE](../android/telecom/Call.md) The state of a`Call`when actively supporting conversation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_AUDIO_PROCESSING](../android/telecom/Call.md) The state of a call that is active with the network, but the audio from the call is being intercepted by an app on the local device. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_CONNECTING](../android/telecom/Call.md) The initial state of an outgoing`Call`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_DIALING](../android/telecom/Call.md) The state of an outgoing`Call`when dialing the remote number, but not yet connected. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_DISCONNECTED](../android/telecom/Call.md) The state of a`Call`when no further voice or other communication is being transmitted, the remote side has been or will inevitably be informed that the`Call`is no longer active, and the local data transport has or inevitably will release resources associated with this`Call`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_DISCONNECTING](../android/telecom/Call.md) The state of a`Call`when the user has initiated a disconnection of the call, but the call has not yet been disconnected by the underlying`ConnectionService`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_HOLDING](../android/telecom/Call.md) The state of a`Call`when in a holding state. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_NEW](../android/telecom/Call.md) The state of a`Call`when newly created. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_PULLING_CALL](../android/telecom/Call.md) The state of an external call which is in the process of being pulled from a remote device to the local device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_RINGING](../android/telecom/Call.md) The state of an incoming`Call`when ringing locally, but not yet connected. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_SELECT_PHONE_ACCOUNT](../android/telecom/Call.md) The state of an outgoing`Call`when waiting on user to select a [PhoneAccount](../android/telecom/PhoneAccount.md) through which to place the call. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_SIMULATED_RINGING](../android/telecom/Call.md) The state of a call that is being presented to the user after being in [STATE_AUDIO_PROCESSING](../android/telecom/Call.md). |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addConferenceParticipants](../android/telecom/Call.md))`(`participants:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Uri](../android/net/Uri.md)!>`)` Pulls participants to existing call by forming a conference call. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [answer](../android/telecom/Call.md))`(`videoState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Instructs this [STATE_RINGING](../android/telecom/Call.md)`Call`to answer. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [conference](../android/telecom/Call.md))`(`callToConferenceWith:` ` [Call](../android/telecom/Call.md)!`)` Instructs this`Call`to enter a conference. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deflect](../android/telecom/Call.md))`(`address:` ` [Uri](../android/net/Uri.md)!`)` Instructs this [STATE_RINGING](../android/telecom/Call.md)`Call`to deflect. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [disconnect](../android/telecom/Call.md))`()` Instructs this`Call`to disconnect. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getCannedTextResponses](../android/telecom/Call.md))`()` Obtains a list of canned, pre-configured message responses to present to the user as ways of rejecting an incoming`Call`using via a text message. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Call](../android/telecom/Call.md)!\>! | [getChildren](../android/telecom/Call.md))`()` Obtains the children of this conference`Call`, if any. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Call](../android/telecom/Call.md)!\>! | [getConferenceableCalls](../android/telecom/Call.md))`()` Returns the list of`Call`s with which this`Call`is allowed to conference. |
| [Call.Details](../android/telecom/Call.Details.md)! | [getDetails](../android/telecom/Call.md))`()` Obtains an object containing call details. |
| --- | --- |
| [Call](../android/telecom/Call.md)? | [getGenericConferenceActiveChildCall](../android/telecom/Call.md))`()` Returns the child [Call](../android/telecom/Call.md) in a generic conference that is currently active. |
| [Call](../android/telecom/Call.md)! | [getParent](../android/telecom/Call.md))`()` Obtains the parent of this`Call`in a conference, if any. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getRemainingPostDialSequence](../android/telecom/Call.md))`()` Obtains the post-dial sequence remaining to be emitted by this`Call`, if any. |
| --- | --- |
| [Call.RttCall](../android/telecom/Call.RttCall.md)? | [getRttCall](../android/telecom/Call.md))`()` Returns this call's RttCall object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getState](../android/telecom/Call.md))`()` Obtains the state of this`Call`. |
| [InCallService.VideoCall](../android/telecom/InCallService.VideoCall.md)! | [getVideoCall](../android/telecom/Call.md))`()` Obtains an object that can be used to display video from this`Call`. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [handoverTo](../android/telecom/Call.md))`(`toHandle:` ` [PhoneAccountHandle](../android/telecom/PhoneAccountHandle.md)!`, `videoState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `extras:` ` [Bundle](../android/os/Bundle.md)!`)` Initiates a handover of this [Call](../android/telecom/Call.md) to the [ConnectionService](../android/telecom/ConnectionService.md) identified by`toHandle`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [hold](../android/telecom/Call.md))`()` Instructs this`Call`to go on hold. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRttActive](../android/telecom/Call.md))`()` Returns whether this call has an active RTT connection. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [mergeConference](../android/telecom/Call.md))`()` Merges the calls within this conference. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [phoneAccountSelected](../android/telecom/Call.md))`(`accountHandle:` ` [PhoneAccountHandle](../android/telecom/PhoneAccountHandle.md)!`, `setDefault:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Notifies this`Call`that an account has been selected and to proceed with placing an outgoing call. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [playDtmfTone](../android/telecom/Call.md))`(`digit:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Instructs this`Call`to play a dual-tone multi-frequency signaling (DTMF) tone. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [postDialContinue](../android/telecom/Call.md))`(`proceed:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Instructs this`Call`to continue playing a post-dial DTMF string. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [pullExternalCall](../android/telecom/Call.md))`()` Initiates a request to the [ConnectionService](../android/telecom/ConnectionService.md) to pull an external call to the local device. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [putExtras](../android/telecom/Call.md))`(`extras:` ` [Bundle](../android/os/Bundle.md)!`)` Adds some extras to this [Call](../android/telecom/Call.md). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerCallback](../android/telecom/Call.md))`(`callback:` ` [Call.Callback](../android/telecom/Call.Callback.md)!`)` Registers a callback to this`Call`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerCallback](../android/telecom/Call.md))`(`callback:` ` [Call.Callback](../android/telecom/Call.Callback.md)!`, `handler:` ` [Handler](../android/os/Handler.md)!`)` Registers a callback to this`Call`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reject](../android/telecom/Call.md))`(`rejectWithMessage:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `textMessage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Instructs this [STATE_RINGING](../android/telecom/Call.md)`Call`to reject. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reject](../android/telecom/Call.md))`(`rejectReason:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Instructs the [ConnectionService](../android/telecom/ConnectionService.md) providing this [STATE_RINGING](../android/telecom/Call.md) call that the user has chosen to reject the call and has indicated a reason why the call is being rejected. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeExtras](../android/telecom/Call.md))`(`vararg` `keys:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Removes extras from this [Call](../android/telecom/Call.md). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeExtras](../android/telecom/Call.md))`(`keys:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Removes extras from this [Call](../android/telecom/Call.md). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [respondToRttRequest](../android/telecom/Call.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `accept:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Responds to an RTT request received via the [Callback.onRttRequest(Call, int)](../android/telecom/Call.Callback.md)))} callback. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendCallEvent](../android/telecom/Call.md))`(`event:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `extras:` ` [Bundle](../android/os/Bundle.md)!`)` Sends a`Call`event from this`Call`to the associated [Connection](../android/telecom/Connection.md) in the [ConnectionService](../android/telecom/ConnectionService.md). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendRttRequest](../android/telecom/Call.md))`()` Sends an RTT upgrade request to the remote end of the connection. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [splitFromConference](../android/telecom/Call.md))`()` Instructs this`Call`to split from any conference call with which it may be connected. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopDtmfTone](../android/telecom/Call.md))`()` Instructs this`Call`to stop any dual-tone multi-frequency signaling (DTMF) tone currently playing. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopRtt](../android/telecom/Call.md))`()` Terminate the RTT session on this call. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [swapConference](../android/telecom/Call.md))`()` Swaps the calls within this conference. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/telecom/Call.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unhold](../android/telecom/Call.md))`()` Instructs this [STATE_HOLDING](../android/telecom/Call.md) call to release from hold. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterCallback](../android/telecom/Call.md))`(`callback:` ` [Call.Callback](../android/telecom/Call.Callback.md)!`)` Unregisters a callback from this`Call`. |

## Constants

### AVAILABLE_PHONE_ACCOUNTS

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AVAILABLE_PHONE_ACCOUNTS: String
```

**Deprecated:** *Use the list from [EXTRA_SUGGESTED_PHONE_ACCOUNTS](../android/telecom/Call.md) instead.*

The key to retrieve the optional`PhoneAccount`s Telecom can bundle with its Call extras. Used to pass the phone accounts to display on the front end to the user in order to select phone accounts to (for example) place a call. 

 Value: "selectPhoneAccountAccounts"

### EVENT_CLEAR_DIAGNOSTIC_MESSAGE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_CLEAR_DIAGNOSTIC_MESSAGE: String
```

Event reported from the telecom framework when a diagnostic message previously raised with [EVENT_DISPLAY_DIAGNOSTIC_MESSAGE](../android/telecom/Call.md) has cleared and is no longer pertinent.

The [EXTRA_DIAGNOSTIC_MESSAGE_ID](../android/telecom/Call.md) indicates the diagnostic message which has been cleared.

The dialer app receives this event via [Call.Callback.onConnectionEvent(Call, String, Bundle)](../android/telecom/Call.Callback.md)). 

 Value: "android.telecom.event.CLEAR_DIAGNOSTIC_MESSAGE"

### EVENT_DISPLAY_DIAGNOSTIC_MESSAGE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_DISPLAY_DIAGNOSTIC_MESSAGE: String
```

Event reported from the Telecom stack to report an in-call diagnostic message which the dialer app may opt to display to the user. A diagnostic message is used to communicate scenarios the device has detected which may impact the quality of the ongoing call.

For example a problem with a bluetooth headset may generate a recommendation for the user to try using the speakerphone instead, or if the device detects it has entered a poor service area, the user might be warned so that they can finish their call prior to it dropping.

A diagnostic message is considered persistent in nature. When the user enters a poor service area, for example, the accompanying diagnostic message persists until they leave the area of poor service. Each message is accompanied with a [EXTRA_DIAGNOSTIC_MESSAGE_ID](../android/telecom/Call.md) which uniquely identifies the diagnostic condition being reported. The framework raises a call event of type [EVENT_CLEAR_DIAGNOSTIC_MESSAGE](../android/telecom/Call.md) when the condition reported has been cleared. The dialer app should display the diagnostic message until it is cleared. If multiple diagnostic messages are sent with different IDs (which have not yet been cleared) the dialer app should prioritize the most recently received message, but still provide the user with a means to review past messages.

The text of the message is found in [EXTRA_DIAGNOSTIC_MESSAGE](../android/telecom/Call.md) in the form of a human readable [CharSequence](../java/lang/CharSequence.md) which is intended for display in the call UX.

The telecom framework audibly notifies the user of the presence of a diagnostic message, so the dialer app needs only to concern itself with visually displaying the message.

The dialer app receives this event via [Call.Callback.onConnectionEvent(Call, String, Bundle)](../android/telecom/Call.Callback.md)). 

 Value: "android.telecom.event.DISPLAY_DIAGNOSTIC_MESSAGE"

### EXTRA_ASSERTED_DISPLAY_NAME

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_ASSERTED_DISPLAY_NAME: String
```

String value indicating the asserted display name reported via ImsCallProfile#EXTRA_ASSERTED_DISPLAY_NAME. [Connection.setExtras(Bundle)](../android/telecom/Connection.md))or [Connection.putExtras(Bundle)](../android/telecom/Connection.md))should be used to notify Telecom this extra has been set. 

 Value: "android.telecom.extra.ASSERTED_DISPLAY_NAME"

### EXTRA_DIAGNOSTIC_MESSAGE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_DIAGNOSTIC_MESSAGE: String
```

[CharSequence](../java/lang/CharSequence.md) extra used with [EVENT_DISPLAY_DIAGNOSTIC_MESSAGE](../android/telecom/Call.md). This is the diagnostic message the dialer app should display. 

 Value: "android.telecom.extra.DIAGNOSTIC_MESSAGE"

### EXTRA_DIAGNOSTIC_MESSAGE_ID

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_DIAGNOSTIC_MESSAGE_ID: String
```

Integer extra representing a message ID for a message posted via [EVENT_DISPLAY_DIAGNOSTIC_MESSAGE](../android/telecom/Call.md). Used to ensure that the dialer app knows when the message in question has cleared via [EVENT_CLEAR_DIAGNOSTIC_MESSAGE](../android/telecom/Call.md). 

 Value: "android.telecom.extra.DIAGNOSTIC_MESSAGE_ID"

### EXTRA_IS_BUSINESS_CALL

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_IS_BUSINESS_CALL: String
```

Boolean indicating that the call is a verified business call. [Connection.setExtras(Bundle)](../android/telecom/Connection.md))or [Connection.putExtras(Bundle)](../android/telecom/Connection.md))should be used to notify Telecom this extra has been set. 

 Value: "android.telecom.extra.IS_BUSINESS_CALL"

### EXTRA_IS_SUPPRESSED_BY_DO_NOT_DISTURB

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_IS_SUPPRESSED_BY_DO_NOT_DISTURB: String
```

Extra key intended for [InCallService](../android/telecom/InCallService.md) s that notify the user of an incoming call. When EXTRA_IS_SUPPRESSED_BY_DO_NOT_DISTURB returns true, the [InCallService](../android/telecom/InCallService.md) should not interrupt the user of the incoming call because the call is being suppressed by Do Not Disturb settings. This extra will be removed from the [Call](../android/telecom/Call.md) object for [InCallService](../android/telecom/InCallService.md) s that do not hold the [android.Manifest.permission#READ_CONTACTS](../android/Manifest.permission.md) permission. 

 Value: "android.telecom.extra.IS_SUPPRESSED_BY_DO_NOT_DISTURB"

### EXTRA_LAST_EMERGENCY_CALLBACK_TIME_MILLIS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_LAST_EMERGENCY_CALLBACK_TIME_MILLIS: String
```

Extra key used to indicate the time (in milliseconds since midnight, January 1, 1970 UTC) when the last outgoing emergency call was made. This is used to identify potential emergency callbacks. 

 Value: "android.telecom.extra.LAST_EMERGENCY_CALLBACK_TIME_MILLIS"

### EXTRA_SILENT_RINGING_REQUESTED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_SILENT_RINGING_REQUESTED: String
```

Extra key used to indicate whether a [CallScreeningService](../android/telecom/CallScreeningService.md) has requested to silence the ringtone for a call. If the [InCallService](../android/telecom/InCallService.md) declares [TelecomManager.METADATA_IN_CALL_SERVICE_RINGING](../android/telecom/TelecomManager.md) in its manifest, it should not play a ringtone for an incoming call with this extra key set. 

 Value: "android.telecom.extra.SILENT_RINGING_REQUESTED"

### EXTRA_SUGGESTED_PHONE_ACCOUNTS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_SUGGESTED_PHONE_ACCOUNTS: String
```

Key for extra used to pass along a list of [PhoneAccountSuggestion](../android/telecom/PhoneAccountSuggestion.md) s to the in-call UI when a call enters the [STATE_SELECT_PHONE_ACCOUNT](../android/telecom/Call.md) state. The list included here will have the same length and be in the same order as the list passed with [AVAILABLE_PHONE_ACCOUNTS](../android/telecom/Call.md). 

 Value: "android.telecom.extra.SUGGESTED_PHONE_ACCOUNTS"

### REJECT_REASON_DECLINED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REJECT_REASON_DECLINED: Int
```

Reject reason used with [reject(int)](../android/telecom/Call.md))to indicate that the user is rejecting this call because they have declined to answer it. This typically means that they are unable to answer the call at this time and would prefer it be sent to voicemail. 

 Value: 1

### REJECT_REASON_UNWANTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REJECT_REASON_UNWANTED: Int
```

Reject reason used with [reject(int)](../android/telecom/Call.md))to indicate that the user is rejecting this call because it is an unwanted call. This allows the user to indicate that they are rejecting a call because it is likely a nuisance call. 

 Value: 2

### STATE_ACTIVE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_ACTIVE: Int
```

The state of a`Call`when actively supporting conversation. 

 Value: 4

### STATE_AUDIO_PROCESSING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_AUDIO_PROCESSING: Int
```

The state of a call that is active with the network, but the audio from the call is being intercepted by an app on the local device. Telecom does not hold audio focus in this state, and the call will be invisible to the user except for a persistent notification. 

 Value: 12

### STATE_CONNECTING

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_CONNECTING: Int
```

The initial state of an outgoing`Call`. Common transitions are to [STATE_DIALING](../android/telecom/Call.md) state for a successful call or [STATE_DISCONNECTED](../android/telecom/Call.md) if it failed. 

 Value: 9

### STATE_DIALING

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_DIALING: Int
```

The state of an outgoing`Call`when dialing the remote number, but not yet connected. 

 Value: 1

### STATE_DISCONNECTED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_DISCONNECTED: Int
```

The state of a`Call`when no further voice or other communication is being transmitted, the remote side has been or will inevitably be informed that the`Call`is no longer active, and the local data transport has or inevitably will release resources associated with this`Call`. 

 Value: 7

### STATE_DISCONNECTING

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_DISCONNECTING: Int
```

The state of a`Call`when the user has initiated a disconnection of the call, but the call has not yet been disconnected by the underlying`ConnectionService`. The next state of the call is (potentially) [STATE_DISCONNECTED](../android/telecom/Call.md). 

 Value: 10

### STATE_HOLDING

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_HOLDING: Int
```

The state of a`Call`when in a holding state. 

 Value: 3

### STATE_NEW

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_NEW: Int
```

The state of a`Call`when newly created. 

 Value: 0

### STATE_PULLING_CALL

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_PULLING_CALL: Int
```

The state of an external call which is in the process of being pulled from a remote device to the local device.

A call can only be in this state if the [Details.PROPERTY_IS_EXTERNAL_CALL](../android/telecom/Call.Details.md) property and [Details.CAPABILITY_CAN_PULL_CALL](../android/telecom/Call.Details.md) capability are set on the call.

An [InCallService](../android/telecom/InCallService.md) will only see this state if it has the [TelecomManager.METADATA_INCLUDE_EXTERNAL_CALLS](../android/telecom/TelecomManager.md) metadata set to`true`in its manifest. 

 Value: 11

### STATE_RINGING

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_RINGING: Int
```

The state of an incoming`Call`when ringing locally, but not yet connected. 

 Value: 2

### STATE_SELECT_PHONE_ACCOUNT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_SELECT_PHONE_ACCOUNT: Int
```

The state of an outgoing`Call`when waiting on user to select a [PhoneAccount](../android/telecom/PhoneAccount.md) through which to place the call. 

 Value: 8

### STATE_SIMULATED_RINGING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_SIMULATED_RINGING: Int
```

The state of a call that is being presented to the user after being in [STATE_AUDIO_PROCESSING](../android/telecom/Call.md). The call is still active with the network in this case, and Telecom will hold audio focus and play a ringtone if appropriate. 

 Value: 13

## Public methods

### addConferenceParticipants

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addConferenceParticipants(participants: MutableList<Uri!>): Unit
```

Pulls participants to existing call by forming a conference call. See [Details.CAPABILITY_ADD_PARTICIPANT](../android/telecom/Call.Details.md).

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `participants` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Uri](../android/net/Uri.md)!\>:participants to be pulled to existing call. This value cannot be`null`. |

### answer

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun answer(videoState: Int): Unit
```

Instructs this [STATE_RINGING](../android/telecom/Call.md)`Call`to answer.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `videoState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The video state in which to answer the call. Value is either`0`or a combination of [android.telecom.VideoProfile#STATE_AUDIO_ONLY](../android/telecom/VideoProfile.md), [android.telecom.VideoProfile#STATE_TX_ENABLED](../android/telecom/VideoProfile.md), [android.telecom.VideoProfile#STATE_RX_ENABLED](../android/telecom/VideoProfile.md), [android.telecom.VideoProfile#STATE_BIDIRECTIONAL](../android/telecom/VideoProfile.md), and [android.telecom.VideoProfile#STATE_PAUSED](../android/telecom/VideoProfile.md) |

### conference

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun conference(callToConferenceWith: Call!): Unit
```

Instructs this`Call`to enter a conference.

| Parameters ||
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| `callToConferenceWith` | [Call](../android/telecom/Call.md)!:The other call with which to conference. |

### deflect

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun deflect(address: Uri!): Unit
```

Instructs this [STATE_RINGING](../android/telecom/Call.md)`Call`to deflect.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------|
| `address` | [Uri](../android/net/Uri.md)!:The address to which the call will be deflected. |

### disconnect

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun disconnect(): Unit
```

Instructs this`Call`to disconnect. 

### getCannedTextResponses

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCannedTextResponses(): MutableList<String!>!
```

Obtains a list of canned, pre-configured message responses to present to the user as ways of rejecting an incoming`Call`using via a text message.

*Note:* Since canned responses may be loaded from the file system, they are not guaranteed to be present when this [Call](../android/telecom/Call.md) is first added to the [InCallService](../android/telecom/InCallService.md) via [InCallService.onCallAdded(Call)](../android/telecom/InCallService.md)). The callback [Call.Callback.onCannedTextResponsesLoaded(Call, List)](../android/telecom/Call.Callback.md))will be called when/if canned responses for the call become available.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | A list of canned text message responses. |

**See Also**

- [#reject(boolean, String)](../android/telecom/Call.md)) 

### getChildren

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getChildren(): MutableList<Call!>!
```

Obtains the children of this conference`Call`, if any.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Call](../android/telecom/Call.md)!>! | The children of this`Call`if this`Call`is a conference, or an empty`List`otherwise. |

### getConferenceableCalls

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConferenceableCalls(): MutableList<Call!>!
```

Returns the list of`Call`s with which this`Call`is allowed to conference.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Call](../android/telecom/Call.md)!>! | The list of conferenceable`Call`s. |

### getDetails

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDetails(): Call.Details!
```

Obtains an object containing call details.

| Return ||
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Call.Details](../android/telecom/Call.Details.md)! | A [Details](../android/telecom/Call.Details.md) object. Depending on the state of the`Call`, the result may be`null`. |

### getGenericConferenceActiveChildCall

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGenericConferenceActiveChildCall(): Call?
```

Returns the child [Call](../android/telecom/Call.md) in a generic conference that is currently active. A "generic conference" is the mechanism used to support two simultaneous calls on a device in CDMA networks. It is effectively equivalent to having one call active and one call on hold in GSM or IMS calls. This method returns the currently active call. In a generic conference, the network exposes the conference to us as a single call, and we switch between talking to the two participants using a CDMA flash command. Since the network exposes no additional information about the call, the only way we know which caller we're currently talking to is by keeping track of the flash commands that we've sent to the network. For calls that are not generic conferences, or when the generic conference has more than 2 children, returns`null`.

| Return ||
|-------------------------------------------------------------------------------|------------------------|
| [Call](../android/telecom/Call.md)? | The active child call. |

**See Also**

- [android.telecom.Call.Details#PROPERTY_GENERIC_CONFERENCE](../android/telecom/Call.Details.md) 

### getParent

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getParent(): Call!
```

Obtains the parent of this`Call`in a conference, if any.

| Return ||
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Call](../android/telecom/Call.md)! | The parent`Call`, or`null`if this`Call`is not a child of any conference`Call`s. |

### getRemainingPostDialSequence

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRemainingPostDialSequence(): String!
```

Obtains the post-dial sequence remaining to be emitted by this`Call`, if any.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The remaining post-dial sequence, or`null`if there is no post-dial sequence remaining or this`Call`is not in a post-dial state. |

### getRttCall

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRttCall(): Call.RttCall?
```

Returns this call's RttCall object. The [RttCall](../android/telecom/Call.RttCall.md) instance is used to send and receive RTT text data, as well as to change the RTT mode.

| Return ||
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [Call.RttCall](../android/telecom/Call.RttCall.md)? | A [Call.RttCall](../android/telecom/Call.RttCall.md).`null`if there is no active RTT connection. |

### getState

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getState(): Int
```

**Deprecated:** *The call state is available via [Call.Details.getState()](../android/telecom/Call.Details.md)).*

Obtains the state of this`Call`.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The call state. Value is [android.telecom.Call#STATE_NEW](../android/telecom/Call.md), [android.telecom.Call#STATE_DIALING](../android/telecom/Call.md), [android.telecom.Call#STATE_RINGING](../android/telecom/Call.md), [android.telecom.Call#STATE_HOLDING](../android/telecom/Call.md), [android.telecom.Call#STATE_ACTIVE](../android/telecom/Call.md), [android.telecom.Call#STATE_DISCONNECTED](../android/telecom/Call.md), [android.telecom.Call#STATE_SELECT_PHONE_ACCOUNT](../android/telecom/Call.md), [android.telecom.Call#STATE_CONNECTING](../android/telecom/Call.md), [android.telecom.Call#STATE_DISCONNECTING](../android/telecom/Call.md), [android.telecom.Call#STATE_PULLING_CALL](../android/telecom/Call.md), [android.telecom.Call#STATE_AUDIO_PROCESSING](../android/telecom/Call.md), or [android.telecom.Call#STATE_SIMULATED_RINGING](../android/telecom/Call.md) |

### getVideoCall

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVideoCall(): InCallService.VideoCall!
```

Obtains an object that can be used to display video from this`Call`.

| Return ||
|--------------------------------------------------------------------------------------------------------------------|---------------------|
| [InCallService.VideoCall](../android/telecom/InCallService.VideoCall.md)! | An`Call.VideoCall`. |

### handoverTo

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun handoverTo(
    toHandle: PhoneAccountHandle!, 
    videoState: Int, 
    extras: Bundle!
): Unit
```

Initiates a handover of this [Call](../android/telecom/Call.md) to the [ConnectionService](../android/telecom/ConnectionService.md) identified by`toHandle`. The videoState specified indicates the desired video state after the handover.

A call handover is the process where an ongoing call is transferred from one app (i.e. [ConnectionService](../android/telecom/ConnectionService.md) to another app. The user could, for example, choose to continue a mobile network call in a video calling app. The mobile network call via the Telephony stack is referred to as the source of the handover, and the video calling app is referred to as the destination.

When considering a handover scenario the device this method is called on is considered the*initiating* device (since the user initiates the handover from this device), and the other device is considered the*receiving*device.

When this method is called on the*initiating* device, the Telecom framework will bind to the [ConnectionService](../android/telecom/ConnectionService.md) defined by the`toHandle` [PhoneAccountHandle](../android/telecom/PhoneAccountHandle.md) and invoke [ConnectionService.onCreateOutgoingHandoverConnection(PhoneAccountHandle,](../android/telecom/ConnectionService.md))to inform the destination app that a request has been made to handover a call to it. The app returns an instance of [Connection](../android/telecom/Connection.md) to represent the handover call At this point the app should display UI to indicate to the user that a call handover is in process.

The destination app is responsible for communicating the handover request from the*initiating* device to the*receiving*device.

When the app on the*receiving* device receives the handover request, it calls [TelecomManager.acceptHandover(Uri, int, PhoneAccountHandle)](../android/telecom/TelecomManager.md))to continue the handover process from the*initiating* device to the*receiving* device. At this point the destination app on the*receiving*device should show UI to allow the user to choose whether they want to continue their call in the destination app.

When the destination app on the*receiving* device calls [TelecomManager.acceptHandover(Uri, int, PhoneAccountHandle)](../android/telecom/TelecomManager.md)), Telecom will bind to its [ConnectionService](../android/telecom/ConnectionService.md) and call [ConnectionService.onCreateIncomingHandoverConnection(PhoneAccountHandle,](../android/telecom/ConnectionService.md))to inform it of the handover request. The app returns an instance of [Connection](../android/telecom/Connection.md) to represent the handover call.

If the user of the*receiving* device accepts the handover, the app calls [Connection.setActive()](../android/telecom/Connection.md))to complete the handover process; Telecom will disconnect the original call. If the user rejects the handover, the app calls [Connection.setDisconnected(DisconnectCause)](../android/telecom/Connection.md))and specifies a [DisconnectCause](../android/telecom/DisconnectCause.md) of [DisconnectCause.CANCELED](../android/telecom/DisconnectCause.md) to indicate that the handover has been cancelled.

Telecom will only allow handovers from [PhoneAccount](../android/telecom/PhoneAccount.md) s which declare [PhoneAccount.EXTRA_SUPPORTS_HANDOVER_FROM](../android/telecom/PhoneAccount.md). Similarly, the [PhoneAccount](../android/telecom/PhoneAccount.md) specified by`toHandle`must declare [PhoneAccount.EXTRA_SUPPORTS_HANDOVER_TO](../android/telecom/PhoneAccount.md).

Errors in the handover process are reported to the [InCallService](../android/telecom/InCallService.md) via [Callback.onHandoverFailed(Call, int)](../android/telecom/Call.Callback.md)). Errors in the handover process are reported to the involved [ConnectionService](../android/telecom/ConnectionService.md) s via [ConnectionService.onHandoverFailed(ConnectionRequest, int)](../android/telecom/ConnectionService.md)).

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `toHandle` | [PhoneAccountHandle](../android/telecom/PhoneAccountHandle.md)!: [PhoneAccountHandle](../android/telecom/PhoneAccountHandle.md) of the [ConnectionService](../android/telecom/ConnectionService.md) to handover this call to. |
| `videoState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Indicates the video state desired after the handover (see the`STATE_*`constants defined in [VideoProfile](../android/telecom/VideoProfile.md)). Value is either`0`or a combination of [android.telecom.VideoProfile#STATE_AUDIO_ONLY](../android/telecom/VideoProfile.md), [android.telecom.VideoProfile#STATE_TX_ENABLED](../android/telecom/VideoProfile.md), [android.telecom.VideoProfile#STATE_RX_ENABLED](../android/telecom/VideoProfile.md), [android.telecom.VideoProfile#STATE_BIDIRECTIONAL](../android/telecom/VideoProfile.md), and [android.telecom.VideoProfile#STATE_PAUSED](../android/telecom/VideoProfile.md) |
| `extras` | [Bundle](../android/os/Bundle.md)!:Bundle containing extra information to be passed to the [ConnectionService](../android/telecom/ConnectionService.md) |
| --- | --- |

### hold

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hold(): Unit
```

Instructs this`Call`to go on hold. 

### isRttActive

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isRttActive(): Boolean
```

Returns whether this call has an active RTT connection.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if there is a connection, false otherwise. |

### mergeConference

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun mergeConference(): Unit
```

Merges the calls within this conference. See [Details.CAPABILITY_MERGE_CONFERENCE](../android/telecom/Call.Details.md). 

### phoneAccountSelected

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun phoneAccountSelected(
    accountHandle: PhoneAccountHandle!, 
    setDefault: Boolean
): Unit
```

Notifies this`Call`that an account has been selected and to proceed with placing an outgoing call. Optionally sets this account as the default account. 

### playDtmfTone

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun playDtmfTone(digit: Char): Unit
```

Instructs this`Call`to play a dual-tone multi-frequency signaling (DTMF) tone.

Tones are both played locally for the user to hear and sent to the network to be relayed to the remote device.

You must ensure that any call to [playDtmfTone(char)](../android/telecom/Call.md))is followed by a matching call to [stopDtmfTone()](../android/telecom/Call.md))and that each tone is stopped before a new one is started. The play and stop commands are relayed to the underlying [android.telecom.ConnectionService](../android/telecom/ConnectionService.md) as executed; implementations may not correctly handle out of order commands.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `digit` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):A character representing the DTMF digit for which to play the tone. This value must be one of`'0'`through`'9'`,`'*'`or`'#'`. |

### postDialContinue

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun postDialContinue(proceed: Boolean): Unit
```

Instructs this`Call`to continue playing a post-dial DTMF string. A post-dial DTMF string is a string of digits entered after a phone number, when dialed, that are immediately sent as DTMF tones to the recipient as soon as the connection is made. If the DTMF string contains a [TelecomManager.DTMF_CHARACTER_PAUSE](../android/telecom/TelecomManager.md) symbol, this`Call`will temporarily pause playing the tones for a pre-defined period of time. If the DTMF string contains a [TelecomManager.DTMF_CHARACTER_WAIT](../android/telecom/TelecomManager.md) symbol, this`Call`will pause playing the tones and notify callbacks via [Callback.onPostDialWait(Call, String)](../android/telecom/Call.Callback.md)). At this point, the in-call app should display to the user an indication of this state and an affordance to continue the postdial sequence. When the user decides to continue the postdial sequence, the in-call app should invoke the [postDialContinue(boolean)](../android/telecom/Call.md))method.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `proceed` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether or not to continue with the post-dial sequence. |

### pullExternalCall

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun pullExternalCall(): Unit
```

Initiates a request to the [ConnectionService](../android/telecom/ConnectionService.md) to pull an external call to the local device.

Calls to this method are ignored if the call does not have the [Call.Details.PROPERTY_IS_EXTERNAL_CALL](../android/telecom/Call.Details.md) property set.

An [InCallService](../android/telecom/InCallService.md) will only see calls which support this method if it has the [TelecomManager.METADATA_INCLUDE_EXTERNAL_CALLS](../android/telecom/TelecomManager.md) metadata set to`true`in its manifest. 

### putExtras

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun putExtras(extras: Bundle!): Unit
```

Adds some extras to this [Call](../android/telecom/Call.md). Existing keys are replaced and new ones are added.

No assumptions should be made as to how an In-Call UI or service will handle these extras. Keys should be fully qualified (e.g., com.example.MY_EXTRA) to avoid conflicts.

Extras added using this method will be made available to the [ConnectionService](../android/telecom/ConnectionService.md) associated with this [Call](../android/telecom/Call.md) and notified via [Connection.onExtrasChanged(Bundle)](../android/telecom/Connection.md)).

Extras added using this method will also be available to other running [InCallService](../android/telecom/InCallService.md) s and notified via [Call.Callback.onDetailsChanged(Call, Details)](../android/telecom/Call.Callback.md)). The extras can be accessed via [Details.getExtras()](../android/telecom/Call.Details.md)).

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------|
| `extras` | [Bundle](../android/os/Bundle.md)!:The extras to add. |

### registerCallback

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun registerCallback(callback: Call.Callback!): Unit
```

Registers a callback to this`Call`.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `callback` | [Call.Callback](../android/telecom/Call.Callback.md)!:A`Callback`. |

### registerCallback

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun registerCallback(
    callback: Call.Callback!, 
    handler: Handler!
): Unit
```

Registers a callback to this`Call`.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [Call.Callback](../android/telecom/Call.Callback.md)!:A`Callback`. |
| `handler` | [Handler](../android/os/Handler.md)!:A handler which command and status changes will be delivered to. |

### reject

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun reject(
    rejectWithMessage: Boolean, 
    textMessage: String!
): Unit
```

Instructs this [STATE_RINGING](../android/telecom/Call.md)`Call`to reject.

| Parameters ||
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `rejectWithMessage` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether to reject with a text message. |
| `textMessage` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:An optional text message with which to respond. |

### reject

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun reject(rejectReason: Int): Unit
```

Instructs the [ConnectionService](../android/telecom/ConnectionService.md) providing this [STATE_RINGING](../android/telecom/Call.md) call that the user has chosen to reject the call and has indicated a reason why the call is being rejected.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `rejectReason` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the reason the call is being rejected. Value is [android.telecom.Call#REJECT_REASON_DECLINED](../android/telecom/Call.md), or [android.telecom.Call#REJECT_REASON_UNWANTED](../android/telecom/Call.md) |

### removeExtras

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeExtras(vararg keys: String!): Unit
```

Removes extras from this [Call](../android/telecom/Call.md).

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------|
| `keys` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The keys of the extras to remove. |

### removeExtras

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeExtras(keys: MutableList<String!>!): Unit
```

Removes extras from this [Call](../android/telecom/Call.md).

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `keys` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:The keys of the extras to remove. |

### respondToRttRequest

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun respondToRttRequest(
    id: Int, 
    accept: Boolean
): Unit
```

Responds to an RTT request received via the [Callback.onRttRequest(Call, int)](../android/telecom/Call.Callback.md)))} callback. The ID used here should be the same as the ID that was received via the callback.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The request ID received via [Callback.onRttRequest(Call, int)](../android/telecom/Call.Callback.md)) |
| `accept` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if the RTT request should be accepted,`false`otherwise. |

### sendCallEvent

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun sendCallEvent(
    event: String!, 
    extras: Bundle!
): Unit
```

Sends a`Call`event from this`Call`to the associated [Connection](../android/telecom/Connection.md) in the [ConnectionService](../android/telecom/ConnectionService.md).

Call events are used to communicate point in time information from an [InCallService](../android/telecom/InCallService.md) to a [ConnectionService](../android/telecom/ConnectionService.md). A [ConnectionService](../android/telecom/ConnectionService.md) implementation could define events which enable the [InCallService](../android/telecom/InCallService.md), for example, toggle a unique feature of the [ConnectionService](../android/telecom/ConnectionService.md).

A [ConnectionService](../android/telecom/ConnectionService.md) can communicate to the [InCallService](../android/telecom/InCallService.md) using [Connection.sendConnectionEvent(String, Bundle)](../android/telecom/Connection.md)).

Events are exposed to [ConnectionService](../android/telecom/ConnectionService.md) implementations via [android.telecom.Connection#onCallEvent(String, Bundle)](../android/telecom/Connection.md)).

No assumptions should be made as to how a [ConnectionService](../android/telecom/ConnectionService.md) will handle these events. The [InCallService](../android/telecom/InCallService.md) must assume that the [ConnectionService](../android/telecom/ConnectionService.md) could chose to ignore some events altogether.

Events should be fully qualified (e.g.,`com.example.event.MY_EVENT`) to avoid conflicts between [InCallService](../android/telecom/InCallService.md) implementations. Further, [InCallService](../android/telecom/InCallService.md) implementations shall not re-purpose events in the`android.*`namespace, nor shall they define their own event types in this namespace. When defining a custom event type, ensure the contents of the extras [Bundle](../android/os/Bundle.md) is clearly defined. Extra keys for this bundle should be named similar to the event type (e.g.`com.example.extra.MY_EXTRA`).

When defining events and the associated extras, it is important to keep their behavior consistent when the associated [InCallService](../android/telecom/InCallService.md) is updated. Support for deprecated events/extras should me maintained to ensure backwards compatibility with older [ConnectionService](../android/telecom/ConnectionService.md) implementations which were built to support the older behavior.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The connection event. |
| `extras` | [Bundle](../android/os/Bundle.md)!:Bundle containing extra information associated with the event. |

### sendRttRequest

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun sendRttRequest(): Unit
```

Sends an RTT upgrade request to the remote end of the connection. Success is not guaranteed, and notification of success will be via the [Callback.onRttStatusChanged(Call, boolean, RttCall)](../android/telecom/Call.Callback.md))callback. 

### splitFromConference

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun splitFromConference(): Unit
```

Instructs this`Call`to split from any conference call with which it may be connected. 

### stopDtmfTone

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun stopDtmfTone(): Unit
```

Instructs this`Call`to stop any dual-tone multi-frequency signaling (DTMF) tone currently playing. DTMF tones are played by calling [playDtmfTone(char)](../android/telecom/Call.md)). If no DTMF tone is currently playing, this method will do nothing. 

### stopRtt

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun stopRtt(): Unit
```

Terminate the RTT session on this call. The resulting state change will be notified via the [Callback.onRttStatusChanged(Call, boolean, RttCall)](../android/telecom/Call.Callback.md))callback. 

### swapConference

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun swapConference(): Unit
```

Swaps the calls within this conference. See [Details.CAPABILITY_SWAP_CONFERENCE](../android/telecom/Call.Details.md). 

### toString

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### unhold

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unhold(): Unit
```

Instructs this [STATE_HOLDING](../android/telecom/Call.md) call to release from hold. 

### unregisterCallback

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unregisterCallback(callback: Call.Callback!): Unit
```

Unregisters a callback from this`Call`.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `callback` | [Call.Callback](../android/telecom/Call.Callback.md)!:A`Callback`. |
