# Call

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Call

Kotlin| [Java](https://developer.android.com/reference/android/telecom/Call "View this page in Java") 
| --- | --- |

```
class Call
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telecom.Call](https://developer.android.com/reference/kotlin/android/telecom/Call#) |

Represents an ongoing phone call that the in-call app should present to the user.

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Callback](https://developer.android.com/reference/kotlin/android/telecom/Call.Callback) Defines callbacks which inform the [InCallService](https://developer.android.com/reference/kotlin/android/telecom/InCallService) of changes to a [Call](https://developer.android.com/reference/kotlin/android/telecom/Call#). |
| | [Details](https://developer.android.com/reference/kotlin/android/telecom/Call.Details) <br /> |
| | [RttCall](https://developer.android.com/reference/kotlin/android/telecom/Call.RttCall) A class that holds the state that describes the state of the RTT channel to the remote party, if it is active. |
| --- | --- |

| Constants ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [AVAILABLE_PHONE_ACCOUNTS](https://developer.android.com/reference/kotlin/android/telecom/Call#AVAILABLE_PHONE_ACCOUNTS:kotlin.String) The key to retrieve the optional`PhoneAccount`s Telecom can bundle with its Call extras. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EVENT_CLEAR_DIAGNOSTIC_MESSAGE](https://developer.android.com/reference/kotlin/android/telecom/Call#EVENT_CLEAR_DIAGNOSTIC_MESSAGE:kotlin.String) Event reported from the telecom framework when a diagnostic message previously raised with [EVENT_DISPLAY_DIAGNOSTIC_MESSAGE](https://developer.android.com/reference/kotlin/android/telecom/Call#EVENT_DISPLAY_DIAGNOSTIC_MESSAGE:kotlin.String) has cleared and is no longer pertinent. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EVENT_DISPLAY_DIAGNOSTIC_MESSAGE](https://developer.android.com/reference/kotlin/android/telecom/Call#EVENT_DISPLAY_DIAGNOSTIC_MESSAGE:kotlin.String) Event reported from the Telecom stack to report an in-call diagnostic message which the dialer app may opt to display to the user. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_ASSERTED_DISPLAY_NAME](https://developer.android.com/reference/kotlin/android/telecom/Call#EXTRA_ASSERTED_DISPLAY_NAME:kotlin.String) String value indicating the asserted display name reported via ImsCallProfile#EXTRA_ASSERTED_DISPLAY_NAME. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_DIAGNOSTIC_MESSAGE](https://developer.android.com/reference/kotlin/android/telecom/Call#EXTRA_DIAGNOSTIC_MESSAGE:kotlin.String) [CharSequence](https://developer.android.com/reference/kotlin/java/lang/CharSequence.html#) extra used with [EVENT_DISPLAY_DIAGNOSTIC_MESSAGE](https://developer.android.com/reference/kotlin/android/telecom/Call#EVENT_DISPLAY_DIAGNOSTIC_MESSAGE:kotlin.String). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_DIAGNOSTIC_MESSAGE_ID](https://developer.android.com/reference/kotlin/android/telecom/Call#EXTRA_DIAGNOSTIC_MESSAGE_ID:kotlin.String) Integer extra representing a message ID for a message posted via [EVENT_DISPLAY_DIAGNOSTIC_MESSAGE](https://developer.android.com/reference/kotlin/android/telecom/Call#EVENT_DISPLAY_DIAGNOSTIC_MESSAGE:kotlin.String). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_IS_BUSINESS_CALL](https://developer.android.com/reference/kotlin/android/telecom/Call#EXTRA_IS_BUSINESS_CALL:kotlin.String) Boolean indicating that the call is a verified business call. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_IS_SUPPRESSED_BY_DO_NOT_DISTURB](https://developer.android.com/reference/kotlin/android/telecom/Call#EXTRA_IS_SUPPRESSED_BY_DO_NOT_DISTURB:kotlin.String) Extra key intended for [InCallService](https://developer.android.com/reference/kotlin/android/telecom/InCallService) s that notify the user of an incoming call. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_LAST_EMERGENCY_CALLBACK_TIME_MILLIS](https://developer.android.com/reference/kotlin/android/telecom/Call#EXTRA_LAST_EMERGENCY_CALLBACK_TIME_MILLIS:kotlin.String) Extra key used to indicate the time (in milliseconds since midnight, January 1, 1970 UTC) when the last outgoing emergency call was made. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_SILENT_RINGING_REQUESTED](https://developer.android.com/reference/kotlin/android/telecom/Call#EXTRA_SILENT_RINGING_REQUESTED:kotlin.String) Extra key used to indicate whether a [CallScreeningService](https://developer.android.com/reference/kotlin/android/telecom/CallScreeningService) has requested to silence the ringtone for a call. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_SUGGESTED_PHONE_ACCOUNTS](https://developer.android.com/reference/kotlin/android/telecom/Call#EXTRA_SUGGESTED_PHONE_ACCOUNTS:kotlin.String) Key for extra used to pass along a list of [PhoneAccountSuggestion](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountSuggestion) s to the in-call UI when a call enters the [STATE_SELECT_PHONE_ACCOUNT](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_SELECT_PHONE_ACCOUNT:kotlin.Int) state. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REJECT_REASON_DECLINED](https://developer.android.com/reference/kotlin/android/telecom/Call#REJECT_REASON_DECLINED:kotlin.Int) Reject reason used with [reject(int)](https://developer.android.com/reference/kotlin/android/telecom/Call#reject(kotlin.Int))to indicate that the user is rejecting this call because they have declined to answer it. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REJECT_REASON_UNWANTED](https://developer.android.com/reference/kotlin/android/telecom/Call#REJECT_REASON_UNWANTED:kotlin.Int) Reject reason used with [reject(int)](https://developer.android.com/reference/kotlin/android/telecom/Call#reject(kotlin.Int))to indicate that the user is rejecting this call because it is an unwanted call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_ACTIVE](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_ACTIVE:kotlin.Int) The state of a`Call`when actively supporting conversation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_AUDIO_PROCESSING](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_AUDIO_PROCESSING:kotlin.Int) The state of a call that is active with the network, but the audio from the call is being intercepted by an app on the local device. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_CONNECTING](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_CONNECTING:kotlin.Int) The initial state of an outgoing`Call`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_DIALING](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_DIALING:kotlin.Int) The state of an outgoing`Call`when dialing the remote number, but not yet connected. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_DISCONNECTED](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_DISCONNECTED:kotlin.Int) The state of a`Call`when no further voice or other communication is being transmitted, the remote side has been or will inevitably be informed that the`Call`is no longer active, and the local data transport has or inevitably will release resources associated with this`Call`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_DISCONNECTING](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_DISCONNECTING:kotlin.Int) The state of a`Call`when the user has initiated a disconnection of the call, but the call has not yet been disconnected by the underlying`ConnectionService`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_HOLDING](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_HOLDING:kotlin.Int) The state of a`Call`when in a holding state. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_NEW](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_NEW:kotlin.Int) The state of a`Call`when newly created. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_PULLING_CALL](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_PULLING_CALL:kotlin.Int) The state of an external call which is in the process of being pulled from a remote device to the local device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_RINGING](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_RINGING:kotlin.Int) The state of an incoming`Call`when ringing locally, but not yet connected. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_SELECT_PHONE_ACCOUNT](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_SELECT_PHONE_ACCOUNT:kotlin.Int) The state of an outgoing`Call`when waiting on user to select a [PhoneAccount](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount) through which to place the call. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_SIMULATED_RINGING](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_SIMULATED_RINGING:kotlin.Int) The state of a call that is being presented to the user after being in [STATE_AUDIO_PROCESSING](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_AUDIO_PROCESSING:kotlin.Int). |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addConferenceParticipants](https://developer.android.com/reference/kotlin/android/telecom/Call#addConferenceParticipants(kotlin.collections.MutableList))`(`participants:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!>`)` Pulls participants to existing call by forming a conference call. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [answer](https://developer.android.com/reference/kotlin/android/telecom/Call#answer(kotlin.Int))`(`videoState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Instructs this [STATE_RINGING](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_RINGING:kotlin.Int)`Call`to answer. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [conference](https://developer.android.com/reference/kotlin/android/telecom/Call#conference(android.telecom.Call))`(`callToConferenceWith:` ` [Call](https://developer.android.com/reference/kotlin/android/telecom/Call#)!`)` Instructs this`Call`to enter a conference. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deflect](https://developer.android.com/reference/kotlin/android/telecom/Call#deflect(android.net.Uri))`(`address:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`)` Instructs this [STATE_RINGING](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_RINGING:kotlin.Int)`Call`to deflect. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [disconnect](https://developer.android.com/reference/kotlin/android/telecom/Call#disconnect())`()` Instructs this`Call`to disconnect. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getCannedTextResponses](https://developer.android.com/reference/kotlin/android/telecom/Call#getCannedTextResponses())`()` Obtains a list of canned, pre-configured message responses to present to the user as ways of rejecting an incoming`Call`using via a text message. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Call](https://developer.android.com/reference/kotlin/android/telecom/Call#)!\>! | [getChildren](https://developer.android.com/reference/kotlin/android/telecom/Call#getChildren())`()` Obtains the children of this conference`Call`, if any. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Call](https://developer.android.com/reference/kotlin/android/telecom/Call#)!\>! | [getConferenceableCalls](https://developer.android.com/reference/kotlin/android/telecom/Call#getConferenceableCalls())`()` Returns the list of`Call`s with which this`Call`is allowed to conference. |
| [Call.Details](https://developer.android.com/reference/kotlin/android/telecom/Call.Details)! | [getDetails](https://developer.android.com/reference/kotlin/android/telecom/Call#getDetails())`()` Obtains an object containing call details. |
| --- | --- |
| [Call](https://developer.android.com/reference/kotlin/android/telecom/Call#)? | [getGenericConferenceActiveChildCall](https://developer.android.com/reference/kotlin/android/telecom/Call#getGenericConferenceActiveChildCall())`()` Returns the child [Call](https://developer.android.com/reference/kotlin/android/telecom/Call#) in a generic conference that is currently active. |
| [Call](https://developer.android.com/reference/kotlin/android/telecom/Call#)! | [getParent](https://developer.android.com/reference/kotlin/android/telecom/Call#getParent())`()` Obtains the parent of this`Call`in a conference, if any. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getRemainingPostDialSequence](https://developer.android.com/reference/kotlin/android/telecom/Call#getRemainingPostDialSequence())`()` Obtains the post-dial sequence remaining to be emitted by this`Call`, if any. |
| --- | --- |
| [Call.RttCall](https://developer.android.com/reference/kotlin/android/telecom/Call.RttCall)? | [getRttCall](https://developer.android.com/reference/kotlin/android/telecom/Call#getRttCall())`()` Returns this call's RttCall object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getState](https://developer.android.com/reference/kotlin/android/telecom/Call#getState())`()` Obtains the state of this`Call`. |
| [InCallService.VideoCall](https://developer.android.com/reference/kotlin/android/telecom/InCallService.VideoCall)! | [getVideoCall](https://developer.android.com/reference/kotlin/android/telecom/Call#getVideoCall())`()` Obtains an object that can be used to display video from this`Call`. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [handoverTo](https://developer.android.com/reference/kotlin/android/telecom/Call#handoverTo(android.telecom.PhoneAccountHandle,%20kotlin.Int,%20android.os.Bundle))`(`toHandle:` ` [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle)!`, `videoState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` Initiates a handover of this [Call](https://developer.android.com/reference/kotlin/android/telecom/Call#) to the [ConnectionService](https://developer.android.com/reference/kotlin/android/telecom/ConnectionService) identified by`toHandle`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [hold](https://developer.android.com/reference/kotlin/android/telecom/Call#hold())`()` Instructs this`Call`to go on hold. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRttActive](https://developer.android.com/reference/kotlin/android/telecom/Call#isRttActive())`()` Returns whether this call has an active RTT connection. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [mergeConference](https://developer.android.com/reference/kotlin/android/telecom/Call#mergeConference())`()` Merges the calls within this conference. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [phoneAccountSelected](https://developer.android.com/reference/kotlin/android/telecom/Call#phoneAccountSelected(android.telecom.PhoneAccountHandle,%20kotlin.Boolean))`(`accountHandle:` ` [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle)!`, `setDefault:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Notifies this`Call`that an account has been selected and to proceed with placing an outgoing call. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [playDtmfTone](https://developer.android.com/reference/kotlin/android/telecom/Call#playDtmfTone(kotlin.Char))`(`digit:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Instructs this`Call`to play a dual-tone multi-frequency signaling (DTMF) tone. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [postDialContinue](https://developer.android.com/reference/kotlin/android/telecom/Call#postDialContinue(kotlin.Boolean))`(`proceed:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Instructs this`Call`to continue playing a post-dial DTMF string. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [pullExternalCall](https://developer.android.com/reference/kotlin/android/telecom/Call#pullExternalCall())`()` Initiates a request to the [ConnectionService](https://developer.android.com/reference/kotlin/android/telecom/ConnectionService) to pull an external call to the local device. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [putExtras](https://developer.android.com/reference/kotlin/android/telecom/Call#putExtras(android.os.Bundle))`(`extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` Adds some extras to this [Call](https://developer.android.com/reference/kotlin/android/telecom/Call#). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerCallback](https://developer.android.com/reference/kotlin/android/telecom/Call#registerCallback(android.telecom.Call.Callback))`(`callback:` ` [Call.Callback](https://developer.android.com/reference/kotlin/android/telecom/Call.Callback)!`)` Registers a callback to this`Call`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerCallback](https://developer.android.com/reference/kotlin/android/telecom/Call#registerCallback(android.telecom.Call.Callback,%20android.os.Handler))`(`callback:` ` [Call.Callback](https://developer.android.com/reference/kotlin/android/telecom/Call.Callback)!`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!`)` Registers a callback to this`Call`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reject](https://developer.android.com/reference/kotlin/android/telecom/Call#reject(kotlin.Boolean,%20kotlin.String))`(`rejectWithMessage:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `textMessage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Instructs this [STATE_RINGING](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_RINGING:kotlin.Int)`Call`to reject. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reject](https://developer.android.com/reference/kotlin/android/telecom/Call#reject(kotlin.Int))`(`rejectReason:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Instructs the [ConnectionService](https://developer.android.com/reference/kotlin/android/telecom/ConnectionService) providing this [STATE_RINGING](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_RINGING:kotlin.Int) call that the user has chosen to reject the call and has indicated a reason why the call is being rejected. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeExtras](https://developer.android.com/reference/kotlin/android/telecom/Call#removeExtras(kotlin.String))`(`vararg` `keys:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Removes extras from this [Call](https://developer.android.com/reference/kotlin/android/telecom/Call#). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeExtras](https://developer.android.com/reference/kotlin/android/telecom/Call#removeExtras(kotlin.collections.MutableList))`(`keys:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Removes extras from this [Call](https://developer.android.com/reference/kotlin/android/telecom/Call#). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [respondToRttRequest](https://developer.android.com/reference/kotlin/android/telecom/Call#respondToRttRequest(kotlin.Int,%20kotlin.Boolean))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `accept:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Responds to an RTT request received via the [Callback.onRttRequest(Call, int)](https://developer.android.com/reference/kotlin/android/telecom/Call.Callback#onRttRequest(android.telecom.Call,%20kotlin.Int)))} callback. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendCallEvent](https://developer.android.com/reference/kotlin/android/telecom/Call#sendCallEvent(kotlin.String,%20android.os.Bundle))`(`event:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` Sends a`Call`event from this`Call`to the associated [Connection](https://developer.android.com/reference/kotlin/android/telecom/Connection) in the [ConnectionService](https://developer.android.com/reference/kotlin/android/telecom/ConnectionService). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendRttRequest](https://developer.android.com/reference/kotlin/android/telecom/Call#sendRttRequest())`()` Sends an RTT upgrade request to the remote end of the connection. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [splitFromConference](https://developer.android.com/reference/kotlin/android/telecom/Call#splitFromConference())`()` Instructs this`Call`to split from any conference call with which it may be connected. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopDtmfTone](https://developer.android.com/reference/kotlin/android/telecom/Call#stopDtmfTone())`()` Instructs this`Call`to stop any dual-tone multi-frequency signaling (DTMF) tone currently playing. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopRtt](https://developer.android.com/reference/kotlin/android/telecom/Call#stopRtt())`()` Terminate the RTT session on this call. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [swapConference](https://developer.android.com/reference/kotlin/android/telecom/Call#swapConference())`()` Swaps the calls within this conference. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/telecom/Call#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unhold](https://developer.android.com/reference/kotlin/android/telecom/Call#unhold())`()` Instructs this [STATE_HOLDING](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_HOLDING:kotlin.Int) call to release from hold. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterCallback](https://developer.android.com/reference/kotlin/android/telecom/Call#unregisterCallback(android.telecom.Call.Callback))`(`callback:` ` [Call.Callback](https://developer.android.com/reference/kotlin/android/telecom/Call.Callback)!`)` Unregisters a callback from this`Call`. |

## Constants

### AVAILABLE_PHONE_ACCOUNTS

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AVAILABLE_PHONE_ACCOUNTS: String
```

**Deprecated:** *Use the list from [EXTRA_SUGGESTED_PHONE_ACCOUNTS](https://developer.android.com/reference/kotlin/android/telecom/Call#EXTRA_SUGGESTED_PHONE_ACCOUNTS:kotlin.String) instead.*

The key to retrieve the optional`PhoneAccount`s Telecom can bundle with its Call extras. Used to pass the phone accounts to display on the front end to the user in order to select phone accounts to (for example) place a call. 

 Value: "selectPhoneAccountAccounts"

### EVENT_CLEAR_DIAGNOSTIC_MESSAGE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_CLEAR_DIAGNOSTIC_MESSAGE: String
```

Event reported from the telecom framework when a diagnostic message previously raised with [EVENT_DISPLAY_DIAGNOSTIC_MESSAGE](https://developer.android.com/reference/kotlin/android/telecom/Call#EVENT_DISPLAY_DIAGNOSTIC_MESSAGE:kotlin.String) has cleared and is no longer pertinent.

The [EXTRA_DIAGNOSTIC_MESSAGE_ID](https://developer.android.com/reference/kotlin/android/telecom/Call#EXTRA_DIAGNOSTIC_MESSAGE_ID:kotlin.String) indicates the diagnostic message which has been cleared.

The dialer app receives this event via [Call.Callback.onConnectionEvent(Call, String, Bundle)](https://developer.android.com/reference/kotlin/android/telecom/Call.Callback#onConnectionEvent(android.telecom.Call,%20kotlin.String,%20android.os.Bundle)). 

 Value: "android.telecom.event.CLEAR_DIAGNOSTIC_MESSAGE"

### EVENT_DISPLAY_DIAGNOSTIC_MESSAGE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_DISPLAY_DIAGNOSTIC_MESSAGE: String
```

Event reported from the Telecom stack to report an in-call diagnostic message which the dialer app may opt to display to the user. A diagnostic message is used to communicate scenarios the device has detected which may impact the quality of the ongoing call.

For example a problem with a bluetooth headset may generate a recommendation for the user to try using the speakerphone instead, or if the device detects it has entered a poor service area, the user might be warned so that they can finish their call prior to it dropping.

A diagnostic message is considered persistent in nature. When the user enters a poor service area, for example, the accompanying diagnostic message persists until they leave the area of poor service. Each message is accompanied with a [EXTRA_DIAGNOSTIC_MESSAGE_ID](https://developer.android.com/reference/kotlin/android/telecom/Call#EXTRA_DIAGNOSTIC_MESSAGE_ID:kotlin.String) which uniquely identifies the diagnostic condition being reported. The framework raises a call event of type [EVENT_CLEAR_DIAGNOSTIC_MESSAGE](https://developer.android.com/reference/kotlin/android/telecom/Call#EVENT_CLEAR_DIAGNOSTIC_MESSAGE:kotlin.String) when the condition reported has been cleared. The dialer app should display the diagnostic message until it is cleared. If multiple diagnostic messages are sent with different IDs (which have not yet been cleared) the dialer app should prioritize the most recently received message, but still provide the user with a means to review past messages.

The text of the message is found in [EXTRA_DIAGNOSTIC_MESSAGE](https://developer.android.com/reference/kotlin/android/telecom/Call#EXTRA_DIAGNOSTIC_MESSAGE:kotlin.String) in the form of a human readable [CharSequence](https://developer.android.com/reference/kotlin/java/lang/CharSequence.html#) which is intended for display in the call UX.

The telecom framework audibly notifies the user of the presence of a diagnostic message, so the dialer app needs only to concern itself with visually displaying the message.

The dialer app receives this event via [Call.Callback.onConnectionEvent(Call, String, Bundle)](https://developer.android.com/reference/kotlin/android/telecom/Call.Callback#onConnectionEvent(android.telecom.Call,%20kotlin.String,%20android.os.Bundle)). 

 Value: "android.telecom.event.DISPLAY_DIAGNOSTIC_MESSAGE"

### EXTRA_ASSERTED_DISPLAY_NAME

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_ASSERTED_DISPLAY_NAME: String
```

String value indicating the asserted display name reported via ImsCallProfile#EXTRA_ASSERTED_DISPLAY_NAME. [Connection.setExtras(Bundle)](https://developer.android.com/reference/kotlin/android/telecom/Connection#setExtras(android.os.Bundle))or [Connection.putExtras(Bundle)](https://developer.android.com/reference/kotlin/android/telecom/Connection#putExtras(android.os.Bundle))should be used to notify Telecom this extra has been set. 

 Value: "android.telecom.extra.ASSERTED_DISPLAY_NAME"

### EXTRA_DIAGNOSTIC_MESSAGE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_DIAGNOSTIC_MESSAGE: String
```

[CharSequence](https://developer.android.com/reference/kotlin/java/lang/CharSequence.html#) extra used with [EVENT_DISPLAY_DIAGNOSTIC_MESSAGE](https://developer.android.com/reference/kotlin/android/telecom/Call#EVENT_DISPLAY_DIAGNOSTIC_MESSAGE:kotlin.String). This is the diagnostic message the dialer app should display. 

 Value: "android.telecom.extra.DIAGNOSTIC_MESSAGE"

### EXTRA_DIAGNOSTIC_MESSAGE_ID

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_DIAGNOSTIC_MESSAGE_ID: String
```

Integer extra representing a message ID for a message posted via [EVENT_DISPLAY_DIAGNOSTIC_MESSAGE](https://developer.android.com/reference/kotlin/android/telecom/Call#EVENT_DISPLAY_DIAGNOSTIC_MESSAGE:kotlin.String). Used to ensure that the dialer app knows when the message in question has cleared via [EVENT_CLEAR_DIAGNOSTIC_MESSAGE](https://developer.android.com/reference/kotlin/android/telecom/Call#EVENT_CLEAR_DIAGNOSTIC_MESSAGE:kotlin.String). 

 Value: "android.telecom.extra.DIAGNOSTIC_MESSAGE_ID"

### EXTRA_IS_BUSINESS_CALL

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_IS_BUSINESS_CALL: String
```

Boolean indicating that the call is a verified business call. [Connection.setExtras(Bundle)](https://developer.android.com/reference/kotlin/android/telecom/Connection#setExtras(android.os.Bundle))or [Connection.putExtras(Bundle)](https://developer.android.com/reference/kotlin/android/telecom/Connection#putExtras(android.os.Bundle))should be used to notify Telecom this extra has been set. 

 Value: "android.telecom.extra.IS_BUSINESS_CALL"

### EXTRA_IS_SUPPRESSED_BY_DO_NOT_DISTURB

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_IS_SUPPRESSED_BY_DO_NOT_DISTURB: String
```

Extra key intended for [InCallService](https://developer.android.com/reference/kotlin/android/telecom/InCallService) s that notify the user of an incoming call. When EXTRA_IS_SUPPRESSED_BY_DO_NOT_DISTURB returns true, the [InCallService](https://developer.android.com/reference/kotlin/android/telecom/InCallService) should not interrupt the user of the incoming call because the call is being suppressed by Do Not Disturb settings. This extra will be removed from the [Call](https://developer.android.com/reference/kotlin/android/telecom/Call#) object for [InCallService](https://developer.android.com/reference/kotlin/android/telecom/InCallService) s that do not hold the [android.Manifest.permission#READ_CONTACTS](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_CONTACTS:kotlin.String) permission. 

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

Extra key used to indicate whether a [CallScreeningService](https://developer.android.com/reference/kotlin/android/telecom/CallScreeningService) has requested to silence the ringtone for a call. If the [InCallService](https://developer.android.com/reference/kotlin/android/telecom/InCallService) declares [TelecomManager.METADATA_IN_CALL_SERVICE_RINGING](https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#METADATA_IN_CALL_SERVICE_RINGING:kotlin.String) in its manifest, it should not play a ringtone for an incoming call with this extra key set. 

 Value: "android.telecom.extra.SILENT_RINGING_REQUESTED"

### EXTRA_SUGGESTED_PHONE_ACCOUNTS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_SUGGESTED_PHONE_ACCOUNTS: String
```

Key for extra used to pass along a list of [PhoneAccountSuggestion](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountSuggestion) s to the in-call UI when a call enters the [STATE_SELECT_PHONE_ACCOUNT](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_SELECT_PHONE_ACCOUNT:kotlin.Int) state. The list included here will have the same length and be in the same order as the list passed with [AVAILABLE_PHONE_ACCOUNTS](https://developer.android.com/reference/kotlin/android/telecom/Call#AVAILABLE_PHONE_ACCOUNTS:kotlin.String). 

 Value: "android.telecom.extra.SUGGESTED_PHONE_ACCOUNTS"

### REJECT_REASON_DECLINED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REJECT_REASON_DECLINED: Int
```

Reject reason used with [reject(int)](https://developer.android.com/reference/kotlin/android/telecom/Call#reject(kotlin.Int))to indicate that the user is rejecting this call because they have declined to answer it. This typically means that they are unable to answer the call at this time and would prefer it be sent to voicemail. 

 Value: 1

### REJECT_REASON_UNWANTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REJECT_REASON_UNWANTED: Int
```

Reject reason used with [reject(int)](https://developer.android.com/reference/kotlin/android/telecom/Call#reject(kotlin.Int))to indicate that the user is rejecting this call because it is an unwanted call. This allows the user to indicate that they are rejecting a call because it is likely a nuisance call. 

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

The initial state of an outgoing`Call`. Common transitions are to [STATE_DIALING](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_DIALING:kotlin.Int) state for a successful call or [STATE_DISCONNECTED](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_DISCONNECTED:kotlin.Int) if it failed. 

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

The state of a`Call`when the user has initiated a disconnection of the call, but the call has not yet been disconnected by the underlying`ConnectionService`. The next state of the call is (potentially) [STATE_DISCONNECTED](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_DISCONNECTED:kotlin.Int). 

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

A call can only be in this state if the [Details.PROPERTY_IS_EXTERNAL_CALL](https://developer.android.com/reference/kotlin/android/telecom/Call.Details#PROPERTY_IS_EXTERNAL_CALL:kotlin.Int) property and [Details.CAPABILITY_CAN_PULL_CALL](https://developer.android.com/reference/kotlin/android/telecom/Call.Details#CAPABILITY_CAN_PULL_CALL:kotlin.Int) capability are set on the call.

An [InCallService](https://developer.android.com/reference/kotlin/android/telecom/InCallService) will only see this state if it has the [TelecomManager.METADATA_INCLUDE_EXTERNAL_CALLS](https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#METADATA_INCLUDE_EXTERNAL_CALLS:kotlin.String) metadata set to`true`in its manifest. 

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

The state of an outgoing`Call`when waiting on user to select a [PhoneAccount](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount) through which to place the call. 

 Value: 8

### STATE_SIMULATED_RINGING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_SIMULATED_RINGING: Int
```

The state of a call that is being presented to the user after being in [STATE_AUDIO_PROCESSING](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_AUDIO_PROCESSING:kotlin.Int). The call is still active with the network in this case, and Telecom will hold audio focus and play a ringtone if appropriate. 

 Value: 13

## Public methods

### addConferenceParticipants

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addConferenceParticipants(participants: MutableList<Uri!>): Unit
```

Pulls participants to existing call by forming a conference call. See [Details.CAPABILITY_ADD_PARTICIPANT](https://developer.android.com/reference/kotlin/android/telecom/Call.Details#CAPABILITY_ADD_PARTICIPANT:kotlin.Int).

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `participants` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!\>:participants to be pulled to existing call. This value cannot be`null`. |

### answer

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun answer(videoState: Int): Unit
```

Instructs this [STATE_RINGING](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_RINGING:kotlin.Int)`Call`to answer.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `videoState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The video state in which to answer the call. Value is either`0`or a combination of [android.telecom.VideoProfile#STATE_AUDIO_ONLY](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_AUDIO_ONLY:kotlin.Int), [android.telecom.VideoProfile#STATE_TX_ENABLED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_TX_ENABLED:kotlin.Int), [android.telecom.VideoProfile#STATE_RX_ENABLED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_RX_ENABLED:kotlin.Int), [android.telecom.VideoProfile#STATE_BIDIRECTIONAL](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_BIDIRECTIONAL:kotlin.Int), and [android.telecom.VideoProfile#STATE_PAUSED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_PAUSED:kotlin.Int) |

### conference

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun conference(callToConferenceWith: Call!): Unit
```

Instructs this`Call`to enter a conference.

| Parameters ||
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| `callToConferenceWith` | [Call](https://developer.android.com/reference/kotlin/android/telecom/Call#)!:The other call with which to conference. |

### deflect

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun deflect(address: Uri!): Unit
```

Instructs this [STATE_RINGING](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_RINGING:kotlin.Int)`Call`to deflect.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------|
| `address` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!:The address to which the call will be deflected. |

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

*Note:* Since canned responses may be loaded from the file system, they are not guaranteed to be present when this [Call](https://developer.android.com/reference/kotlin/android/telecom/Call#) is first added to the [InCallService](https://developer.android.com/reference/kotlin/android/telecom/InCallService) via [InCallService.onCallAdded(Call)](https://developer.android.com/reference/kotlin/android/telecom/InCallService#onCallAdded(android.telecom.Call)). The callback [Call.Callback.onCannedTextResponsesLoaded(Call, List)](https://developer.android.com/reference/kotlin/android/telecom/Call.Callback#onCannedTextResponsesLoaded(android.telecom.Call,%20kotlin.collections.MutableList))will be called when/if canned responses for the call become available.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | A list of canned text message responses. |

**See Also**

- [#reject(boolean, String)](https://developer.android.com/reference/kotlin/android/telecom/Call#reject(kotlin.Boolean,%20kotlin.String)) 

### getChildren

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getChildren(): MutableList<Call!>!
```

Obtains the children of this conference`Call`, if any.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Call](https://developer.android.com/reference/kotlin/android/telecom/Call#)!>! | The children of this`Call`if this`Call`is a conference, or an empty`List`otherwise. |

### getConferenceableCalls

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConferenceableCalls(): MutableList<Call!>!
```

Returns the list of`Call`s with which this`Call`is allowed to conference.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Call](https://developer.android.com/reference/kotlin/android/telecom/Call#)!>! | The list of conferenceable`Call`s. |

### getDetails

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDetails(): Call.Details!
```

Obtains an object containing call details.

| Return ||
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Call.Details](https://developer.android.com/reference/kotlin/android/telecom/Call.Details)! | A [Details](https://developer.android.com/reference/kotlin/android/telecom/Call.Details) object. Depending on the state of the`Call`, the result may be`null`. |

### getGenericConferenceActiveChildCall

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGenericConferenceActiveChildCall(): Call?
```

Returns the child [Call](https://developer.android.com/reference/kotlin/android/telecom/Call#) in a generic conference that is currently active. A "generic conference" is the mechanism used to support two simultaneous calls on a device in CDMA networks. It is effectively equivalent to having one call active and one call on hold in GSM or IMS calls. This method returns the currently active call. In a generic conference, the network exposes the conference to us as a single call, and we switch between talking to the two participants using a CDMA flash command. Since the network exposes no additional information about the call, the only way we know which caller we're currently talking to is by keeping track of the flash commands that we've sent to the network. For calls that are not generic conferences, or when the generic conference has more than 2 children, returns`null`.

| Return ||
|-------------------------------------------------------------------------------|------------------------|
| [Call](https://developer.android.com/reference/kotlin/android/telecom/Call#)? | The active child call. |

**See Also**

- [android.telecom.Call.Details#PROPERTY_GENERIC_CONFERENCE](https://developer.android.com/reference/kotlin/android/telecom/Call.Details#PROPERTY_GENERIC_CONFERENCE:kotlin.Int) 

### getParent

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getParent(): Call!
```

Obtains the parent of this`Call`in a conference, if any.

| Return ||
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Call](https://developer.android.com/reference/kotlin/android/telecom/Call#)! | The parent`Call`, or`null`if this`Call`is not a child of any conference`Call`s. |

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

Returns this call's RttCall object. The [RttCall](https://developer.android.com/reference/kotlin/android/telecom/Call.RttCall) instance is used to send and receive RTT text data, as well as to change the RTT mode.

| Return ||
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [Call.RttCall](https://developer.android.com/reference/kotlin/android/telecom/Call.RttCall)? | A [Call.RttCall](https://developer.android.com/reference/kotlin/android/telecom/Call.RttCall).`null`if there is no active RTT connection. |

### getState

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getState(): Int
```

**Deprecated:** *The call state is available via [Call.Details.getState()](https://developer.android.com/reference/kotlin/android/telecom/Call.Details#getState()).*

Obtains the state of this`Call`.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The call state. Value is [android.telecom.Call#STATE_NEW](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_NEW:kotlin.Int), [android.telecom.Call#STATE_DIALING](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_DIALING:kotlin.Int), [android.telecom.Call#STATE_RINGING](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_RINGING:kotlin.Int), [android.telecom.Call#STATE_HOLDING](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_HOLDING:kotlin.Int), [android.telecom.Call#STATE_ACTIVE](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_ACTIVE:kotlin.Int), [android.telecom.Call#STATE_DISCONNECTED](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_DISCONNECTED:kotlin.Int), [android.telecom.Call#STATE_SELECT_PHONE_ACCOUNT](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_SELECT_PHONE_ACCOUNT:kotlin.Int), [android.telecom.Call#STATE_CONNECTING](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_CONNECTING:kotlin.Int), [android.telecom.Call#STATE_DISCONNECTING](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_DISCONNECTING:kotlin.Int), [android.telecom.Call#STATE_PULLING_CALL](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_PULLING_CALL:kotlin.Int), [android.telecom.Call#STATE_AUDIO_PROCESSING](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_AUDIO_PROCESSING:kotlin.Int), or [android.telecom.Call#STATE_SIMULATED_RINGING](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_SIMULATED_RINGING:kotlin.Int) |

### getVideoCall

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVideoCall(): InCallService.VideoCall!
```

Obtains an object that can be used to display video from this`Call`.

| Return ||
|--------------------------------------------------------------------------------------------------------------------|---------------------|
| [InCallService.VideoCall](https://developer.android.com/reference/kotlin/android/telecom/InCallService.VideoCall)! | An`Call.VideoCall`. |

### handoverTo

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun handoverTo(
    toHandle: PhoneAccountHandle!, 
    videoState: Int, 
    extras: Bundle!
): Unit
```

Initiates a handover of this [Call](https://developer.android.com/reference/kotlin/android/telecom/Call#) to the [ConnectionService](https://developer.android.com/reference/kotlin/android/telecom/ConnectionService) identified by`toHandle`. The videoState specified indicates the desired video state after the handover.

A call handover is the process where an ongoing call is transferred from one app (i.e. [ConnectionService](https://developer.android.com/reference/kotlin/android/telecom/ConnectionService) to another app. The user could, for example, choose to continue a mobile network call in a video calling app. The mobile network call via the Telephony stack is referred to as the source of the handover, and the video calling app is referred to as the destination.

When considering a handover scenario the device this method is called on is considered the*initiating* device (since the user initiates the handover from this device), and the other device is considered the*receiving*device.

When this method is called on the*initiating* device, the Telecom framework will bind to the [ConnectionService](https://developer.android.com/reference/kotlin/android/telecom/ConnectionService) defined by the`toHandle` [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle) and invoke [ConnectionService.onCreateOutgoingHandoverConnection(PhoneAccountHandle,](https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateOutgoingHandoverConnection(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest))to inform the destination app that a request has been made to handover a call to it. The app returns an instance of [Connection](https://developer.android.com/reference/kotlin/android/telecom/Connection) to represent the handover call At this point the app should display UI to indicate to the user that a call handover is in process.

The destination app is responsible for communicating the handover request from the*initiating* device to the*receiving*device.

When the app on the*receiving* device receives the handover request, it calls [TelecomManager.acceptHandover(Uri, int, PhoneAccountHandle)](https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#acceptHandover(android.net.Uri,%20kotlin.Int,%20android.telecom.PhoneAccountHandle))to continue the handover process from the*initiating* device to the*receiving* device. At this point the destination app on the*receiving*device should show UI to allow the user to choose whether they want to continue their call in the destination app.

When the destination app on the*receiving* device calls [TelecomManager.acceptHandover(Uri, int, PhoneAccountHandle)](https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#acceptHandover(android.net.Uri,%20kotlin.Int,%20android.telecom.PhoneAccountHandle)), Telecom will bind to its [ConnectionService](https://developer.android.com/reference/kotlin/android/telecom/ConnectionService) and call [ConnectionService.onCreateIncomingHandoverConnection(PhoneAccountHandle,](https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateIncomingHandoverConnection(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest))to inform it of the handover request. The app returns an instance of [Connection](https://developer.android.com/reference/kotlin/android/telecom/Connection) to represent the handover call.

If the user of the*receiving* device accepts the handover, the app calls [Connection.setActive()](https://developer.android.com/reference/kotlin/android/telecom/Connection#setActive())to complete the handover process; Telecom will disconnect the original call. If the user rejects the handover, the app calls [Connection.setDisconnected(DisconnectCause)](https://developer.android.com/reference/kotlin/android/telecom/Connection#setDisconnected(android.telecom.DisconnectCause))and specifies a [DisconnectCause](https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause) of [DisconnectCause.CANCELED](https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#CANCELED:kotlin.Int) to indicate that the handover has been cancelled.

Telecom will only allow handovers from [PhoneAccount](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount) s which declare [PhoneAccount.EXTRA_SUPPORTS_HANDOVER_FROM](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#EXTRA_SUPPORTS_HANDOVER_FROM:kotlin.String). Similarly, the [PhoneAccount](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount) specified by`toHandle`must declare [PhoneAccount.EXTRA_SUPPORTS_HANDOVER_TO](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#EXTRA_SUPPORTS_HANDOVER_TO:kotlin.String).

Errors in the handover process are reported to the [InCallService](https://developer.android.com/reference/kotlin/android/telecom/InCallService) via [Callback.onHandoverFailed(Call, int)](https://developer.android.com/reference/kotlin/android/telecom/Call.Callback#onHandoverFailed(android.telecom.Call,%20kotlin.Int)). Errors in the handover process are reported to the involved [ConnectionService](https://developer.android.com/reference/kotlin/android/telecom/ConnectionService) s via [ConnectionService.onHandoverFailed(ConnectionRequest, int)](https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onHandoverFailed(android.telecom.ConnectionRequest,%20kotlin.Int)).

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `toHandle` | [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle)!: [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle) of the [ConnectionService](https://developer.android.com/reference/kotlin/android/telecom/ConnectionService) to handover this call to. |
| `videoState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Indicates the video state desired after the handover (see the`STATE_*`constants defined in [VideoProfile](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile)). Value is either`0`or a combination of [android.telecom.VideoProfile#STATE_AUDIO_ONLY](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_AUDIO_ONLY:kotlin.Int), [android.telecom.VideoProfile#STATE_TX_ENABLED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_TX_ENABLED:kotlin.Int), [android.telecom.VideoProfile#STATE_RX_ENABLED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_RX_ENABLED:kotlin.Int), [android.telecom.VideoProfile#STATE_BIDIRECTIONAL](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_BIDIRECTIONAL:kotlin.Int), and [android.telecom.VideoProfile#STATE_PAUSED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_PAUSED:kotlin.Int) |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:Bundle containing extra information to be passed to the [ConnectionService](https://developer.android.com/reference/kotlin/android/telecom/ConnectionService) |
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

Merges the calls within this conference. See [Details.CAPABILITY_MERGE_CONFERENCE](https://developer.android.com/reference/kotlin/android/telecom/Call.Details#CAPABILITY_MERGE_CONFERENCE:kotlin.Int). 

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

You must ensure that any call to [playDtmfTone(char)](https://developer.android.com/reference/kotlin/android/telecom/Call#playDtmfTone(kotlin.Char))is followed by a matching call to [stopDtmfTone()](https://developer.android.com/reference/kotlin/android/telecom/Call#stopDtmfTone())and that each tone is stopped before a new one is started. The play and stop commands are relayed to the underlying [android.telecom.ConnectionService](https://developer.android.com/reference/kotlin/android/telecom/ConnectionService) as executed; implementations may not correctly handle out of order commands.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `digit` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):A character representing the DTMF digit for which to play the tone. This value must be one of`'0'`through`'9'`,`'*'`or`'#'`. |

### postDialContinue

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun postDialContinue(proceed: Boolean): Unit
```

Instructs this`Call`to continue playing a post-dial DTMF string. A post-dial DTMF string is a string of digits entered after a phone number, when dialed, that are immediately sent as DTMF tones to the recipient as soon as the connection is made. If the DTMF string contains a [TelecomManager.DTMF_CHARACTER_PAUSE](https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#DTMF_CHARACTER_PAUSE:kotlin.Char) symbol, this`Call`will temporarily pause playing the tones for a pre-defined period of time. If the DTMF string contains a [TelecomManager.DTMF_CHARACTER_WAIT](https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#DTMF_CHARACTER_WAIT:kotlin.Char) symbol, this`Call`will pause playing the tones and notify callbacks via [Callback.onPostDialWait(Call, String)](https://developer.android.com/reference/kotlin/android/telecom/Call.Callback#onPostDialWait(android.telecom.Call,%20kotlin.String)). At this point, the in-call app should display to the user an indication of this state and an affordance to continue the postdial sequence. When the user decides to continue the postdial sequence, the in-call app should invoke the [postDialContinue(boolean)](https://developer.android.com/reference/kotlin/android/telecom/Call#postDialContinue(kotlin.Boolean))method.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `proceed` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether or not to continue with the post-dial sequence. |

### pullExternalCall

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun pullExternalCall(): Unit
```

Initiates a request to the [ConnectionService](https://developer.android.com/reference/kotlin/android/telecom/ConnectionService) to pull an external call to the local device.

Calls to this method are ignored if the call does not have the [Call.Details.PROPERTY_IS_EXTERNAL_CALL](https://developer.android.com/reference/kotlin/android/telecom/Call.Details#PROPERTY_IS_EXTERNAL_CALL:kotlin.Int) property set.

An [InCallService](https://developer.android.com/reference/kotlin/android/telecom/InCallService) will only see calls which support this method if it has the [TelecomManager.METADATA_INCLUDE_EXTERNAL_CALLS](https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#METADATA_INCLUDE_EXTERNAL_CALLS:kotlin.String) metadata set to`true`in its manifest. 

### putExtras

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun putExtras(extras: Bundle!): Unit
```

Adds some extras to this [Call](https://developer.android.com/reference/kotlin/android/telecom/Call#). Existing keys are replaced and new ones are added.

No assumptions should be made as to how an In-Call UI or service will handle these extras. Keys should be fully qualified (e.g., com.example.MY_EXTRA) to avoid conflicts.

Extras added using this method will be made available to the [ConnectionService](https://developer.android.com/reference/kotlin/android/telecom/ConnectionService) associated with this [Call](https://developer.android.com/reference/kotlin/android/telecom/Call#) and notified via [Connection.onExtrasChanged(Bundle)](https://developer.android.com/reference/kotlin/android/telecom/Connection#onExtrasChanged(android.os.Bundle)).

Extras added using this method will also be available to other running [InCallService](https://developer.android.com/reference/kotlin/android/telecom/InCallService) s and notified via [Call.Callback.onDetailsChanged(Call, Details)](https://developer.android.com/reference/kotlin/android/telecom/Call.Callback#onDetailsChanged(android.telecom.Call,%20android.telecom.Call.Details)). The extras can be accessed via [Details.getExtras()](https://developer.android.com/reference/kotlin/android/telecom/Call.Details#getExtras()).

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------|
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:The extras to add. |

### registerCallback

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun registerCallback(callback: Call.Callback!): Unit
```

Registers a callback to this`Call`.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `callback` | [Call.Callback](https://developer.android.com/reference/kotlin/android/telecom/Call.Callback)!:A`Callback`. |

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
| `callback` | [Call.Callback](https://developer.android.com/reference/kotlin/android/telecom/Call.Callback)!:A`Callback`. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!:A handler which command and status changes will be delivered to. |

### reject

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun reject(
    rejectWithMessage: Boolean, 
    textMessage: String!
): Unit
```

Instructs this [STATE_RINGING](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_RINGING:kotlin.Int)`Call`to reject.

| Parameters ||
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `rejectWithMessage` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether to reject with a text message. |
| `textMessage` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:An optional text message with which to respond. |

### reject

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun reject(rejectReason: Int): Unit
```

Instructs the [ConnectionService](https://developer.android.com/reference/kotlin/android/telecom/ConnectionService) providing this [STATE_RINGING](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_RINGING:kotlin.Int) call that the user has chosen to reject the call and has indicated a reason why the call is being rejected.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `rejectReason` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the reason the call is being rejected. Value is [android.telecom.Call#REJECT_REASON_DECLINED](https://developer.android.com/reference/kotlin/android/telecom/Call#REJECT_REASON_DECLINED:kotlin.Int), or [android.telecom.Call#REJECT_REASON_UNWANTED](https://developer.android.com/reference/kotlin/android/telecom/Call#REJECT_REASON_UNWANTED:kotlin.Int) |

### removeExtras

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeExtras(vararg keys: String!): Unit
```

Removes extras from this [Call](https://developer.android.com/reference/kotlin/android/telecom/Call#).

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------|
| `keys` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The keys of the extras to remove. |

### removeExtras

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeExtras(keys: MutableList<String!>!): Unit
```

Removes extras from this [Call](https://developer.android.com/reference/kotlin/android/telecom/Call#).

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

Responds to an RTT request received via the [Callback.onRttRequest(Call, int)](https://developer.android.com/reference/kotlin/android/telecom/Call.Callback#onRttRequest(android.telecom.Call,%20kotlin.Int)))} callback. The ID used here should be the same as the ID that was received via the callback.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The request ID received via [Callback.onRttRequest(Call, int)](https://developer.android.com/reference/kotlin/android/telecom/Call.Callback#onRttRequest(android.telecom.Call,%20kotlin.Int)) |
| `accept` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if the RTT request should be accepted,`false`otherwise. |

### sendCallEvent

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun sendCallEvent(
    event: String!, 
    extras: Bundle!
): Unit
```

Sends a`Call`event from this`Call`to the associated [Connection](https://developer.android.com/reference/kotlin/android/telecom/Connection) in the [ConnectionService](https://developer.android.com/reference/kotlin/android/telecom/ConnectionService).

Call events are used to communicate point in time information from an [InCallService](https://developer.android.com/reference/kotlin/android/telecom/InCallService) to a [ConnectionService](https://developer.android.com/reference/kotlin/android/telecom/ConnectionService). A [ConnectionService](https://developer.android.com/reference/kotlin/android/telecom/ConnectionService) implementation could define events which enable the [InCallService](https://developer.android.com/reference/kotlin/android/telecom/InCallService), for example, toggle a unique feature of the [ConnectionService](https://developer.android.com/reference/kotlin/android/telecom/ConnectionService).

A [ConnectionService](https://developer.android.com/reference/kotlin/android/telecom/ConnectionService) can communicate to the [InCallService](https://developer.android.com/reference/kotlin/android/telecom/InCallService) using [Connection.sendConnectionEvent(String, Bundle)](https://developer.android.com/reference/kotlin/android/telecom/Connection#sendConnectionEvent(kotlin.String,%20android.os.Bundle)).

Events are exposed to [ConnectionService](https://developer.android.com/reference/kotlin/android/telecom/ConnectionService) implementations via [android.telecom.Connection#onCallEvent(String, Bundle)](https://developer.android.com/reference/kotlin/android/telecom/Connection#onCallEvent(kotlin.String,%20android.os.Bundle)).

No assumptions should be made as to how a [ConnectionService](https://developer.android.com/reference/kotlin/android/telecom/ConnectionService) will handle these events. The [InCallService](https://developer.android.com/reference/kotlin/android/telecom/InCallService) must assume that the [ConnectionService](https://developer.android.com/reference/kotlin/android/telecom/ConnectionService) could chose to ignore some events altogether.

Events should be fully qualified (e.g.,`com.example.event.MY_EVENT`) to avoid conflicts between [InCallService](https://developer.android.com/reference/kotlin/android/telecom/InCallService) implementations. Further, [InCallService](https://developer.android.com/reference/kotlin/android/telecom/InCallService) implementations shall not re-purpose events in the`android.*`namespace, nor shall they define their own event types in this namespace. When defining a custom event type, ensure the contents of the extras [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) is clearly defined. Extra keys for this bundle should be named similar to the event type (e.g.`com.example.extra.MY_EXTRA`).

When defining events and the associated extras, it is important to keep their behavior consistent when the associated [InCallService](https://developer.android.com/reference/kotlin/android/telecom/InCallService) is updated. Support for deprecated events/extras should me maintained to ensure backwards compatibility with older [ConnectionService](https://developer.android.com/reference/kotlin/android/telecom/ConnectionService) implementations which were built to support the older behavior.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The connection event. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:Bundle containing extra information associated with the event. |

### sendRttRequest

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun sendRttRequest(): Unit
```

Sends an RTT upgrade request to the remote end of the connection. Success is not guaranteed, and notification of success will be via the [Callback.onRttStatusChanged(Call, boolean, RttCall)](https://developer.android.com/reference/kotlin/android/telecom/Call.Callback#onRttStatusChanged(android.telecom.Call,%20kotlin.Boolean,%20android.telecom.Call.RttCall))callback. 

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

Instructs this`Call`to stop any dual-tone multi-frequency signaling (DTMF) tone currently playing. DTMF tones are played by calling [playDtmfTone(char)](https://developer.android.com/reference/kotlin/android/telecom/Call#playDtmfTone(kotlin.Char)). If no DTMF tone is currently playing, this method will do nothing. 

### stopRtt

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun stopRtt(): Unit
```

Terminate the RTT session on this call. The resulting state change will be notified via the [Callback.onRttStatusChanged(Call, boolean, RttCall)](https://developer.android.com/reference/kotlin/android/telecom/Call.Callback#onRttStatusChanged(android.telecom.Call,%20kotlin.Boolean,%20android.telecom.Call.RttCall))callback. 

### swapConference

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun swapConference(): Unit
```

Swaps the calls within this conference. See [Details.CAPABILITY_SWAP_CONFERENCE](https://developer.android.com/reference/kotlin/android/telecom/Call.Details#CAPABILITY_SWAP_CONFERENCE:kotlin.Int). 

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

Instructs this [STATE_HOLDING](https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_HOLDING:kotlin.Int) call to release from hold. 

### unregisterCallback

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unregisterCallback(callback: Call.Callback!): Unit
```

Unregisters a callback from this`Call`.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `callback` | [Call.Callback](https://developer.android.com/reference/kotlin/android/telecom/Call.Callback)!:A`Callback`. |
