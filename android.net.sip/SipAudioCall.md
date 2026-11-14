# SipAudioCall

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SipAudioCall

Kotlin| [Java](https://developer.android.com/reference/android/net/sip/SipAudioCall "View this page in Java") 
| --- | --- |

```
open class SipAudioCall
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.sip.SipAudioCall](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall#) |

| **This class was deprecated in API level 31.**
|
| [android.net.sip.SipManager](https://developer.android.com/reference/kotlin/android/net/sip/SipManager) and associated classes are no longer supported and should not be used as the basis of future VOIP apps.

Handles an Internet audio call over SIP. You can instantiate this class with [SipManager](https://developer.android.com/reference/kotlin/android/net/sip/SipManager), using android.net.sip.SipManager#makeAudioCall and [takeAudioCall()](https://developer.android.com/reference/kotlin/android/net/sip/SipManager#takeAudioCall(android.content.Intent,%20android.net.sip.SipAudioCall.Listener)).

**Note:** Using this class require the [android.Manifest.permission#INTERNET](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#INTERNET:kotlin.String) and [android.Manifest.permission#USE_SIP](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#USE_SIP:kotlin.String) permissions. In addition, [startAudio](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall#startAudio())requires the [android.Manifest.permission#RECORD_AUDIO](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#RECORD_AUDIO:kotlin.String), [android.Manifest.permission#ACCESS_WIFI_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String), and [android.Manifest.permission#WAKE_LOCK](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WAKE_LOCK:kotlin.String) permissions; and [setSpeakerMode()](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall#setSpeakerMode(kotlin.Boolean))requires the [android.Manifest.permission#MODIFY_AUDIO_SETTINGS](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_AUDIO_SETTINGS:kotlin.String) permission.
|
| ### Developer Guides
|
| For more information about using SIP, read the [Session Initiation Protocol](https://developer.android.com/guide/topics/network/sip.html) developer guide.

## Summary

| Nested classes ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Listener](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall.Listener) Listener for events relating to a SIP call, such as when a call is being received ("on ringing") or a call is outgoing ("on calling"). |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SipAudioCall](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall#SipAudioCall(android.content.Context,%20android.net.sip.SipProfile))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `localProfile:` ` [SipProfile](https://developer.android.com/reference/kotlin/android/net/sip/SipProfile)!`)` Creates a call object with the local SIP profile. |

| Public methods ||
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [answerCall](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall#answerCall(kotlin.Int))`(`timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Answers a call. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [attachCall](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall#attachCall(android.net.sip.SipSession,%20kotlin.String))`(`session:` ` [SipSession](https://developer.android.com/reference/kotlin/android/net/sip/SipSession)!`, `sessionDescription:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Attaches an incoming call to this call object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall#close())`()` Closes this object. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [continueCall](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall#continueCall(kotlin.Int))`(`timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Continues a call that's on hold. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endCall](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall#endCall())`()` Ends a call. |
| open [SipProfile](https://developer.android.com/reference/kotlin/android/net/sip/SipProfile)! | [getLocalProfile](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall#getLocalProfile())`()` Gets the local SIP profile. |
| --- | --- |
| open [SipProfile](https://developer.android.com/reference/kotlin/android/net/sip/SipProfile)! | [getPeerProfile](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall#getPeerProfile())`()` Gets the peer's SIP profile. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getState](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall#getState())`()` Gets the state of the [SipSession](https://developer.android.com/reference/kotlin/android/net/sip/SipSession) that carries this call. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [holdCall](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall#holdCall(kotlin.Int))`(`timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Puts a call on hold. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInCall](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall#isInCall())`()` Checks if the call is established. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMuted](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall#isMuted())`()` Checks if the call is muted. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOnHold](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall#isOnHold())`()` Checks if the call is on hold. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [makeCall](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall#makeCall(android.net.sip.SipProfile,%20android.net.sip.SipSession,%20kotlin.Int))`(`peerProfile:` ` [SipProfile](https://developer.android.com/reference/kotlin/android/net/sip/SipProfile)!`, `sipSession:` ` [SipSession](https://developer.android.com/reference/kotlin/android/net/sip/SipSession)!`, `timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Initiates an audio call to the specified profile. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendDtmf](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall#sendDtmf(kotlin.Int))`(`code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sends a DTMF code. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendDtmf](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall#sendDtmf(kotlin.Int,%20android.os.Message))`(`code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `result:` ` [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#)!`)` Sends a DTMF code. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setListener](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall#setListener(android.net.sip.SipAudioCall.Listener))`(`listener:` ` [SipAudioCall.Listener](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall.Listener)!`)` Sets the listener to listen to the audio call events. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setListener](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall#setListener(android.net.sip.SipAudioCall.Listener,%20kotlin.Boolean))`(`listener:` ` [SipAudioCall.Listener](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall.Listener)!`, `callbackImmediately:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the listener to listen to the audio call events. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSpeakerMode](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall#setSpeakerMode(kotlin.Boolean))`(`speakerMode:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Puts the device to speaker mode. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startAudio](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall#startAudio())`()` Starts the audio for the established call. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [toggleMute](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall#toggleMute())`()` Toggles mute. |

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:the context for accessing system services such as ringtone, audio, WIFI etc |

## Public methods

### answerCall

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun answerCall(timeout: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Answers a call. The attempt will be timed out if the call is not established within`timeout`seconds and [onError(SipAudioCall, SipErrorCode.TIME_OUT, String)](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall.Listener#onError(android.net.sip.SipAudioCall,%20kotlin.Int,%20kotlin.String))will be called.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the timeout value in seconds. Default value (defined by SIP protocol) is used if`timeout`is zero or negative. |

| Exceptions ||
|--------------------------------|---------------------------------------------|
| `android.net.sip.SipException` | if the SIP service fails to answer the call |

**See Also**

- [android.net.sip.SipAudioCall.Listener#onError](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall.Listener#onError(android.net.sip.SipAudioCall,%20kotlin.Int,%20kotlin.String)) 

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
| `session` | [SipSession](https://developer.android.com/reference/kotlin/android/net/sip/SipSession)!:the session that receives the incoming call |
| `sessionDescription` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the session description of the incoming call |

| Exceptions ||
|--------------------------------|----------------------------------------------------------------------------------------------------------|
| `android.net.sip.SipException` | if the SIP service fails to attach this object to the session or VOIP API is not supported by the device |

**See Also**

- [android.net.sip.SipManager#isVoipSupported](https://developer.android.com/reference/kotlin/android/net/sip/SipManager#isVoipSupported(android.content.Context)) 

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

Continues a call that's on hold. When succeeds, [Listener.onCallEstablished](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall.Listener#onCallEstablished(android.net.sip.SipAudioCall))is called. The attempt will be timed out if the call is not established within`timeout`seconds and [onError(SipAudioCall, SipErrorCode.TIME_OUT, String)](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall.Listener#onError(android.net.sip.SipAudioCall,%20kotlin.Int,%20kotlin.String))will be called.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the timeout value in seconds. Default value (defined by SIP protocol) is used if`timeout`is zero or negative. |

| Exceptions ||
|--------------------------------|---------------------------------------------|
| `android.net.sip.SipException` | if the SIP service fails to unhold the call |

**See Also**

- [android.net.sip.SipAudioCall.Listener#onError](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall.Listener#onError(android.net.sip.SipAudioCall,%20kotlin.Int,%20kotlin.String)) 

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
| [SipProfile](https://developer.android.com/reference/kotlin/android/net/sip/SipProfile)! | the local SIP profile |

### getPeerProfile

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPeerProfile(): SipProfile!
```

**Deprecated:** *Deprecated in Java.*

Gets the peer's SIP profile.

| Return ||
|------------------------------------------------------------------------------------------|------------------------|
| [SipProfile](https://developer.android.com/reference/kotlin/android/net/sip/SipProfile)! | the peer's SIP profile |

### getState

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getState(): Int
```

**Deprecated:** *Deprecated in Java.*

Gets the state of the [SipSession](https://developer.android.com/reference/kotlin/android/net/sip/SipSession) that carries this call. The value returned must be one of the states in [SipSession.State](https://developer.android.com/reference/kotlin/android/net/sip/SipSession.State).

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the session state |

### holdCall

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun holdCall(timeout: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Puts a call on hold. When succeeds, [Listener.onCallHeld](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall.Listener#onCallHeld(android.net.sip.SipAudioCall))is called. The attempt will be timed out if the call is not established within`timeout`seconds and [onError(SipAudioCall, SipErrorCode.TIME_OUT, String)](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall.Listener#onError(android.net.sip.SipAudioCall,%20kotlin.Int,%20kotlin.String))will be called.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the timeout value in seconds. Default value (defined by SIP protocol) is used if`timeout`is zero or negative. |

| Exceptions ||
|--------------------------------|-------------------------------------------|
| `android.net.sip.SipException` | if the SIP service fails to hold the call |

**See Also**

- [android.net.sip.SipAudioCall.Listener#onError](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall.Listener#onError(android.net.sip.SipAudioCall,%20kotlin.Int,%20kotlin.String)) 

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

Initiates an audio call to the specified profile. The attempt will be timed out if the call is not established within`timeout`seconds and [onError(SipAudioCall, SipErrorCode.TIME_OUT, String)](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall.Listener#onError(android.net.sip.SipAudioCall,%20kotlin.Int,%20kotlin.String))will be called.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `peerProfile` | [SipProfile](https://developer.android.com/reference/kotlin/android/net/sip/SipProfile)!:the SIP profile to make the call to |
| `sipSession` | [SipSession](https://developer.android.com/reference/kotlin/android/net/sip/SipSession)!:the [SipSession](https://developer.android.com/reference/kotlin/android/net/sip/SipSession) for carrying out the call |
| `timeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the timeout value in seconds. Default value (defined by SIP protocol) is used if`timeout`is zero or negative. |
| --- | --- |

| Exceptions ||
|--------------------------------|------------------------------------------------------------------------------------------------------|
| `android.net.sip.SipException` | if the SIP service fails to create a session for the call or VOIP API is not supported by the device |

**See Also**

- [android.net.sip.SipAudioCall.Listener#onError](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall.Listener#onError(android.net.sip.SipAudioCall,%20kotlin.Int,%20kotlin.String))
- [android.net.sip.SipManager#isVoipSupported](https://developer.android.com/reference/kotlin/android/net/sip/SipManager#isVoipSupported(android.content.Context)) 

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
| `result` | [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#)!:the result message to send when done |

### setListener

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setListener(listener: SipAudioCall.Listener!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the listener to listen to the audio call events. The method calls #setListener.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [SipAudioCall.Listener](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall.Listener)!:to listen to the audio call events of this object |

**See Also**

- [#setListener(Listener, boolean)](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall#setListener(android.net.sip.SipAudioCall.Listener,%20kotlin.Boolean)) 

### setListener

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setListener(
    listener: SipAudioCall.Listener!, 
    callbackImmediately: Boolean
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the listener to listen to the audio call events. A [SipAudioCall](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall#) can only hold one listener at a time. Subsequent calls to this method override the previous listener.

| Parameters ||
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [SipAudioCall.Listener](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall.Listener)!:to listen to the audio call events of this object |
| `callbackImmediately` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):set to true if the caller wants to be called back immediately on the current state |

### setSpeakerMode

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSpeakerMode(speakerMode: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Puts the device to speaker mode.

**Note:** Requires the [android.Manifest.permission#MODIFY_AUDIO_SETTINGS](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_AUDIO_SETTINGS:kotlin.String) permission.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `speakerMode` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):set true to enable speaker mode; false to disable |

### startAudio

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startAudio(): Unit
```

**Deprecated:** *Deprecated in Java.*

Starts the audio for the established call. This method should be called after [Listener.onCallEstablished](https://developer.android.com/reference/kotlin/android/net/sip/SipAudioCall.Listener#onCallEstablished(android.net.sip.SipAudioCall))is called.

**Note:** Requires the [android.Manifest.permission#RECORD_AUDIO](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#RECORD_AUDIO:kotlin.String), [android.Manifest.permission#ACCESS_WIFI_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String) and [android.Manifest.permission#WAKE_LOCK](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WAKE_LOCK:kotlin.String) permissions. 

### toggleMute

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toggleMute(): Unit
```

**Deprecated:** *Deprecated in Java.*

Toggles mute.
