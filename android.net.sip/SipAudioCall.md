# SipAudioCall

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SipAudioCall

Kotlin| [Java](../android/net/sip/SipAudioCall.md) 
| --- | --- |

```
open class SipAudioCall
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.sip.SipAudioCall](../android/net/sip/SipAudioCall.md) |

| **This class was deprecated in API level 31.**
|
| [android.net.sip.SipManager](../android/net/sip/SipManager.md) and associated classes are no longer supported and should not be used as the basis of future VOIP apps.

Handles an Internet audio call over SIP. You can instantiate this class with [SipManager](../android/net/sip/SipManager.md), using android.net.sip.SipManager#makeAudioCall and [takeAudioCall()](../android/net/sip/SipManager.md)).

**Note:** Using this class require the [android.Manifest.permission#INTERNET](../android/Manifest.permission.md) and [android.Manifest.permission#USE_SIP](../android/Manifest.permission.md) permissions. In addition, [startAudio](../android/net/sip/SipAudioCall.md))requires the [android.Manifest.permission#RECORD_AUDIO](../android/Manifest.permission.md), [android.Manifest.permission#ACCESS_WIFI_STATE](../android/Manifest.permission.md), and [android.Manifest.permission#WAKE_LOCK](../android/Manifest.permission.md) permissions; and [setSpeakerMode()](../android/net/sip/SipAudioCall.md))requires the [android.Manifest.permission#MODIFY_AUDIO_SETTINGS](../android/Manifest.permission.md) permission.
|
| ### Developer Guides
|
| For more information about using SIP, read the [Session Initiation Protocol](https://developer.android.com/guide/topics/network/sip.html) developer guide.

## Summary

| Nested classes ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Listener](../android/net/sip/SipAudioCall.Listener.md) Listener for events relating to a SIP call, such as when a call is being received ("on ringing") or a call is outgoing ("on calling"). |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SipAudioCall](../android/net/sip/SipAudioCall.md))`(`context:` ` [Context](../android/content/Context.md)!`, `localProfile:` ` [SipProfile](../android/net/sip/SipProfile.md)!`)` Creates a call object with the local SIP profile. |

| Public methods ||
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [answerCall](../android/net/sip/SipAudioCall.md))`(`timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Answers a call. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [attachCall](../android/net/sip/SipAudioCall.md))`(`session:` ` [SipSession](../android/net/sip/SipSession.md)!`, `sessionDescription:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Attaches an incoming call to this call object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../android/net/sip/SipAudioCall.md))`()` Closes this object. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [continueCall](../android/net/sip/SipAudioCall.md))`(`timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Continues a call that's on hold. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endCall](../android/net/sip/SipAudioCall.md))`()` Ends a call. |
| open [SipProfile](../android/net/sip/SipProfile.md)! | [getLocalProfile](../android/net/sip/SipAudioCall.md))`()` Gets the local SIP profile. |
| --- | --- |
| open [SipProfile](../android/net/sip/SipProfile.md)! | [getPeerProfile](../android/net/sip/SipAudioCall.md))`()` Gets the peer's SIP profile. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getState](../android/net/sip/SipAudioCall.md))`()` Gets the state of the [SipSession](../android/net/sip/SipSession.md) that carries this call. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [holdCall](../android/net/sip/SipAudioCall.md))`(`timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Puts a call on hold. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInCall](../android/net/sip/SipAudioCall.md))`()` Checks if the call is established. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMuted](../android/net/sip/SipAudioCall.md))`()` Checks if the call is muted. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOnHold](../android/net/sip/SipAudioCall.md))`()` Checks if the call is on hold. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [makeCall](../android/net/sip/SipAudioCall.md))`(`peerProfile:` ` [SipProfile](../android/net/sip/SipProfile.md)!`, `sipSession:` ` [SipSession](../android/net/sip/SipSession.md)!`, `timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Initiates an audio call to the specified profile. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendDtmf](../android/net/sip/SipAudioCall.md))`(`code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sends a DTMF code. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendDtmf](../android/net/sip/SipAudioCall.md))`(`code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `result:` ` [Message](../android/os/Message.md)!`)` Sends a DTMF code. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setListener](../android/net/sip/SipAudioCall.md))`(`listener:` ` [SipAudioCall.Listener](../android/net/sip/SipAudioCall.Listener.md)!`)` Sets the listener to listen to the audio call events. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setListener](../android/net/sip/SipAudioCall.md))`(`listener:` ` [SipAudioCall.Listener](../android/net/sip/SipAudioCall.Listener.md)!`, `callbackImmediately:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the listener to listen to the audio call events. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSpeakerMode](../android/net/sip/SipAudioCall.md))`(`speakerMode:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Puts the device to speaker mode. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startAudio](../android/net/sip/SipAudioCall.md))`()` Starts the audio for the established call. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [toggleMute](../android/net/sip/SipAudioCall.md))`()` Toggles mute. |

## Public constructors

### SipAudioCall

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SipAudioCall(
    context: Context!, 
    localProfile: SipProfile!)
```

Creates a call object with the local SIP profile.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:the context for accessing system services such as ringtone, audio, WIFI etc |

## Public methods

### answerCall

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun answerCall(timeout: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Answers a call. The attempt will be timed out if the call is not established within`timeout`seconds and [onError(SipAudioCall, SipErrorCode.TIME_OUT, String)](../android/net/sip/SipAudioCall.Listener.md))will be called.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the timeout value in seconds. Default value (defined by SIP protocol) is used if`timeout`is zero or negative. |

| Exceptions ||
|--------------------------------|---------------------------------------------|
| `android.net.sip.SipException` | if the SIP service fails to answer the call |

**See Also**

- [android.net.sip.SipAudioCall.Listener#onError](../android/net/sip/SipAudioCall.Listener.md)) 

### attachCall

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun attachCall(
    session: SipSession!, 
    sessionDescription: String!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Attaches an incoming call to this call object.

| Parameters ||
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `session` | [SipSession](../android/net/sip/SipSession.md)!:the session that receives the incoming call |
| `sessionDescription` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the session description of the incoming call |

| Exceptions ||
|--------------------------------|----------------------------------------------------------------------------------------------------------|
| `android.net.sip.SipException` | if the SIP service fails to attach this object to the session or VOIP API is not supported by the device |

**See Also**

- [android.net.sip.SipManager#isVoipSupported](../android/net/sip/SipManager.md)) 

### close

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

**Deprecated:** *Deprecated in Java.*

Closes this object. This object is not usable after being closed. 

### continueCall

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun continueCall(timeout: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Continues a call that's on hold. When succeeds, [Listener.onCallEstablished](../android/net/sip/SipAudioCall.Listener.md))is called. The attempt will be timed out if the call is not established within`timeout`seconds and [onError(SipAudioCall, SipErrorCode.TIME_OUT, String)](../android/net/sip/SipAudioCall.Listener.md))will be called.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the timeout value in seconds. Default value (defined by SIP protocol) is used if`timeout`is zero or negative. |

| Exceptions ||
|--------------------------------|---------------------------------------------|
| `android.net.sip.SipException` | if the SIP service fails to unhold the call |

**See Also**

- [android.net.sip.SipAudioCall.Listener#onError](../android/net/sip/SipAudioCall.Listener.md)) 

### endCall

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun endCall(): Unit
```

**Deprecated:** *Deprecated in Java.*

Ends a call.

| Exceptions ||
|--------------------------------|------------------------------------------|
| `android.net.sip.SipException` | if the SIP service fails to end the call |

### getLocalProfile

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLocalProfile(): SipProfile!
```

**Deprecated:** *Deprecated in Java.*

Gets the local SIP profile.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------|
| [SipProfile](../android/net/sip/SipProfile.md)! | the local SIP profile |

### getPeerProfile

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPeerProfile(): SipProfile!
```

**Deprecated:** *Deprecated in Java.*

Gets the peer's SIP profile.

| Return ||
|------------------------------------------------------------------------------------------|------------------------|
| [SipProfile](../android/net/sip/SipProfile.md)! | the peer's SIP profile |

### getState

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getState(): Int
```

**Deprecated:** *Deprecated in Java.*

Gets the state of the [SipSession](../android/net/sip/SipSession.md) that carries this call. The value returned must be one of the states in [SipSession.State](../android/net/sip/SipSession.State.md).

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the session state |

### holdCall

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun holdCall(timeout: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Puts a call on hold. When succeeds, [Listener.onCallHeld](../android/net/sip/SipAudioCall.Listener.md))is called. The attempt will be timed out if the call is not established within`timeout`seconds and [onError(SipAudioCall, SipErrorCode.TIME_OUT, String)](../android/net/sip/SipAudioCall.Listener.md))will be called.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the timeout value in seconds. Default value (defined by SIP protocol) is used if`timeout`is zero or negative. |

| Exceptions ||
|--------------------------------|-------------------------------------------|
| `android.net.sip.SipException` | if the SIP service fails to hold the call |

**See Also**

- [android.net.sip.SipAudioCall.Listener#onError](../android/net/sip/SipAudioCall.Listener.md)) 

### isInCall

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isInCall(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Checks if the call is established.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the call is established |

### isMuted

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isMuted(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Checks if the call is muted.

| Return ||
|------------------------------------------------------------------------------------|---------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the call is muted |

### isOnHold

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isOnHold(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Checks if the call is on hold.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the call is on hold |

### makeCall

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun makeCall(
    peerProfile: SipProfile!, 
    sipSession: SipSession!, 
    timeout: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Initiates an audio call to the specified profile. The attempt will be timed out if the call is not established within`timeout`seconds and [onError(SipAudioCall, SipErrorCode.TIME_OUT, String)](../android/net/sip/SipAudioCall.Listener.md))will be called.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `peerProfile` | [SipProfile](../android/net/sip/SipProfile.md)!:the SIP profile to make the call to |
| `sipSession` | [SipSession](../android/net/sip/SipSession.md)!:the [SipSession](../android/net/sip/SipSession.md) for carrying out the call |
| `timeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the timeout value in seconds. Default value (defined by SIP protocol) is used if`timeout`is zero or negative. |
| --- | --- |

| Exceptions ||
|--------------------------------|------------------------------------------------------------------------------------------------------|
| `android.net.sip.SipException` | if the SIP service fails to create a session for the call or VOIP API is not supported by the device |

**See Also**

- [android.net.sip.SipAudioCall.Listener#onError](../android/net/sip/SipAudioCall.Listener.md))
- [android.net.sip.SipManager#isVoipSupported](../android/net/sip/SipManager.md)) 

### sendDtmf

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun sendDtmf(code: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Sends a DTMF code. According to [RFC 2883](http://tools.ietf.org/html/rfc2833), event 0--9 maps to decimal value 0--9, '\*' to 10, '#' to 11, event 'A'--'D' to 12--15, and event flash to 16. Currently, event flash is not supported.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the DTMF code to send. Value 0 to 15 (inclusive) are valid inputs. |

### sendDtmf

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun sendDtmf(
    code: Int, 
    result: Message!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sends a DTMF code. According to [RFC 2883](http://tools.ietf.org/html/rfc2833), event 0--9 maps to decimal value 0--9, '\*' to 10, '#' to 11, event 'A'--'D' to 12--15, and event flash to 16. Currently, event flash is not supported.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the DTMF code to send. Value 0 to 15 (inclusive) are valid inputs. |
| `result` | [Message](../android/os/Message.md)!:the result message to send when done |

### setListener

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setListener(listener: SipAudioCall.Listener!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the listener to listen to the audio call events. The method calls #setListener.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [SipAudioCall.Listener](../android/net/sip/SipAudioCall.Listener.md)!:to listen to the audio call events of this object |

**See Also**

- [#setListener(Listener, boolean)](../android/net/sip/SipAudioCall.md)) 

### setListener

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setListener(
    listener: SipAudioCall.Listener!, 
    callbackImmediately: Boolean
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the listener to listen to the audio call events. A [SipAudioCall](../android/net/sip/SipAudioCall.md) can only hold one listener at a time. Subsequent calls to this method override the previous listener.

| Parameters ||
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [SipAudioCall.Listener](../android/net/sip/SipAudioCall.Listener.md)!:to listen to the audio call events of this object |
| `callbackImmediately` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):set to true if the caller wants to be called back immediately on the current state |

### setSpeakerMode

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSpeakerMode(speakerMode: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Puts the device to speaker mode.

**Note:** Requires the [android.Manifest.permission#MODIFY_AUDIO_SETTINGS](../android/Manifest.permission.md) permission.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `speakerMode` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):set true to enable speaker mode; false to disable |

### startAudio

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startAudio(): Unit
```

**Deprecated:** *Deprecated in Java.*

Starts the audio for the established call. This method should be called after [Listener.onCallEstablished](../android/net/sip/SipAudioCall.Listener.md))is called.

**Note:** Requires the [android.Manifest.permission#RECORD_AUDIO](../android/Manifest.permission.md), [android.Manifest.permission#ACCESS_WIFI_STATE](../android/Manifest.permission.md) and [android.Manifest.permission#WAKE_LOCK](../android/Manifest.permission.md) permissions. 

### toggleMute

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toggleMute(): Unit
```

**Deprecated:** *Deprecated in Java.*

Toggles mute.
