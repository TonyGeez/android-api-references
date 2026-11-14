# RemoteConference

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RemoteConference

Kotlin| [Java](RemoteConference.md) 
| --- | --- |

```
class RemoteConference
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telecom.RemoteConference](RemoteConference.md) |

A conference provided to a [ConnectionService](ConnectionService.md) by another`ConnectionService`through [ConnectionService.conferenceRemoteConnections](ConnectionService.md)). Once created, a`RemoteConference`can be used to control the conference call or monitor changes through [RemoteConnection.Callback](../android/telecom/RemoteConnection.Callback.md).

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Callback](../android/telecom/RemoteConference.Callback.md) Callback base class for [RemoteConference](RemoteConference.md). |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [disconnect](RemoteConference.md))`()` Disconnects the conference call as well as the child [RemoteConnection](RemoteConnection.md) s. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [RemoteConnection](RemoteConnection.md)!\>! | [getConferenceableConnections](RemoteConference.md))`()` Returns a list of independent connections that can me merged with this conference. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getConnectionCapabilities](RemoteConference.md))`()` Returns the capabilities of the conference. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getConnectionProperties](RemoteConference.md))`()` Returns the properties of the conference. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [RemoteConnection](RemoteConnection.md)!\>! | [getConnections](RemoteConference.md))`()` Returns the list of [RemoteConnection](RemoteConnection.md) s contained in this conference. |
| [DisconnectCause](DisconnectCause.md)! | [getDisconnectCause](RemoteConference.md))`()` Returns the [DisconnectCause](DisconnectCause.md) for the conference if it is in the state [Connection.STATE_DISCONNECTED](Connection.md). |
| --- | --- |
| [Bundle](../android.os/Bundle.md)! | [getExtras](RemoteConference.md))`()` Obtain the extras associated with this`RemoteConnection`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getState](RemoteConference.md))`()` Gets the state of the conference call. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [hold](RemoteConference.md))`()` Puts the conference on hold. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [merge](RemoteConference.md))`()` Merges all [RemoteConnection](RemoteConnection.md) s of this conference into a single call. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [playDtmfTone](RemoteConference.md))`(`digit:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Requests that the conference start playing the specified DTMF tone. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerCallback](RemoteConference.md))`(`callback:` ` [RemoteConference.Callback](../android/telecom/RemoteConference.Callback.md)!`)` Register a callback through which to receive state updates for this conference. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerCallback](RemoteConference.md))`(`callback:` ` [RemoteConference.Callback](../android/telecom/RemoteConference.Callback.md)!`, `handler:` ` [Handler](../android.os/Handler.md)!`)` Registers a callback through which to receive state updates for this conference. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [separate](RemoteConference.md))`(`connection:` ` [RemoteConnection](RemoteConnection.md)!`)` Removes the specified [RemoteConnection](RemoteConnection.md) from the conference. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCallAudioState](RemoteConference.md))`(`state:` ` [CallAudioState](CallAudioState.md)!`)` Request to change the conference's audio routing to the specified state. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopDtmfTone](RemoteConference.md))`()` Stops the most recent request to play a DTMF tone. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [swap](RemoteConference.md))`()` Swaps the active audio stream between the conference's child [RemoteConnection](RemoteConnection.md) s. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unhold](RemoteConference.md))`()` Unholds the conference call. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterCallback](RemoteConference.md))`(`callback:` ` [RemoteConference.Callback](../android/telecom/RemoteConference.Callback.md)!`)` Unregisters a previously registered callback. |

## Public methods

### disconnect

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun disconnect(): Unit
```

Disconnects the conference call as well as the child [RemoteConnection](RemoteConnection.md) s. 

### getConferenceableConnections

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConferenceableConnections(): MutableList<RemoteConnection!>!
```

Returns a list of independent connections that can me merged with this conference.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [RemoteConnection](RemoteConnection.md)!>! | A list of conferenceable connections. |

### getConnectionCapabilities

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConnectionCapabilities(): Int
```

Returns the capabilities of the conference. See`CAPABILITY_*`constants in class [Connection](Connection.md) for valid values.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A bitmask of the capabilities of the conference call. |

### getConnectionProperties

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConnectionProperties(): Int
```

Returns the properties of the conference. See`PROPERTY_*`constants in class [Connection](Connection.md) for valid values.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A bitmask of the properties of the conference call. |

### getConnections

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConnections(): MutableList<RemoteConnection!>!
```

Returns the list of [RemoteConnection](RemoteConnection.md) s contained in this conference.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [RemoteConnection](RemoteConnection.md)!>! | A list of child connections. |

### getDisconnectCause

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisconnectCause(): DisconnectCause!
```

Returns the [DisconnectCause](DisconnectCause.md) for the conference if it is in the state [Connection.STATE_DISCONNECTED](Connection.md). If the conference is not disconnected, this will return null.

| Return ||
|----------------------------------------------------------------------------------------------------|-----------------------|
| [DisconnectCause](DisconnectCause.md)! | The disconnect cause. |

### getExtras

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExtras(): Bundle!
```

Obtain the extras associated with this`RemoteConnection`.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------|
| [Bundle](../android.os/Bundle.md)! | The extras for this connection. |

### getState

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getState(): Int
```

Gets the state of the conference call. See [Connection](Connection.md) for valid values.

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

Merges all [RemoteConnection](RemoteConnection.md) s of this conference into a single call. This should be invoked only if the conference contains the capability [Connection.CAPABILITY_MERGE_CONFERENCE](Connection.md), otherwise it is a no-op. The presence of said capability indicates that the connections of this conference, despite being part of the same conference object, are yet to have their audio streams merged; this is a common pattern for CDMA conference calls, but the capability is not used for GSM and SIP conference calls. Invoking this method will cause the unmerged child connections to merge their audio streams. 

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
| `callback` | [RemoteConference.Callback](../android/telecom/RemoteConference.Callback.md)!:The callback to notify of state changes. |

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
| `callback` | [RemoteConference.Callback](../android/telecom/RemoteConference.Callback.md)!:The callback to notify of state changes. |
| `handler` | [Handler](../android.os/Handler.md)!:The handler on which to execute the callbacks. |

### separate

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun separate(connection: RemoteConnection!): Unit
```

Removes the specified [RemoteConnection](RemoteConnection.md) from the conference. This causes the [RemoteConnection](RemoteConnection.md) to become a standalone connection. This is a no-op if the [RemoteConnection](RemoteConnection.md) does not belong to this conference.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `connection` | [RemoteConnection](RemoteConnection.md)!:The remote-connection to remove. |

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

- [#playDtmfTone](RemoteConference.md)) 

### swap

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun swap(): Unit
```

Swaps the active audio stream between the conference's child [RemoteConnection](RemoteConnection.md) s. This should be invoked only if the conference contains the capability [Connection.CAPABILITY_SWAP_CONFERENCE](Connection.md), otherwise it is a no-op. This is only used by [ConnectionService](ConnectionService.md) s that create conferences for connections that do not yet have their audio streams merged; this is a common pattern for CDMA conference calls, but the capability is not used for GSM and SIP conference calls. Invoking this method will change the active audio stream to a different child connection. 

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
| `callback` | [RemoteConference.Callback](../android/telecom/RemoteConference.Callback.md)!:The callback to unregister. |

**See Also**
