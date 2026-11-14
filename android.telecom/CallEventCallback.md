Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CallEventCallback

Kotlin | [Java](https://developer.android.com/reference/android/telecom/CallEventCallback "View this page in Java")

```
interface CallEventCallback
```

| [android.telecom.CallEventCallback](https://developer.android.com/reference/kotlin/android/telecom/CallEventCallback#) |

CallEventCallback relays call updates (that do not require any action) from the Telecom framework out to the application. This can include operations which the app must implement on a Call due to the presence of other calls on the device, requests relayed from a Bluetooth device, or from another calling surface.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/CallEventCallback#onAvailableCallEndpointsChanged(kotlin.collections.MutableList)(availableEndpoints: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint!>)` Telecom is informing the client that the available `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint`s have changed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/CallEventCallback#onCallEndpointChanged(android.telecom.CallEndpoint)(newCallEndpoint: https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint)` Telecom is informing the client the current `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint` changed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/CallEventCallback#onCallStreamingFailed(kotlin.Int)(reason: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Telecom is informing the client user requested call streaming but the stream can't be started. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/CallEventCallback#onEvent(kotlin.String,%20android.os.Bundle)(event: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#)` Informs this `https://developer.android.com/reference/kotlin/android/telecom/CallEventCallback#` on events raised from a `https://developer.android.com/reference/kotlin/android/telecom/InCallService` presenting this call. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/CallEventCallback#onMuteStateChanged(kotlin.Boolean)(isMuted: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Called when the mute state changes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/CallEventCallback#onVideoStateChanged(kotlin.Int)(videoState: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Called when the video state changes. |

## Public methods

### onAvailableCallEndpointsChanged

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onAvailableCallEndpointsChanged(availableEndpoints: MutableList<CallEndpoint!>): Unit
```

Telecom is informing the client that the available `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint`s have changed.

| Parameters ||
|---|---|
| `availableEndpoints` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [CallEndpoint](https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint)!\>: The set of available `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint`s reported by Telecom. This value cannot be `null`. |

### onCallEndpointChanged

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onCallEndpointChanged(newCallEndpoint: CallEndpoint): Unit
```

Telecom is informing the client the current `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint` changed.

| Parameters ||
|---|---|
| `newCallEndpoint` | [CallEndpoint](https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint): The new `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint` through which call media flows (i.e. speaker, bluetooth, etc.). This value cannot be `null`. |

### onCallStreamingFailed

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onCallStreamingFailed(reason: Int): Unit
```

Telecom is informing the client user requested call streaming but the stream can't be started.

| Parameters ||
|---|---|
| `reason` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Code to indicate the reason of this failure. Value is one of the following: |

### onEvent

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onEvent(
    event: String, 
    extras: Bundle
): Unit
```

Informs this `https://developer.android.com/reference/kotlin/android/telecom/CallEventCallback#` on events raised from a `https://developer.android.com/reference/kotlin/android/telecom/InCallService` presenting this call. These events and the associated extra keys for the `Bundle` parameter are mutually defined by a VoIP application and `https://developer.android.com/reference/kotlin/android/telecom/InCallService`. This enables alternative calling surfaces, such as an automotive UI, to relay requests to perform other non-standard call actions to the app. For example, an automotive calling solution may offer the ability for the user to raise their hand during a meeting.

| Parameters ||
|---|---|
| `event` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): a string event identifier agreed upon between a VoIP application and an `https://developer.android.com/reference/kotlin/android/telecom/InCallService` This value cannot be `null`. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#): a `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` containing information about the event, as agreed upon between a VoIP application and `https://developer.android.com/reference/kotlin/android/telecom/InCallService`. This value cannot be `null`. |

### onMuteStateChanged

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onMuteStateChanged(isMuted: Boolean): Unit
```

Called when the mute state changes.

| Parameters ||
|---|---|
| `isMuted` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): The current mute state. |

### onVideoStateChanged

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onVideoStateChanged(videoState: Int): Unit
```

Called when the video state changes.

| Parameters ||
|---|---|
| `videoState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The current video state. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#AUDIO_CALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#VIDEO_CALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#MESSAGING:kotlin.Int` |
