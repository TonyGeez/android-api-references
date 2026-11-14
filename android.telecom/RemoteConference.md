# RemoteConference

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RemoteConference

Kotlin| [Java](https://developer.android.com/reference/android/telecom/RemoteConference "View this page in Java") 
| --- | --- |

```
class RemoteConference
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telecom.RemoteConference](https://developer.android.com/reference/kotlin/android/telecom/RemoteConference#) |

A conference provided to a [ConnectionService](https://developer.android.com/reference/kotlin/android/telecom/ConnectionService) by another`ConnectionService`through [ConnectionService.conferenceRemoteConnections](https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#conferenceRemoteConnections(android.telecom.RemoteConnection,%20android.telecom.RemoteConnection)). Once created, a`RemoteConference`can be used to control the conference call or monitor changes through [RemoteConnection.Callback](https://developer.android.com/reference/kotlin/android/telecom/RemoteConnection.Callback).

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Callback](https://developer.android.com/reference/kotlin/android/telecom/RemoteConference.Callback) Callback base class for [RemoteConference](https://developer.android.com/reference/kotlin/android/telecom/RemoteConference#). |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [disconnect](https://developer.android.com/reference/kotlin/android/telecom/RemoteConference#disconnect())`()` Disconnects the conference call as well as the child [RemoteConnection](https://developer.android.com/reference/kotlin/android/telecom/RemoteConnection) s. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [RemoteConnection](https://developer.android.com/reference/kotlin/android/telecom/RemoteConnection)!\>! | [getConferenceableConnections](https://developer.android.com/reference/kotlin/android/telecom/RemoteConference#getConferenceableConnections())`()` Returns a list of independent connections that can me merged with this conference. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getConnectionCapabilities](https://developer.android.com/reference/kotlin/android/telecom/RemoteConference#getConnectionCapabilities())`()` Returns the capabilities of the conference. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getConnectionProperties](https://developer.android.com/reference/kotlin/android/telecom/RemoteConference#getConnectionProperties())`()` Returns the properties of the conference. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [RemoteConnection](https://developer.android.com/reference/kotlin/android/telecom/RemoteConnection)!\>! | [getConnections](https://developer.android.com/reference/kotlin/android/telecom/RemoteConference#getConnections())`()` Returns the list of [RemoteConnection](https://developer.android.com/reference/kotlin/android/telecom/RemoteConnection) s contained in this conference. |
| [DisconnectCause](https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause)! | [getDisconnectCause](https://developer.android.com/reference/kotlin/android/telecom/RemoteConference#getDisconnectCause())`()` Returns the [DisconnectCause](https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause) for the conference if it is in the state [Connection.STATE_DISCONNECTED](https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_DISCONNECTED:kotlin.Int). |
| --- | --- |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | [getExtras](https://developer.android.com/reference/kotlin/android/telecom/RemoteConference#getExtras())`()` Obtain the extras associated with this`RemoteConnection`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getState](https://developer.android.com/reference/kotlin/android/telecom/RemoteConference#getState())`()` Gets the state of the conference call. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [hold](https://developer.android.com/reference/kotlin/android/telecom/RemoteConference#hold())`()` Puts the conference on hold. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [merge](https://developer.android.com/reference/kotlin/android/telecom/RemoteConference#merge())`()` Merges all [RemoteConnection](https://developer.android.com/reference/kotlin/android/telecom/RemoteConnection) s of this conference into a single call. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [playDtmfTone](https://developer.android.com/reference/kotlin/android/telecom/RemoteConference#playDtmfTone(kotlin.Char))`(`digit:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Requests that the conference start playing the specified DTMF tone. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerCallback](https://developer.android.com/reference/kotlin/android/telecom/RemoteConference#registerCallback(android.telecom.RemoteConference.Callback))`(`callback:` ` [RemoteConference.Callback](https://developer.android.com/reference/kotlin/android/telecom/RemoteConference.Callback)!`)` Register a callback through which to receive state updates for this conference. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerCallback](https://developer.android.com/reference/kotlin/android/telecom/RemoteConference#registerCallback(android.telecom.RemoteConference.Callback,%20android.os.Handler))`(`callback:` ` [RemoteConference.Callback](https://developer.android.com/reference/kotlin/android/telecom/RemoteConference.Callback)!`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!`)` Registers a callback through which to receive state updates for this conference. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [separate](https://developer.android.com/reference/kotlin/android/telecom/RemoteConference#separate(android.telecom.RemoteConnection))`(`connection:` ` [RemoteConnection](https://developer.android.com/reference/kotlin/android/telecom/RemoteConnection)!`)` Removes the specified [RemoteConnection](https://developer.android.com/reference/kotlin/android/telecom/RemoteConnection) from the conference. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCallAudioState](https://developer.android.com/reference/kotlin/android/telecom/RemoteConference#setCallAudioState(android.telecom.CallAudioState))`(`state:` ` [CallAudioState](https://developer.android.com/reference/kotlin/android/telecom/CallAudioState)!`)` Request to change the conference's audio routing to the specified state. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopDtmfTone](https://developer.android.com/reference/kotlin/android/telecom/RemoteConference#stopDtmfTone())`()` Stops the most recent request to play a DTMF tone. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [swap](https://developer.android.com/reference/kotlin/android/telecom/RemoteConference#swap())`()` Swaps the active audio stream between the conference's child [RemoteConnection](https://developer.android.com/reference/kotlin/android/telecom/RemoteConnection) s. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unhold](https://developer.android.com/reference/kotlin/android/telecom/RemoteConference#unhold())`()` Unholds the conference call. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterCallback](https://developer.android.com/reference/kotlin/android/telecom/RemoteConference#unregisterCallback(android.telecom.RemoteConference.Callback))`(`callback:` ` [RemoteConference.Callback](https://developer.android.com/reference/kotlin/android/telecom/RemoteConference.Callback)!`)` Unregisters a previously registered callback. |

## Public methods

### disconnect

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun disconnect(): Unit
```

Disconnects the conference call as well as the child [RemoteConnection](https://developer.android.com/reference/kotlin/android/telecom/RemoteConnection) s. 

### getConferenceableConnections

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConferenceableConnections(): MutableList<RemoteConnection!>!
```

Returns a list of independent connections that can me merged with this conference.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [RemoteConnection](https://developer.android.com/reference/kotlin/android/telecom/RemoteConnection)!>! | A list of conferenceable connections. |

### getConnectionCapabilities

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConnectionCapabilities(): Int
```

Returns the capabilities of the conference. See`CAPABILITY_*`constants in class [Connection](https://developer.android.com/reference/kotlin/android/telecom/Connection) for valid values.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A bitmask of the capabilities of the conference call. |

### getConnectionProperties

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConnectionProperties(): Int
```

Returns the properties of the conference. See`PROPERTY_*`constants in class [Connection](https://developer.android.com/reference/kotlin/android/telecom/Connection) for valid values.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A bitmask of the properties of the conference call. |

### getConnections

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConnections(): MutableList<RemoteConnection!>!
```

Returns the list of [RemoteConnection](https://developer.android.com/reference/kotlin/android/telecom/RemoteConnection) s contained in this conference.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [RemoteConnection](https://developer.android.com/reference/kotlin/android/telecom/RemoteConnection)!>! | A list of child connections. |

### getDisconnectCause

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisconnectCause(): DisconnectCause!
```

Returns the [DisconnectCause](https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause) for the conference if it is in the state [Connection.STATE_DISCONNECTED](https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_DISCONNECTED:kotlin.Int). If the conference is not disconnected, this will return null.

| Return ||
|----------------------------------------------------------------------------------------------------|-----------------------|
| [DisconnectCause](https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause)! | The disconnect cause. |

### getExtras

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExtras(): Bundle!
```

Obtain the extras associated with this`RemoteConnection`.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | The extras for this connection. |

### getState

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getState(): Int
```

Gets the state of the conference call. See [Connection](https://developer.android.com/reference/kotlin/android/telecom/Connection) for valid values.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A constant representing the state the conference call is currently in. |

### hold

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hold(): Unit
```

Puts the conference on hold. 

### merge

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun merge(): Unit
```

Merges all [RemoteConnection](https://developer.android.com/reference/kotlin/android/telecom/RemoteConnection) s of this conference into a single call. This should be invoked only if the conference contains the capability [Connection.CAPABILITY_MERGE_CONFERENCE](https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_MERGE_CONFERENCE:kotlin.Int), otherwise it is a no-op. The presence of said capability indicates that the connections of this conference, despite being part of the same conference object, are yet to have their audio streams merged; this is a common pattern for CDMA conference calls, but the capability is not used for GSM and SIP conference calls. Invoking this method will cause the unmerged child connections to merge their audio streams. 

### playDtmfTone

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun playDtmfTone(digit: Char): Unit
```

Requests that the conference start playing the specified DTMF tone.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------|
| `digit` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):The digit for which to play a DTMF tone. |

### registerCallback

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun registerCallback(callback: RemoteConference.Callback!): Unit
```

Register a callback through which to receive state updates for this conference.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [RemoteConference.Callback](https://developer.android.com/reference/kotlin/android/telecom/RemoteConference.Callback)!:The callback to notify of state changes. |

### registerCallback

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun registerCallback(
    callback: RemoteConference.Callback!, 
    handler: Handler!
): Unit
```

Registers a callback through which to receive state updates for this conference. Callbacks will be notified using the specified handler, if provided.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [RemoteConference.Callback](https://developer.android.com/reference/kotlin/android/telecom/RemoteConference.Callback)!:The callback to notify of state changes. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!:The handler on which to execute the callbacks. |

### separate

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun separate(connection: RemoteConnection!): Unit
```

Removes the specified [RemoteConnection](https://developer.android.com/reference/kotlin/android/telecom/RemoteConnection) from the conference. This causes the [RemoteConnection](https://developer.android.com/reference/kotlin/android/telecom/RemoteConnection) to become a standalone connection. This is a no-op if the [RemoteConnection](https://developer.android.com/reference/kotlin/android/telecom/RemoteConnection) does not belong to this conference.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `connection` | [RemoteConnection](https://developer.android.com/reference/kotlin/android/telecom/RemoteConnection)!:The remote-connection to remove. |

### setCallAudioState

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setCallAudioState(state: CallAudioState!): Unit
```

Request to change the conference's audio routing to the specified state. The specified state can include audio routing (Bluetooth, Speaker, etc) and muting state. 

### stopDtmfTone

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun stopDtmfTone(): Unit
```

Stops the most recent request to play a DTMF tone. 
**See Also**

- [#playDtmfTone](https://developer.android.com/reference/kotlin/android/telecom/RemoteConference#playDtmfTone(kotlin.Char)) 

### swap

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun swap(): Unit
```

Swaps the active audio stream between the conference's child [RemoteConnection](https://developer.android.com/reference/kotlin/android/telecom/RemoteConnection) s. This should be invoked only if the conference contains the capability [Connection.CAPABILITY_SWAP_CONFERENCE](https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_SWAP_CONFERENCE:kotlin.Int), otherwise it is a no-op. This is only used by [ConnectionService](https://developer.android.com/reference/kotlin/android/telecom/ConnectionService) s that create conferences for connections that do not yet have their audio streams merged; this is a common pattern for CDMA conference calls, but the capability is not used for GSM and SIP conference calls. Invoking this method will change the active audio stream to a different child connection. 

### unhold

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unhold(): Unit
```

Unholds the conference call. 

### unregisterCallback

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unregisterCallback(callback: RemoteConference.Callback!): Unit
```

Unregisters a previously registered callback.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [RemoteConference.Callback](https://developer.android.com/reference/kotlin/android/telecom/RemoteConference.Callback)!:The callback to unregister. |

**See Also**
