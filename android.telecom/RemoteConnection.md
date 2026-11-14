Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RemoteConnection

Kotlin | [Java](RemoteConnection.md)
| --- | --- |

```
class RemoteConnection
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telecom.RemoteConnection](RemoteConnection.md) |

A connection provided to a ConnectionService by another `ConnectionService` running in a different process.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/telecom/RemoteConnection.Callback` Callback base class for RemoteConnection. |
| | `https://developer.android.com/reference/kotlin/android/telecom/RemoteConnection.VideoProvider` `https://developer.android.com/reference/kotlin/android/telecom/RemoteConnection.VideoProvider` associated with a RemoteConnection. |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | abort Instructs this `RemoteConnection` to abort. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addConferenceParticipants Instructs this RemoteConnection to initiate a conference with a list of participants. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | answer Instructs this `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_RINGING:kotlin.Int` `RemoteConnection` to answer. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | disconnect Instructs this `RemoteConnection` to disconnect. |
| [Uri](../android.net/Uri.md)! | getAddress Obtains the address of this `RemoteConnection`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getAddressPresentation Obtains the presentation requirements for the address of this `RemoteConnection`. |
| --- | --- |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | getCallerDisplayName Obtains the display name for this `RemoteConnection`'s caller. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getCallerDisplayNamePresentation Obtains the presentation requirements for this `RemoteConnection`'s caller's display name. |
| [RemoteConference](RemoteConference.md)! | getConference Obtain the `RemoteConference` that this `RemoteConnection` may be a part of, or `null` if there is no such `RemoteConference`. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [RemoteConnection](RemoteConnection.md)!\>! | getConferenceableConnections Obtain the `RemoteConnection`s with which this `RemoteConnection` may be successfully asked to create a conference with. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getConnectionCapabilities Obtains the capabilities of this `RemoteConnection`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getConnectionProperties Obtains the properties of this `RemoteConnection`. |
| --- | --- |
| [DisconnectCause](DisconnectCause.md)! | getDisconnectCause Obtains the reason why this `RemoteConnection` may have been disconnected. |
| [Bundle](../android.os/Bundle.md)! | getExtras Obtain the extras associated with this `RemoteConnection`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getState Obtains the state of this `RemoteConnection`. |
| --- | --- |
| [StatusHints](StatusHints.md)! | getStatusHints Obtains status hints pertaining to this `RemoteConnection`. |
| [RemoteConnection.VideoProvider](../android/telecom/RemoteConnection.VideoProvider.md)! | getVideoProvider Obtains the video provider of this `RemoteConnection`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getVideoState Obtains the video state of this `RemoteConnection`. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | hold Instructs this `RemoteConnection` to go on hold. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isRingbackRequested Determines whether this `RemoteConnection` is requesting ringback. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isVoipAudioMode Determines if the audio mode of this `RemoteConnection` is VOIP. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | playDtmfTone Instructs this `RemoteConnection` to play a dual-tone multi-frequency signaling (DTMF) tone. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | postDialContinue Instructs this `RemoteConnection` to continue playing a post-dial DTMF string. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | pullExternalCall Instructs this RemoteConnection to pull itself to the local device. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | registerCallback Adds a callback to this `RemoteConnection`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | registerCallback Adds a callback to this `RemoteConnection`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | reject Instructs this `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_RINGING:kotlin.Int` `RemoteConnection` to reject. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setCallAudioState Set the audio state of this `RemoteConnection`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | stopDtmfTone Instructs this `RemoteConnection` to stop any dual-tone multi-frequency signaling (DTMF) tone currently playing. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | unhold Instructs this `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_HOLDING:kotlin.Int` call to release from hold. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | unregisterCallback Removes a callback from this `RemoteConnection`. |

## Public methods

### abort

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun abort(): Unit
```

Instructs this `RemoteConnection` to abort.

### addConferenceParticipants

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addConferenceParticipants(participants: MutableList<Uri!>): Unit
```

Instructs this RemoteConnection to initiate a conference with a list of participants.

<br />

| Parameters ||
|---|---|
| `participants` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Uri](../android.net/Uri.md)!\>: with which conference call will be formed. This value cannot be `null`. |

### answer

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun answer(): Unit
```

Instructs this `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_RINGING:kotlin.Int` `RemoteConnection` to answer.

### disconnect

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun disconnect(): Unit
```

Instructs this `RemoteConnection` to disconnect.

### getAddress

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAddress(): Uri!
```

Obtains the address of this `RemoteConnection`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#!` | The address (e.g., phone number) to which the `RemoteConnection` is currently connected. |

### getAddressPresentation

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAddressPresentation(): Int
```

Obtains the presentation requirements for the address of this `RemoteConnection`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The presentation requirements for the address. See TelecomManager for valid values. |

### getCallerDisplayName

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCallerDisplayName(): CharSequence!
```

Obtains the display name for this `RemoteConnection`'s caller.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` | The display name for the caller. |

### getCallerDisplayNamePresentation

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCallerDisplayNamePresentation(): Int
```

Obtains the presentation requirements for this `RemoteConnection`'s caller's display name.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The presentation requirements for the caller display name. See TelecomManager for valid values. |

### getConference

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getConference(): RemoteConference!
```

Obtain the `RemoteConference` that this `RemoteConnection` may be a part of, or `null` if there is no such `RemoteConference`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/RemoteConference!` | A `RemoteConference` or `null`; |

### getConferenceableConnections

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getConferenceableConnections(): MutableList<RemoteConnection!>!
```

Obtain the `RemoteConnection`s with which this `RemoteConnection` may be successfully asked to create a conference with.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/telecom/RemoteConnection#!>!` | The `RemoteConnection`s with which this `RemoteConnection` may be merged into a RemoteConference. |

### getConnectionCapabilities

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getConnectionCapabilities(): Int
```

Obtains the capabilities of this `RemoteConnection`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A bitmask of the capabilities of the `RemoteConnection`, as defined in the `CAPABILITY_*` constants in class Connection. |

### getConnectionProperties

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getConnectionProperties(): Int
```

Obtains the properties of this `RemoteConnection`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A bitmask of the properties of the `RemoteConnection`, as defined in the `PROPERTY_*` constants in class Connection. |

### getDisconnectCause

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDisconnectCause(): DisconnectCause!
```

Obtains the reason why this `RemoteConnection` may have been disconnected.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause!` | For a `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_DISCONNECTED:kotlin.Int` `RemoteConnection`, the disconnect cause expressed as a code chosen from among those declared in DisconnectCause. |

### getExtras

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getExtras(): Bundle!
```

Obtain the extras associated with this `RemoteConnection`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` | The extras for this connection. |

### getState

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getState(): Int
```

Obtains the state of this `RemoteConnection`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A state value, chosen from the `STATE_*` constants. |

### getStatusHints

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getStatusHints(): StatusHints!
```

Obtains status hints pertaining to this `RemoteConnection`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/StatusHints!` | The current StatusHints of this `RemoteConnection`, or `null` if none have been set. |

### getVideoProvider

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getVideoProvider(): RemoteConnection.VideoProvider!
```

Obtains the video provider of this `RemoteConnection`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/RemoteConnection.VideoProvider!` | The video provider associated with this `RemoteConnection`. |

### getVideoState

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getVideoState(): Int
```

Obtains the video state of this `RemoteConnection`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The video state of the `RemoteConnection`. See VideoProfile. |

### hold

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hold(): Unit
```

Instructs this `RemoteConnection` to go on hold.

### isRingbackRequested

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isRingbackRequested(): Boolean
```

Determines whether this `RemoteConnection` is requesting ringback.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the `RemoteConnection` is requesting that the framework play a ringback tone on its behalf. |

### isVoipAudioMode

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isVoipAudioMode(): Boolean
```

Determines if the audio mode of this `RemoteConnection` is VOIP.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the `RemoteConnection`'s current audio mode is VOIP. |

### playDtmfTone

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun playDtmfTone(digit: Char): Unit
```

Instructs this `RemoteConnection` to play a dual-tone multi-frequency signaling (DTMF) tone. Any other currently playing DTMF tone in the specified call is immediately stopped.

| Parameters ||
|---|---|
| `digit` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): A character representing the DTMF digit for which to play the tone. This value must be one of `'0'` through `'9'`, `'*'` or `'#'`. |

### postDialContinue

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun postDialContinue(proceed: Boolean): Unit
```

Instructs this `RemoteConnection` to continue playing a post-dial DTMF string. A post-dial DTMF string is a string of digits following the first instance of either `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#DTMF_CHARACTER_WAIT:kotlin.Char` or `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#DTMF_CHARACTER_PAUSE:kotlin.Char`. These digits are immediately sent as DTMF tones to the recipient as soon as the connection is made. If the DTMF string contains a `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#DTMF_CHARACTER_PAUSE:kotlin.Char` symbol, this `RemoteConnection` will temporarily pause playing the tones for a pre-defined period of time. If the DTMF string contains a `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#DTMF_CHARACTER_WAIT:kotlin.Char` symbol, this `RemoteConnection` will pause playing the tones and notify callbacks via onPostDialWait. At this point, the in-call app should display to the user an indication of this state and an affordance to continue the postdial sequence. When the user decides to continue the postdial sequence, the in-call app should invoke the postDialContinue method.

| Parameters ||
|---|---|
| `proceed` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether or not to continue with the post-dial sequence. |

### pullExternalCall

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun pullExternalCall(): Unit
```

Instructs this RemoteConnection to pull itself to the local device.

See pullExternalCall for more information.

### registerCallback

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerCallback(callback: RemoteConnection.Callback!): Unit
```

Adds a callback to this `RemoteConnection`.

| Parameters ||
|---|---|
| `callback` | [RemoteConnection.Callback](../android/telecom/RemoteConnection.Callback.md)!: A `Callback`. |

### registerCallback

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerCallback(
    callback: RemoteConnection.Callback!, 
    handler: Handler!
): Unit
```

Adds a callback to this `RemoteConnection`.

| Parameters ||
|---|---|
| `callback` | [RemoteConnection.Callback](../android/telecom/RemoteConnection.Callback.md)!: A `Callback`. |
| `handler` | [Handler](../android.os/Handler.md)!: A `Handler` which command and status changes will be delivered to. |

### reject

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun reject(): Unit
```

Instructs this `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_RINGING:kotlin.Int` `RemoteConnection` to reject.

### setCallAudioState

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setCallAudioState(state: CallAudioState!): Unit
```

Set the audio state of this `RemoteConnection`.

| Parameters ||
|---|---|
| `state` | [CallAudioState](CallAudioState.md)!: The audio state of this `RemoteConnection`. |

### stopDtmfTone

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun stopDtmfTone(): Unit
```

Instructs this `RemoteConnection` to stop any dual-tone multi-frequency signaling (DTMF) tone currently playing. DTMF tones are played by calling playDtmfTone. If no DTMF tone is currently playing, this method will do nothing.

### unhold

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unhold(): Unit
```

Instructs this `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_HOLDING:kotlin.Int` call to release from hold.

### unregisterCallback

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unregisterCallback(callback: RemoteConnection.Callback!): Unit
```

Removes a callback from this `RemoteConnection`.

| Parameters ||
|---|---|
| `callback` | [RemoteConnection.Callback](../android/telecom/RemoteConnection.Callback.md)!: A `Callback`. |
