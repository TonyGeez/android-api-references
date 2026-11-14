Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Conference

```
abstract class Conference : Conferenceable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.telecom.Conferenceable](https://developer.android.com/reference/kotlin/android/telecom/Conferenceable) ||
| | ↳ | [android.telecom.Conference](https://developer.android.com/reference/kotlin/android/telecom/Conference#) |

Represents a conference call which can contain any number of `https://developer.android.com/reference/kotlin/android/telecom/Connection` objects.

## Summary

| Constants ||
|---|---|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#CONNECT_TIME_NOT_SPECIFIED:kotlin.Long` Used to indicate that the conference connection time is not specified. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/Conference#Conference(android.telecom.PhoneAccountHandle)(phoneAccount: https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle!)` Constructs a new Conference with a mandatory `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle` |

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#addConnection(android.telecom.Connection)(connection: https://developer.android.com/reference/kotlin/android/telecom/Connection!)` Adds the specified connection as a child of this conference. |
| open static [Conference](https://developer.android.com/reference/kotlin/android/telecom/Conference#) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#createFailedConference(android.telecom.DisconnectCause,%20android.telecom.PhoneAccountHandle)(disconnectCause: https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause, phoneAccount: https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle)` Return a `Conference` which represents a failed conference attempt. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#destroy()()` Tears down the conference object and any of its current connections. |
| --- | --- |
| [CallAudioState](https://developer.android.com/reference/kotlin/android/telecom/CallAudioState)! | `https://developer.android.com/reference/kotlin/android/telecom/Conference#getCallAudioState()()` <br /> |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Connection](https://developer.android.com/reference/kotlin/android/telecom/Connection)!\>! | `https://developer.android.com/reference/kotlin/android/telecom/Conference#getConferenceableConnections()()` Returns the connections with which this connection can be conferenced. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Conferenceable](https://developer.android.com/reference/kotlin/android/telecom/Conferenceable)!\> | `https://developer.android.com/reference/kotlin/android/telecom/Conference#getConferenceables()()` Returns the `https://developer.android.com/reference/kotlin/android/telecom/Connection`s or `https://developer.android.com/reference/kotlin/android/telecom/Conference#`s with which this `https://developer.android.com/reference/kotlin/android/telecom/Conference#` can be merged / conferenced. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#getConnectionCapabilities()()` Returns the capabilities of the conference. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#getConnectionProperties()()` Returns the properties of the conference. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#getConnectionStartElapsedRealtimeMillis()()` Retrieves the connection start time of the `https://developer.android.com/reference/kotlin/android/telecom/Conference#`, if specified. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#getConnectionTime()()` Retrieves the connection start time of the `Conference`, if specified. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Connection](https://developer.android.com/reference/kotlin/android/telecom/Connection)!\>! | `https://developer.android.com/reference/kotlin/android/telecom/Conference#getConnections()()` Returns the list of connections currently associated with the conference call. |
| [CallEndpoint](https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#getCurrentCallEndpoint()()` Obtains the current CallEndpoint. |
| --- | --- |
| [DisconnectCause](https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause)! | `https://developer.android.com/reference/kotlin/android/telecom/Conference#getDisconnectCause()()` <br /> |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | `https://developer.android.com/reference/kotlin/android/telecom/Conference#getExtras()()` Returns the extras associated with this conference. |
| [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle)! | `https://developer.android.com/reference/kotlin/android/telecom/Conference#getPhoneAccountHandle()()` Returns the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle` the conference call is being placed through. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#getState()()` Gets the state of the conference call. |
| [StatusHints](https://developer.android.com/reference/kotlin/android/telecom/StatusHints)! | `https://developer.android.com/reference/kotlin/android/telecom/Conference#getStatusHints()()` <br /> |
| open [Connection.VideoProvider](https://developer.android.com/reference/kotlin/android/telecom/Connection.VideoProvider)! | `https://developer.android.com/reference/kotlin/android/telecom/Conference#getVideoProvider()()` Returns VideoProvider of the primary call. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#getVideoState()()` Returns video state of the primary call. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#isRingbackRequested()()` Returns whether this conference is requesting that the system play a ringback tone on its behalf. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#notifyConferenceMergeFailed()()` Called by a `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` to notify Telecom that a `https://developer.android.com/reference/kotlin/android/telecom/Conference#onMerge()` request failed. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#onAddConferenceParticipants(kotlin.collections.MutableList)(participants: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>)` Notifies the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` of a request to add a new participants to the conference call |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#onAnswer(kotlin.Int)(videoState: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Notifies this Conference, which is in `STATE_RINGING`, of a request to accept. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#onAvailableCallEndpointsChanged(kotlin.collections.MutableList)(availableEndpoints: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint!>)` Notifies the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` that the available call endpoints have been changed. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#onCallAudioStateChanged(android.telecom.CallAudioState)(state: https://developer.android.com/reference/kotlin/android/telecom/CallAudioState!)` Notifies the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` that the `https://developer.android.com/reference/kotlin/android/telecom/Conference#getCallAudioState()` property has a new value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#onCallEndpointChanged(android.telecom.CallEndpoint)(callEndpoint: https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint)` Notifies the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` that the audio endpoint has been changed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#onConnectionAdded(android.telecom.Connection)(connection: https://developer.android.com/reference/kotlin/android/telecom/Connection!)` Notifies the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` that a `https://developer.android.com/reference/kotlin/android/telecom/Connection` has been added to it. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#onDisconnect()()` Notifies the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` when the Conference and all it's `https://developer.android.com/reference/kotlin/android/telecom/Connection`s should be disconnected. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#onExtrasChanged(android.os.Bundle)(extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` Notifies this `https://developer.android.com/reference/kotlin/android/telecom/Conference#` of a change to the extras made outside the `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#onHold()()` Notifies the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` when it should be put on hold. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#onMerge()()` Notifies the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` when the child calls should be merged. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#onMerge(android.telecom.Conference)(conference: https://developer.android.com/reference/kotlin/android/telecom/Conference#)` Notifies the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` when the specified `https://developer.android.com/reference/kotlin/android/telecom/Conference#` should be merged with the conference call. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#onMerge(android.telecom.Connection)(connection: https://developer.android.com/reference/kotlin/android/telecom/Connection!)` Notifies the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` when the specified `https://developer.android.com/reference/kotlin/android/telecom/Connection` should merged with the conference call. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#onMuteStateChanged(kotlin.Boolean)(isMuted: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Notifies the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` that its audio mute state has been changed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#onPlayDtmfTone(kotlin.Char)(c: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Notifies the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` of a request to play a DTMF tone. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#onReject()()` Notifies this Conference, which is in `STATE_RINGING`, of a request to reject. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#onSeparate(android.telecom.Connection)(connection: https://developer.android.com/reference/kotlin/android/telecom/Connection!)` Notifies the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` when the specified `https://developer.android.com/reference/kotlin/android/telecom/Connection` should be separated from the conference call. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#onStopDtmfTone()()` Notifies the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` of a request to stop any currently playing DTMF tones. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#onSwap()()` Notifies the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` when the child calls should be swapped. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#onUnhold()()` Notifies the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` when it should be moved from a held to active state. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#putExtras(android.os.Bundle)(extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#)` Adds some extras to this `https://developer.android.com/reference/kotlin/android/telecom/Conference#`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#removeConnection(android.telecom.Connection)(connection: https://developer.android.com/reference/kotlin/android/telecom/Connection!)` Removes the specified connection as a child of this conference. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#removeExtras(kotlin.String)(vararg keys: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Removes extras from this `https://developer.android.com/reference/kotlin/android/telecom/Conference#`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#removeExtras(kotlin.collections.MutableList)(keys: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Removes extras from this `https://developer.android.com/reference/kotlin/android/telecom/Conference#`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#sendConferenceEvent(kotlin.String,%20android.os.Bundle)(event: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Sends an event associated with this `https://developer.android.com/reference/kotlin/android/telecom/Conference#` with associated event extras to the `https://developer.android.com/reference/kotlin/android/telecom/InCallService`. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#setActive()()` Sets state to be active. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#setConferenceableConnections(kotlin.collections.MutableList)(conferenceableConnections: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/telecom/Connection!>!)` Sets the connections with which this connection can be conferenced. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#setConferenceables(kotlin.collections.MutableList)(conferenceables: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/telecom/Conferenceable!>)` Sets a list of connections or conferences with which this conference can be conferenced. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#setConnectionCapabilities(kotlin.Int)(connectionCapabilities: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the capabilities of a conference. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#setConnectionProperties(kotlin.Int)(connectionProperties: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the properties of a conference. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#setConnectionStartElapsedRealTime(kotlin.Long)(connectionStartElapsedRealTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Sets the start time of the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` which is the basis for the determining the duration of the `https://developer.android.com/reference/kotlin/android/telecom/Conference#`. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#setConnectionStartElapsedRealtimeMillis(kotlin.Long)(connectionStartElapsedRealTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Sets the start time of the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` which is the basis for the determining the duration of the `https://developer.android.com/reference/kotlin/android/telecom/Conference#`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#setConnectionTime(kotlin.Long)(connectionTimeMillis: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Sets the connection start time of the `Conference`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#setDialing()()` Sets state to be dialing. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#setDisconnected(android.telecom.DisconnectCause)(disconnectCause: https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause!)` Sets state to disconnected. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#setExtras(android.os.Bundle)(extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Replaces all the extras associated with this `Conference`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#setOnHold()()` Sets state to be on hold. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#setRingbackRequested(kotlin.Boolean)(ringback: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Requests that the framework play a ringback tone. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#setRinging()()` Sets state to be ringing. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#setStatusHints(android.telecom.StatusHints)(statusHints: https://developer.android.com/reference/kotlin/android/telecom/StatusHints!)` Sets the label and icon status to display in the InCall UI. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#setVideoProvider(android.telecom.Connection,%20android.telecom.Connection.VideoProvider)(c: https://developer.android.com/reference/kotlin/android/telecom/Connection!, videoProvider: https://developer.android.com/reference/kotlin/android/telecom/Connection.VideoProvider!)` Sets the video connection provider. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#setVideoState(android.telecom.Connection,%20kotlin.Int)(c: https://developer.android.com/reference/kotlin/android/telecom/Connection!, videoState: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the video state for the conference. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Conference#toString()()` Returns a string representation of the object. |
| --- | --- |

## Constants

### CONNECT_TIME_NOT_SPECIFIED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONNECT_TIME_NOT_SPECIFIED: Long
```

Used to indicate that the conference connection time is not specified. If not specified, Telecom will set the connect time.

 Value: 0L

## Public constructors

### Conference

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Conference(phoneAccount: PhoneAccountHandle!)
```

Constructs a new Conference with a mandatory `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle`

| Parameters ||
|---|---|
| `phoneAccount` | [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle)!: The `PhoneAccountHandle` associated with the conference. |

## Public methods

### addConnection

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addConnection(connection: Connection!): Boolean
```

Adds the specified connection as a child of this conference.

| Parameters ||
|---|---|
| `connection` | [Connection](https://developer.android.com/reference/kotlin/android/telecom/Connection)!: The connection to add. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the connection was successfully added. |

### createFailedConference

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createFailedConference(
    disconnectCause: DisconnectCause, 
    phoneAccount: PhoneAccountHandle
): Conference
```

Return a `Conference` which represents a failed conference attempt. The returned `Conference` will have a `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause` and as specified, and a `https://developer.android.com/reference/kotlin/android/telecom/Conference#getState()` of `STATE_DISCONNECTED`.

The returned `Conference` can be assumed to `https://developer.android.com/reference/kotlin/android/telecom/Conference#destroy()` itself when appropriate, so users of this method need not maintain a reference to its return value to destroy it.

| Parameters ||
|---|---|
| `disconnectCause` | [DisconnectCause](https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause): The disconnect cause, (see android.telecomm.DisconnectCause). This value cannot be `null`. |
| `phoneAccount` | [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle): This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/Conference#` | A `Conference` which indicates failure. This value cannot be `null`. |

### destroy

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun destroy(): Unit
```

Tears down the conference object and any of its current connections.

### getCallAudioState

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCallAudioState(): CallAudioState!
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/telecom/Conference#getCurrentCallEndpoint()`, `https://developer.android.com/reference/kotlin/android/telecom/Conference#onAvailableCallEndpointsChanged(kotlin.collections.MutableList)` and `https://developer.android.com/reference/kotlin/android/telecom/Conference#onMuteStateChanged(kotlin.Boolean)` instead.*

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState!` | The audio state of the conference, describing how its audio is currently being routed by the system. This is `null` if this Conference does not directly know about its audio state. |

### getConferenceableConnections

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getConferenceableConnections(): MutableList<Connection!>!
```

Returns the connections with which this connection can be conferenced.

### getConferenceables

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getConferenceables(): MutableList<Conferenceable!>
```

Returns the `https://developer.android.com/reference/kotlin/android/telecom/Connection`s or `https://developer.android.com/reference/kotlin/android/telecom/Conference#`s with which this `https://developer.android.com/reference/kotlin/android/telecom/Conference#` can be merged / conferenced.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/telecom/Conferenceable!>` | This value cannot be `null`. |

### getConnectionCapabilities

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getConnectionCapabilities(): Int
```

Returns the capabilities of the conference. See `CAPABILITY_*` constants in class `https://developer.android.com/reference/kotlin/android/telecom/Connection` for valid values.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A bitmask of the capabilities of the conference call. |

### getConnectionProperties

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getConnectionProperties(): Int
```

Returns the properties of the conference. See `PROPERTY_*` constants in class `https://developer.android.com/reference/kotlin/android/telecom/Connection` for valid values.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A bitmask of the properties of the conference call. |

### getConnectionStartElapsedRealtimeMillis

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getConnectionStartElapsedRealtimeMillis(): Long
```

Retrieves the connection start time of the `https://developer.android.com/reference/kotlin/android/telecom/Conference#`, if specified. A value of `https://developer.android.com/reference/kotlin/android/telecom/Conference#CONNECT_TIME_NOT_SPECIFIED:kotlin.Long` indicates that Telecom should determine the start time of the conference.

This is based on the value of `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#elapsedRealtime()` to ensure that it is not impacted by wall clock changes (user initiated, network initiated, time zone change, etc).

Note: This is only exposed for use by the Telephony framework which needs it to copy conference start times among conference participants. It is exposed as a system API since it has no general use other than to the Telephony framework. 
Value is a non-negative timestamp in the `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#elapsedRealtime()` time base.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | The elapsed time at which the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` was connected. Value is a non-negative timestamp in the `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#elapsedRealtime()` time base. |

### getConnectionTime

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getConnectionTime(): Long
```

Retrieves the connection start time of the `Conference`, if specified. A value of `https://developer.android.com/reference/kotlin/android/telecom/Conference#CONNECT_TIME_NOT_SPECIFIED:kotlin.Long` indicates that Telecom should determine the start time of the conference.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | The time at which the `Conference` was connected. Value is 0 or greater |

### getConnections

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getConnections(): MutableList<Connection!>!
```

Returns the list of connections currently associated with the conference call.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/telecom/Connection!>!` | A list of `Connection` objects which represent the children of the conference. |

### getCurrentCallEndpoint

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCurrentCallEndpoint(): CallEndpoint
```

Obtains the current CallEndpoint.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint` | An object encapsulating the CallEndpoint. This value cannot be `null`. |

### getDisconnectCause

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDisconnectCause(): DisconnectCause!
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause!` | The `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause` for this connection. |

### getExtras

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getExtras(): Bundle!
```

Returns the extras associated with this conference.

Extras should be updated using `https://developer.android.com/reference/kotlin/android/telecom/Conference#putExtras(android.os.Bundle)` and `https://developer.android.com/reference/kotlin/android/telecom/Conference#removeExtras(kotlin.collections.MutableList)`.

Telecom or an `https://developer.android.com/reference/kotlin/android/telecom/InCallService` can also update the extras via `https://developer.android.com/reference/kotlin/android/telecom/Call#putExtras(android.os.Bundle)`, and `https://developer.android.com/reference/kotlin/android/telecom/Call#removeExtras(kotlin.collections.MutableList)`.

The conference is notified of changes to the extras made by Telecom or an `https://developer.android.com/reference/kotlin/android/telecom/InCallService` by `https://developer.android.com/reference/kotlin/android/telecom/Conference#onExtrasChanged(android.os.Bundle)`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` | The extras associated with this connection. |

### getPhoneAccountHandle

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPhoneAccountHandle(): PhoneAccountHandle!
```

Returns the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle` the conference call is being placed through.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle!` | A `PhoneAccountHandle` object representing the PhoneAccount of the conference. |

### getState

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getState(): Int
```

Gets the state of the conference call. See `https://developer.android.com/reference/kotlin/android/telecom/Connection` for valid values.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A constant representing the state the conference call is currently in. |

### getStatusHints

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getStatusHints(): StatusHints!
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/StatusHints!` | The status hints for this conference. |

### getVideoProvider

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getVideoProvider(): Connection.VideoProvider!
```

Returns VideoProvider of the primary call. This can be null.

### getVideoState

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getVideoState(): Int
```

Returns video state of the primary call.

### isRingbackRequested

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isRingbackRequested(): Boolean
```

Returns whether this conference is requesting that the system play a ringback tone on its behalf. A ringback tone may be played when an outgoing conference is in the process of connecting to give the user an audible indication of that process.

### notifyConferenceMergeFailed

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun notifyConferenceMergeFailed(): Unit
```

Called by a `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` to notify Telecom that a `https://developer.android.com/reference/kotlin/android/telecom/Conference#onMerge()` request failed.

### onAddConferenceParticipants

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onAddConferenceParticipants(participants: MutableList<Uri!>): Unit
```

Notifies the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` of a request to add a new participants to the conference call

| Parameters ||
|---|---|
| `participants` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!\>: that will be added to this conference call. This value cannot be `null`. |

### onAnswer

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onAnswer(videoState: Int): Unit
```

Notifies this Conference, which is in `STATE_RINGING`, of a request to accept. For managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`s, this will be called when the user answers a call via the default dialer's `https://developer.android.com/reference/kotlin/android/telecom/InCallService`.

| Parameters ||
|---|---|
| `videoState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The video state in which to answer the connection. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_AUDIO_ONLY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_TX_ENABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_RX_ENABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_BIDIRECTIONAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_PAUSED:kotlin.Int` |

### onAvailableCallEndpointsChanged

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onAvailableCallEndpointsChanged(availableEndpoints: MutableList<CallEndpoint!>): Unit
```

Notifies the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` that the available call endpoints have been changed.

| Parameters ||
|---|---|
| `availableEndpoints` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [CallEndpoint](https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint)!\>: The available call endpoints. This value cannot be `null`. |

### onCallAudioStateChanged

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCallAudioStateChanged(state: CallAudioState!): Unit
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/telecom/Conference#onCallEndpointChanged(android.telecom.CallEndpoint)`, `https://developer.android.com/reference/kotlin/android/telecom/Conference#onAvailableCallEndpointsChanged(kotlin.collections.MutableList)` and `https://developer.android.com/reference/kotlin/android/telecom/Conference#onMuteStateChanged(kotlin.Boolean)` instead.*

Notifies the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` that the `https://developer.android.com/reference/kotlin/android/telecom/Conference#getCallAudioState()` property has a new value.

| Parameters ||
|---|---|
| `state` | [CallAudioState](https://developer.android.com/reference/kotlin/android/telecom/CallAudioState)!: The new call audio state. |

### onCallEndpointChanged

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCallEndpointChanged(callEndpoint: CallEndpoint): Unit
```

Notifies the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` that the audio endpoint has been changed.

| Parameters ||
|---|---|
| `callEndpoint` | [CallEndpoint](https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint): The new call endpoint. This value cannot be `null`. |

### onConnectionAdded

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onConnectionAdded(connection: Connection!): Unit
```

Notifies the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` that a `https://developer.android.com/reference/kotlin/android/telecom/Connection` has been added to it.

| Parameters ||
|---|---|
| `connection` | [Connection](https://developer.android.com/reference/kotlin/android/telecom/Connection)!: The newly added connection. |

### onDisconnect

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onDisconnect(): Unit
```

Notifies the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` when the Conference and all it's `https://developer.android.com/reference/kotlin/android/telecom/Connection`s should be disconnected.

### onExtrasChanged

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onExtrasChanged(extras: Bundle!): Unit
```

Notifies this `https://developer.android.com/reference/kotlin/android/telecom/Conference#` of a change to the extras made outside the `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`.

These extras changes can originate from Telecom itself, or from an `https://developer.android.com/reference/kotlin/android/telecom/InCallService` via `https://developer.android.com/reference/kotlin/android/telecom/Call#putExtras(android.os.Bundle)`, and `https://developer.android.com/reference/kotlin/android/telecom/Call#removeExtras(kotlin.collections.MutableList)`.

| Parameters ||
|---|---|
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: The new extras bundle. |

### onHold

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onHold(): Unit
```

Notifies the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` when it should be put on hold.

### onMerge

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onMerge(): Unit
```

Notifies the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` when the child calls should be merged. Only invoked if the conference contains the capability `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_MERGE_CONFERENCE:kotlin.Int`.

### onMerge

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onMerge(conference: Conference): Unit
```

Notifies the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` when the specified `https://developer.android.com/reference/kotlin/android/telecom/Conference#` should be merged with the conference call.

| Parameters ||
|---|---|
| `conference` | [Conference](https://developer.android.com/reference/kotlin/android/telecom/Conference#): The `Conference` to merge. This value cannot be `null`. |

### onMerge

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onMerge(connection: Connection!): Unit
```

Notifies the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` when the specified `https://developer.android.com/reference/kotlin/android/telecom/Connection` should merged with the conference call.

| Parameters ||
|---|---|
| `connection` | [Connection](https://developer.android.com/reference/kotlin/android/telecom/Connection)!: The `Connection` to merge. |

### onMuteStateChanged

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onMuteStateChanged(isMuted: Boolean): Unit
```

Notifies the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` that its audio mute state has been changed.

| Parameters ||
|---|---|
| `isMuted` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): The new mute state. |

### onPlayDtmfTone

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onPlayDtmfTone(c: Char): Unit
```

Notifies the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` of a request to play a DTMF tone.

| Parameters ||
|---|---|
| `c` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): A DTMF character. |

### onReject

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onReject(): Unit
```

Notifies this Conference, which is in `STATE_RINGING`, of a request to reject. For managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`s, this will be called when the user rejects a call via the default dialer's `https://developer.android.com/reference/kotlin/android/telecom/InCallService`.

### onSeparate

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onSeparate(connection: Connection!): Unit
```

Notifies the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` when the specified `https://developer.android.com/reference/kotlin/android/telecom/Connection` should be separated from the conference call.

| Parameters ||
|---|---|
| `connection` | [Connection](https://developer.android.com/reference/kotlin/android/telecom/Connection)!: The connection to separate. |

### onStopDtmfTone

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onStopDtmfTone(): Unit
```

Notifies the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` of a request to stop any currently playing DTMF tones.

### onSwap

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onSwap(): Unit
```

Notifies the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` when the child calls should be swapped. Only invoked if the conference contains the capability `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_SWAP_CONFERENCE:kotlin.Int`.

### onUnhold

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onUnhold(): Unit
```

Notifies the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` when it should be moved from a held to active state.

### putExtras

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun putExtras(extras: Bundle): Unit
```

Adds some extras to this `https://developer.android.com/reference/kotlin/android/telecom/Conference#`. Existing keys are replaced and new ones are added.

No assumptions should be made as to how an In-Call UI or service will handle these extras. Keys should be fully qualified (e.g., com.example.MY_EXTRA) to avoid conflicts.

| Parameters ||
|---|---|
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#): The extras to add. This value cannot be `null`. |

### removeConnection

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeConnection(connection: Connection!): Unit
```

Removes the specified connection as a child of this conference.

| Parameters ||
|---|---|
| `connection` | [Connection](https://developer.android.com/reference/kotlin/android/telecom/Connection)!: The connection to remove. |

### removeExtras

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeExtras(vararg keys: String!): Unit
```

Removes extras from this `https://developer.android.com/reference/kotlin/android/telecom/Conference#`.

| Parameters ||
|---|---|
| `keys` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The keys of the extras to remove. |

### removeExtras

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeExtras(keys: MutableList<String!>!): Unit
```

Removes extras from this `https://developer.android.com/reference/kotlin/android/telecom/Conference#`.

| Parameters ||
|---|---|
| `keys` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: The keys of the extras to remove. |

### sendConferenceEvent

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendConferenceEvent(
    event: String, 
    extras: Bundle?
): Unit
```

Sends an event associated with this `https://developer.android.com/reference/kotlin/android/telecom/Conference#` with associated event extras to the `https://developer.android.com/reference/kotlin/android/telecom/InCallService`.

Connection events are used to communicate point in time information from a `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` to an `https://developer.android.com/reference/kotlin/android/telecom/InCallService` implementation. An example of a custom connection event includes notifying the UI when a WIFI call has been handed over to LTE, which the InCall UI might use to inform the user that billing charges may apply. The Android Telephony framework will send the `https://developer.android.com/reference/kotlin/android/telecom/Connection#EVENT_MERGE_COMPLETE:kotlin.String` connection event when a call to `https://developer.android.com/reference/kotlin/android/telecom/Call#mergeConference()` has completed successfully.

Events are exposed to `https://developer.android.com/reference/kotlin/android/telecom/InCallService` implementations via `https://developer.android.com/reference/kotlin/android/telecom/Call.Callback#onConnectionEvent(android.telecom.Call,%20kotlin.String,%20android.os.Bundle)`.

No assumptions should be made as to how an In-Call UI or service will handle these events. The `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` must assume that the In-Call UI could even chose to ignore some events altogether.

Events should be fully qualified (e.g. `com.example.event.MY_EVENT`) to avoid conflicts between `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` implementations. Further, custom `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` implementations shall not re-purpose events in the `android.*` namespace, nor shall they define new event types in this namespace. When defining a custom event type, ensure the contents of the extras `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` is clearly defined. Extra keys for this bundle should be named similar to the event type (e.g. `com.example.extra.MY_EXTRA`).

When defining events and the associated extras, it is important to keep their behavior consistent when the associated `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` is updated. Support for deprecated events/extras should me maintained to ensure backwards compatibility with older `https://developer.android.com/reference/kotlin/android/telecom/InCallService` implementations which were built to support the older behavior.

Expected connection events from the Telephony stack are:

- `https://developer.android.com/reference/kotlin/android/telecom/Connection#EVENT_CALL_HOLD_FAILED:kotlin.String` with `null` `extras` when the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` could not be held.
- `https://developer.android.com/reference/kotlin/android/telecom/Connection#EVENT_MERGE_START:kotlin.String` with `null` `extras` when a new call is being merged into the conference.
- `https://developer.android.com/reference/kotlin/android/telecom/Connection#EVENT_MERGE_COMPLETE:kotlin.String` with `null` `extras` a new call has completed being merged into the conference.
- `https://developer.android.com/reference/kotlin/android/telecom/Connection#EVENT_CALL_MERGE_FAILED:kotlin.String` with `null` `extras` a new call has failed to merge into the conference (the dialer app can determine which call failed to merge based on the fact that the call still exists outside of the conference at the end of the merge process).

| Parameters ||
|---|---|
| `event` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The conference event. This value cannot be `null`. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?: Optional bundle containing extra information associated with the event. This value may be `null`. |

### setActive

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setActive(): Unit
```

Sets state to be active.

### setConferenceableConnections

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setConferenceableConnections(conferenceableConnections: MutableList<Connection!>!): Unit
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/telecom/Conference#setConferenceables(kotlin.collections.MutableList)` instead.*

Sets the connections with which this connection can be conferenced.

| Parameters ||
|---|---|
| `conferenceableConnections` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Connection](https://developer.android.com/reference/kotlin/android/telecom/Connection)!\>!: The set of connections this conference can conference with. |

### setConferenceables

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setConferenceables(conferenceables: MutableList<Conferenceable!>): Unit
```

Sets a list of connections or conferences with which this conference can be conferenced.

| Parameters ||
|---|---|
| `conferenceables` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Conferenceable](https://developer.android.com/reference/kotlin/android/telecom/Conferenceable)!\>: The set of conferenceables this conference can conference with. This value cannot be `null`. |

### setConnectionCapabilities

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setConnectionCapabilities(connectionCapabilities: Int): Unit
```

Sets the capabilities of a conference. See `CAPABILITY_*` constants of class `https://developer.android.com/reference/kotlin/android/telecom/Connection` for valid values.

| Parameters ||
|---|---|
| `connectionCapabilities` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A bitmask of the `Capabilities` of the conference call. |

### setConnectionProperties

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setConnectionProperties(connectionProperties: Int): Unit
```

Sets the properties of a conference. See `PROPERTY_*` constants of class `https://developer.android.com/reference/kotlin/android/telecom/Connection` for valid values.

| Parameters ||
|---|---|
| `connectionProperties` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A bitmask of the `Properties` of the conference call. |

### setConnectionStartElapsedRealTime

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setConnectionStartElapsedRealTime(connectionStartElapsedRealTime: Long): Unit
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/telecom/Conference#setConnectionStartElapsedRealtimeMillis(kotlin.Long)` instead.*

Sets the start time of the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` which is the basis for the determining the duration of the `https://developer.android.com/reference/kotlin/android/telecom/Conference#`.

You should use a value returned by `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#elapsedRealtime()` to ensure that time zone changes do not impact the conference duration.

When setting this, you should also set the connection time via `https://developer.android.com/reference/kotlin/android/telecom/Conference#setConnectionTime(kotlin.Long)`.

| Parameters ||
|---|---|
| `connectionStartElapsedRealTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The connection time, as measured by `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#elapsedRealtime()`. |

### setConnectionStartElapsedRealtimeMillis

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setConnectionStartElapsedRealtimeMillis(connectionStartElapsedRealTime: Long): Unit
```

Sets the start time of the `https://developer.android.com/reference/kotlin/android/telecom/Conference#` which is the basis for the determining the duration of the `https://developer.android.com/reference/kotlin/android/telecom/Conference#`.

You should use a value returned by `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#elapsedRealtime()` to ensure that time zone changes do not impact the conference duration.

When setting this, you should also set the connection time via `https://developer.android.com/reference/kotlin/android/telecom/Conference#setConnectionTime(kotlin.Long)`.

| Parameters ||
|---|---|
| `connectionStartElapsedRealTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The connection time, as measured by `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#elapsedRealtime()`. Value is a non-negative timestamp in the `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#elapsedRealtime()` time base. |

### setConnectionTime

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setConnectionTime(connectionTimeMillis: Long): Unit
```

Sets the connection start time of the `Conference`. This is used in the call log to indicate the date and time when the conference took place.

Should be specified in wall-clock time returned by `https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()`.

When setting the connection time, you should always set the connection elapsed time via `https://developer.android.com/reference/kotlin/android/telecom/Conference#setConnectionStartElapsedRealtimeMillis(kotlin.Long)` to ensure the duration is reflected.

| Parameters ||
|---|---|
| `connectionTimeMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The connection time, in milliseconds, as returned by `https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()`. Value is 0 or greater |

### setDialing

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setDialing(): Unit
```

Sets state to be dialing.

### setDisconnected

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setDisconnected(disconnectCause: DisconnectCause!): Unit
```

Sets state to disconnected.

| Parameters ||
|---|---|
| `disconnectCause` | [DisconnectCause](https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause)!: The reason for the disconnection, as described by `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause`. |

### setExtras

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setExtras(extras: Bundle?): Unit
```

Replaces all the extras associated with this `Conference`.

New or existing keys are replaced in the `Conference` extras. Keys which are no longer in the new extras, but were present the last time `setExtras` was called are removed.

Alternatively you may use the `https://developer.android.com/reference/kotlin/android/telecom/Conference#putExtras(android.os.Bundle)`, and `https://developer.android.com/reference/kotlin/android/telecom/Conference#removeExtras(kotlin.String)` methods to modify the extras.

No assumptions should be made as to how an In-Call UI or service will handle these extras. Keys should be fully qualified (e.g., com.example.extras.MY_EXTRA) to avoid conflicts.

| Parameters ||
|---|---|
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?: The extras associated with this `Conference`. This value may be `null`. |

### setOnHold

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setOnHold(): Unit
```

Sets state to be on hold.

### setRingbackRequested

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setRingbackRequested(ringback: Boolean): Unit
```

Requests that the framework play a ringback tone. This is to be invoked by implementations that do not play a ringback tone themselves in the conference's audio stream.

| Parameters ||
|---|---|
| `ringback` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether the ringback tone is to be played. |

### setRinging

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setRinging(): Unit
```

Sets state to be ringing.

### setStatusHints

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setStatusHints(statusHints: StatusHints!): Unit
```

Sets the label and icon status to display in the InCall UI.

| Parameters ||
|---|---|
| `statusHints` | [StatusHints](https://developer.android.com/reference/kotlin/android/telecom/StatusHints)!: The status label and icon to set. |

### setVideoProvider

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setVideoProvider(
    c: Connection!, 
    videoProvider: Connection.VideoProvider!
): Unit
```

Sets the video connection provider.

| Parameters ||
|---|---|
| `videoProvider` | [Connection.VideoProvider](https://developer.android.com/reference/kotlin/android/telecom/Connection.VideoProvider)!: The video provider. |

### setVideoState

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setVideoState(
    c: Connection!, 
    videoState: Int
): Unit
```

Set the video state for the conference. Valid values: `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_AUDIO_ONLY:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_BIDIRECTIONAL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_TX_ENABLED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_RX_ENABLED:kotlin.Int`.

| Parameters ||
|---|---|
| `videoState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new video state. |

### toString

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |
