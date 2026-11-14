# SipSession

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SipSession

Kotlin| [Java](SipSession.md) 
| --- | --- |

```
class SipSession
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.sip.SipSession](SipSession.md) |

| **This class was deprecated in API level 31.**
|
| [android.net.sip.SipManager](SipManager.md) and associated classes are no longer supported and should not be used as the basis of future VOIP apps.

Represents a SIP session that is associated with a SIP dialog or a standalone transaction not within a dialog.

You can get a [SipSession](SipSession.md) from [SipManager](SipManager.md) with [createSipSession()](SipManager.md))(when initiating calls) or [getSessionFor()](SipManager.md))(when receiving calls).

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Listener](../android/net/sip/SipSession.Listener.md) Listener for events relating to a SIP session, such as when a session is being registered ("on registering") or a call is outgoing ("on calling"). |
| | [State](../android/net/sip/SipSession.State.md) Defines SIP session states, such as "registering", "outgoing call", and "in call". |

| Public methods ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [answerCall](SipSession.md))`(`sessionDescription:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Answers an incoming call with the specified session description. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [changeCall](SipSession.md))`(`sessionDescription:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Changes the session description during a call. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endCall](SipSession.md))`()` Ends an established call, terminates an outgoing call or rejects an incoming call. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getCallId](SipSession.md))`()` Gets the call ID of the session. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getLocalIp](SipSession.md))`()` Gets the IP address of the local host on which this SIP session runs. |
| [SipProfile](SipProfile.md)! | [getLocalProfile](SipSession.md))`()` Gets the SIP profile that this session is associated with. |
| --- | --- |
| [SipProfile](SipProfile.md)! | [getPeerProfile](SipSession.md))`()` Gets the SIP profile that this session is connected to. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getState](SipSession.md))`()` Gets the session state. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInCall](SipSession.md))`()` Checks if the session is in a call. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [makeCall](SipSession.md))`(`callee:` ` [SipProfile](SipProfile.md)!`, `sessionDescription:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Initiates a call to the specified profile. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [register](SipSession.md))`(`duration:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Performs registration to the server specified by the associated local profile. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setListener](SipSession.md))`(`listener:` ` [SipSession.Listener](../android/net/sip/SipSession.Listener.md)!`)` Sets the listener to listen to the session events. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregister](SipSession.md))`()` Performs unregistration to the server specified by the associated local profile. |

## Public methods

### answerCall

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun answerCall(
    sessionDescription: String!, 
    timeout: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Answers an incoming call with the specified session description. The method is only valid to call when the session state is in [State.INCOMING_CALL](../android/net/sip/SipSession.State.md).

| Parameters ||
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sessionDescription` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the session description to answer this call |
| `timeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the session will be timed out if the call is not established within`timeout`seconds. Default value (defined by SIP protocol) is used if`timeout`is zero or negative. |

### changeCall

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun changeCall(
    sessionDescription: String!, 
    timeout: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Changes the session description during a call. The method is only valid to call when the session state is in [State.IN_CALL](../android/net/sip/SipSession.State.md).

| Parameters ||
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sessionDescription` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the new session description |
| `timeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the session will be timed out if the call is not established within`timeout`seconds. Default value (defined by SIP protocol) is used if`timeout`is zero or negative. |

### endCall

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun endCall(): Unit
```

**Deprecated:** *Deprecated in Java.*

Ends an established call, terminates an outgoing call or rejects an incoming call. The method is only valid to call when the session state is in [State.IN_CALL](../android/net/sip/SipSession.State.md), [State.INCOMING_CALL](../android/net/sip/SipSession.State.md), [State.OUTGOING_CALL](../android/net/sip/SipSession.State.md) or [State.OUTGOING_CALL_RING_BACK](../android/net/sip/SipSession.State.md). 

### getCallId

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCallId(): String!
```

**Deprecated:** *Deprecated in Java.*

Gets the call ID of the session.

| Return ||
|-----------------------------------------------------------------------------------|-------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the call ID |

### getLocalIp

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLocalIp(): String!
```

**Deprecated:** *Deprecated in Java.*

Gets the IP address of the local host on which this SIP session runs.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the IP address of the local host |

### getLocalProfile

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLocalProfile(): SipProfile!
```

**Deprecated:** *Deprecated in Java.*

Gets the SIP profile that this session is associated with.

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------------|
| [SipProfile](SipProfile.md)! | the SIP profile that this session is associated with |

### getPeerProfile

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPeerProfile(): SipProfile!
```

**Deprecated:** *Deprecated in Java.*

Gets the SIP profile that this session is connected to. Only available when the session is associated with a SIP dialog.

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------------------|
| [SipProfile](SipProfile.md)! | the SIP profile that this session is connected to |

### getState

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getState(): Int
```

**Deprecated:** *Deprecated in Java.*

Gets the session state. The value returned must be one of the states in [State](../android/net/sip/SipSession.State.md).

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the session state |

### isInCall

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isInCall(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Checks if the session is in a call.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the session is in a call |

### makeCall

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun makeCall(
    callee: SipProfile!, 
    sessionDescription: String!, 
    timeout: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Initiates a call to the specified profile. The session listener is called back upon defined session events. The method is only valid to call when the session state is in [State.READY_TO_CALL](../android/net/sip/SipSession.State.md).

| Parameters ||
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callee` | [SipProfile](SipProfile.md)!:the SIP profile to make the call to |
| `sessionDescription` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the session description of this call |
| `timeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the session will be timed out if the call is not established within`timeout`seconds. Default value (defined by SIP protocol) is used if`timeout`is zero or negative. |
| --- | --- |

**See Also**

- [android.net.sip.SipSession.Listener](../android/net/sip/SipSession.Listener.md) 

### register

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun register(duration: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Performs registration to the server specified by the associated local profile. The session listener is called back upon success or failure of registration. The method is only valid to call when the session state is in [State.READY_TO_CALL](../android/net/sip/SipSession.State.md).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------|
| `duration` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):duration in second before the registration expires |

**See Also**

- [android.net.sip.SipSession.Listener](../android/net/sip/SipSession.Listener.md) 

### setListener

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setListener(listener: SipSession.Listener!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the listener to listen to the session events. A`SipSession`can only hold one listener at a time. Subsequent calls to this method override the previous listener.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [SipSession.Listener](../android/net/sip/SipSession.Listener.md)!:to listen to the session events of this object |

### unregister

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unregister(): Unit
```

**Deprecated:** *Deprecated in Java.*

Performs unregistration to the server specified by the associated local profile. Unregistration is technically the same as registration with zero expiration duration. The session listener is called back upon success or failure of unregistration. The method is only valid to call when the session state is in [State.READY_TO_CALL](../android/net/sip/SipSession.State.md). 
**See Also**

- [android.net.sip.SipSession.Listener](../android/net/sip/SipSession.Listener.md)
