# CallControl

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CallControl

Kotlin| [Java](CallControl.md) 
| --- | --- |

```
class CallControl
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telecom.CallControl](CallControl.md) |

CallControl provides client side control of a call. Each Call will get an individual CallControl instance in which the client can alter the state of the associated call. Outgoing and incoming calls should move to active (via [CallControl.setActive(Executor, OutcomeReceiver)](CallControl.md))or answered (via [CallControl.answer(int, Executor, OutcomeReceiver)](CallControl.md))before 60 seconds. If the new call is not moved to active or answered before 60 seconds, the call will be disconnected.

Each method is Transactional meaning that it can succeed or fail. If a transaction succeeds, the [OutcomeReceiver.onResult](../android.os/OutcomeReceiver.md))will be called by Telecom. Otherwise, the [OutcomeReceiver.onError](../android.os/OutcomeReceiver.md))is called and provides a [CallException](CallException.md) that details why the operation failed.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [answer](CallControl.md))`(`videoState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `callback:` ` [OutcomeReceiver](../android.os/OutcomeReceiver.md)< [Void](../java.lang/Void.md)!,` ` [CallException](CallException.md)!>`)` Request Telecom answer an incoming call. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [disconnect](CallControl.md))`(`disconnectCause:` ` [DisconnectCause](DisconnectCause.md)`, `executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `callback:` ` [OutcomeReceiver](../android.os/OutcomeReceiver.md)< [Void](../java.lang/Void.md)!,` ` [CallException](CallException.md)!>`)` Request Telecom disconnect the call and remove the call from telecom tracking. |
| [ParcelUuid](../android.os/ParcelUuid.md) | [getCallId](CallControl.md))`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestCallEndpointChange](CallControl.md))`(`callEndpoint:` ` [CallEndpoint](CallEndpoint.md)`, `executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `callback:` ` [OutcomeReceiver](../android.os/OutcomeReceiver.md)< [Void](../java.lang/Void.md)!,` ` [CallException](CallException.md)!>`)` Request a CallEndpoint change. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestMuteState](CallControl.md))`(`isMuted:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `callback:` ` [OutcomeReceiver](../android.os/OutcomeReceiver.md)< [Void](../java.lang/Void.md)!,` ` [CallException](CallException.md)!>`)` Request a new mute state. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestVideoState](CallControl.md))`(`videoState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `callback:` ` [OutcomeReceiver](../android.os/OutcomeReceiver.md)< [Void](../java.lang/Void.md)!,` ` [CallException](CallException.md)!>`)` Request a new video state for the ongoing call. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendEvent](CallControl.md))`(`event:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `extras:` ` [Bundle](../android.os/Bundle.md)`)` Raises an event to the [android.telecom.InCallService](InCallService.md) implementations tracking this call via [android.telecom.Call.Callback#onConnectionEvent(Call, String, Bundle)](../android/telecom/Call.Callback.md)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setActive](CallControl.md))`(`executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `callback:` ` [OutcomeReceiver](../android.os/OutcomeReceiver.md)< [Void](../java.lang/Void.md)!,` ` [CallException](CallException.md)!>`)` Request Telecom set the call state to active. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInactive](CallControl.md))`(`executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `callback:` ` [OutcomeReceiver](../android.os/OutcomeReceiver.md)< [Void](../java.lang/Void.md)!,` ` [CallException](CallException.md)!>`)` Request Telecom set the call state to inactive. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startCallStreaming](CallControl.md))`(`executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `callback:` ` [OutcomeReceiver](../android.os/OutcomeReceiver.md)< [Void](../java.lang/Void.md)!,` ` [CallException](CallException.md)!>`)` Request start a call streaming session. |

## Public methods

### answer

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun answer(
    videoState: Int, 
    executor: Executor, 
    callback: OutcomeReceiver<Void!, CallException!>
): Unit
```

Request Telecom answer an incoming call. For outgoing calls and calls that have been placed on hold, use [CallControl.setActive(Executor, OutcomeReceiver)](CallControl.md)).

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `videoState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):to report to Telecom. Telecom will store VideoState in the event another service/device requests it in order to continue the call on another screen. Value is [android.telecom.CallAttributes#AUDIO_CALL](CallAttributes.md), or [android.telecom.CallAttributes#VIDEO_CALL](CallAttributes.md) |
| `executor` | [Executor](../java.util.concurrent/Executor.md):The [Executor](../java.util.concurrent/Executor.md) on which the [OutcomeReceiver](../android.os/OutcomeReceiver.md) callback will be called on. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. This value cannot be`null`. |
| `callback` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [Void](../java.lang/Void.md)!, [CallException](CallException.md)!\>:that will be completed on the Telecom side that details success or failure of the requested operation. [OutcomeReceiver.onResult](../android.os/OutcomeReceiver.md))will be called if Telecom has successfully switched the call state to active [OutcomeReceiver.onError](../android.os/OutcomeReceiver.md))will be called if Telecom has failed to set the call state to active. A [CallException](CallException.md) will be passed that details why the operation failed. This value cannot be`null`. |
| --- | --- |

### disconnect

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun disconnect(
    disconnectCause: DisconnectCause, 
    executor: Executor, 
    callback: OutcomeReceiver<Void!, CallException!>
): Unit
```

Request Telecom disconnect the call and remove the call from telecom tracking.

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `disconnectCause` | [DisconnectCause](DisconnectCause.md):represents the cause for disconnecting the call. The only valid codes for the [android.telecom.DisconnectCause](DisconnectCause.md) passed in are: - [DisconnectCause.LOCAL](DisconnectCause.md) - [DisconnectCause.REMOTE](DisconnectCause.md) - [DisconnectCause.REJECTED](DisconnectCause.md) - [DisconnectCause.MISSED](DisconnectCause.md) This value cannot be`null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md):The [Executor](../java.util.concurrent/Executor.md) on which the [OutcomeReceiver](../android.os/OutcomeReceiver.md) callback will be called on. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. This value cannot be`null`. |
| `callback` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [Void](../java.lang/Void.md)!, [CallException](CallException.md)!\>:That will be completed on the Telecom side that details success or failure of the requested operation. [OutcomeReceiver.onResult](../android.os/OutcomeReceiver.md))will be called if Telecom has successfully disconnected the call. [OutcomeReceiver.onError](../android.os/OutcomeReceiver.md))will be called if Telecom has failed to disconnect the call. A [CallException](CallException.md) will be passed that details why the operation failed. Note: After the call has been successfully disconnected, calling any CallControl API will result in the [OutcomeReceiver.onError](../android.os/OutcomeReceiver.md))with [CallException.CODE_CALL_IS_NOT_BEING_TRACKED](CallException.md). This value cannot be`null`. |
| --- | --- |

### getCallId

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCallId(): ParcelUuid
```

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [ParcelUuid](../android.os/ParcelUuid.md) | the callId Telecom assigned to this CallControl object which should be attached to an individual call. This value cannot be`null`. |

### requestCallEndpointChange

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun requestCallEndpointChange(
    callEndpoint: CallEndpoint, 
    executor: Executor, 
    callback: OutcomeReceiver<Void!, CallException!>
): Unit
```

Request a CallEndpoint change. Clients should not define their own CallEndpoint when requesting a change. Instead, the new endpoint should be one of the valid endpoints provided by [CallEventCallback.onAvailableCallEndpointsChanged(List)](CallEventCallback.md)).

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callEndpoint` | [CallEndpoint](CallEndpoint.md):The [CallEndpoint](CallEndpoint.md) to change to. This value cannot be`null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md):The [Executor](../java.util.concurrent/Executor.md) on which the [OutcomeReceiver](../android.os/OutcomeReceiver.md) callback will be called on. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. This value cannot be`null`. |
| `callback` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [Void](../java.lang/Void.md)!, [CallException](CallException.md)!\>:The [OutcomeReceiver](../android.os/OutcomeReceiver.md) that will be completed on the Telecom side that details success or failure of the requested operation. [OutcomeReceiver.onResult](../android.os/OutcomeReceiver.md))will be called if Telecom has successfully changed the CallEndpoint that was requested. [OutcomeReceiver.onError](../android.os/OutcomeReceiver.md))will be called if Telecom has failed to switch to the requested CallEndpoint. A [CallException](CallException.md) will be passed that details why the operation failed. This value cannot be`null`. |
| --- | --- |

### requestMuteState

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun requestMuteState(
    isMuted: Boolean, 
    executor: Executor, 
    callback: OutcomeReceiver<Void!, CallException!>
): Unit
```

Request a new mute state. Note: [CallEventCallback.onMuteStateChanged(boolean)](CallEventCallback.md))will be called every time the mute state is changed and can be used to track the current mute state.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `isMuted` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):The new mute state. Passing in a [Boolean.TRUE](../java.lang/Boolean.md) for the isMuted parameter will mute the call. [Boolean.FALSE](../java.lang/Boolean.md) will unmute the call. |
| `executor` | [Executor](../java.util.concurrent/Executor.md):The [Executor](../java.util.concurrent/Executor.md) on which the [OutcomeReceiver](../android.os/OutcomeReceiver.md) callback will be called on. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. This value cannot be`null`. |
| `callback` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [Void](../java.lang/Void.md)!, [CallException](CallException.md)!\>:The [OutcomeReceiver](../android.os/OutcomeReceiver.md) that will be completed on the Telecom side that details success or failure of the requested operation. [OutcomeReceiver.onResult](../android.os/OutcomeReceiver.md))will be called if Telecom has successfully changed the mute state. [OutcomeReceiver.onError](../android.os/OutcomeReceiver.md))will be called if Telecom has failed to switch to the mute state. A [CallException](CallException.md) will be passed that details why the operation failed. This value cannot be`null`. |
| --- | --- |

### requestVideoState

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun requestVideoState(
    videoState: Int, 
    executor: Executor, 
    callback: OutcomeReceiver<Void!, CallException!>
): Unit
```

Request a new video state for the ongoing call. This can only be changed if the application has registered a [PhoneAccount](PhoneAccount.md) with the [PhoneAccount.CAPABILITY_SUPPORTS_VIDEO_CALLING](PhoneAccount.md) and set the [CallAttributes.SUPPORTS_VIDEO_CALLING](CallAttributes.md) when adding the call via [TelecomManager.addCall(CallAttributes, Executor, OutcomeReceiver,](TelecomManager.md))

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `videoState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):to report to Telecom. To see the valid argument to pass, see android.telecom.CallAttributes.CallType. Value is [android.telecom.CallAttributes#AUDIO_CALL](CallAttributes.md), or [android.telecom.CallAttributes#VIDEO_CALL](CallAttributes.md) |
| `executor` | [Executor](../java.util.concurrent/Executor.md):The [Executor](../java.util.concurrent/Executor.md) on which the [OutcomeReceiver](../android.os/OutcomeReceiver.md) callback will be called on. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. This value cannot be`null`. |
| `callback` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [Void](../java.lang/Void.md)!, [CallException](CallException.md)!\>:that will be completed on the Telecom side that details success or failure of the requested operation. [OutcomeReceiver.onResult](../android.os/OutcomeReceiver.md))will be called if Telecom has successfully switched the video state. [OutcomeReceiver.onError](../android.os/OutcomeReceiver.md))will be called if Telecom has failed to set the new video state. A [CallException](CallException.md) will be passed that details why the operation failed. This value cannot be`null`. |
| --- | --- |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the argument passed for videoState is invalid. To see a list of valid states, see android.telecom.CallAttributes.CallType. |

### sendEvent

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun sendEvent(
    event: String, 
    extras: Bundle
): Unit
```

Raises an event to the [android.telecom.InCallService](InCallService.md) implementations tracking this call via [android.telecom.Call.Callback#onConnectionEvent(Call, String, Bundle)](../android/telecom/Call.Callback.md)). These events and the associated extra keys for the`Bundle`parameter are mutually defined by a VoIP application and [android.telecom.InCallService](InCallService.md). This API is used to relay additional information about a call other than what is specified in the [android.telecom.CallAttributes](CallAttributes.md) to [android.telecom.InCallService](InCallService.md) s. This might include, for example, a change to the list of participants in a meeting, or the name of the speakers who have their hand raised. Where appropriate, the [InCallService](InCallService.md) s tracking this call may choose to render this additional information about the call. An automotive calling UX, for example may have enough screen real estate to indicate the number of participants in a meeting, but to prevent distractions could suppress the list of participants.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a string event identifier agreed upon between a VoIP application and an [android.telecom.InCallService](InCallService.md) This value cannot be`null`. |
| `extras` | [Bundle](../android.os/Bundle.md):a [android.os.Bundle](../android.os/Bundle.md) containing information about the event, as agreed upon between a VoIP application and [android.telecom.InCallService](InCallService.md). This value cannot be`null`. |

### setActive

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setActive(
    executor: Executor, 
    callback: OutcomeReceiver<Void!, CallException!>
): Unit
```

Request Telecom set the call state to active. This method should be called when either an outgoing call is ready to go active or a held call is ready to go active again. For incoming calls that are ready to be answered, use [CallControl.answer(int, Executor, OutcomeReceiver)](CallControl.md)).

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java.util.concurrent/Executor.md):The [Executor](../java.util.concurrent/Executor.md) on which the [OutcomeReceiver](../android.os/OutcomeReceiver.md) callback will be called on. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. This value cannot be`null`. |
| `callback` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [Void](../java.lang/Void.md)!, [CallException](CallException.md)!\>:that will be completed on the Telecom side that details success or failure of the requested operation. [OutcomeReceiver.onResult](../android.os/OutcomeReceiver.md))will be called if Telecom has successfully switched the call state to active [OutcomeReceiver.onError](../android.os/OutcomeReceiver.md))will be called if Telecom has failed to set the call state to active. A [CallException](CallException.md) will be passed that details why the operation failed. This value cannot be`null`. |

### setInactive

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setInactive(
    executor: Executor, 
    callback: OutcomeReceiver<Void!, CallException!>
): Unit
```

Request Telecom set the call state to inactive. This the same as hold for two call endpoints but can be extended to setting a meeting to inactive.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java.util.concurrent/Executor.md):The [Executor](../java.util.concurrent/Executor.md) on which the [OutcomeReceiver](../android.os/OutcomeReceiver.md) callback will be called on. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. This value cannot be`null`. |
| `callback` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [Void](../java.lang/Void.md)!, [CallException](CallException.md)!\>:that will be completed on the Telecom side that details success or failure of the requested operation. [OutcomeReceiver.onResult](../android.os/OutcomeReceiver.md))will be called if Telecom has successfully switched the call state to inactive [OutcomeReceiver.onError](../android.os/OutcomeReceiver.md))will be called if Telecom has failed to set the call state to inactive. A [CallException](CallException.md) will be passed that details why the operation failed. This value cannot be`null`. |

### startCallStreaming

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun startCallStreaming(
    executor: Executor, 
    callback: OutcomeReceiver<Void!, CallException!>
): Unit
```

Request start a call streaming session. On receiving valid request, telecom will bind to the`CallStreamingService`implemented by a general call streaming sender. So that the call streaming sender can perform streaming local device audio to another remote device and control the call during streaming.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java.util.concurrent/Executor.md):The [Executor](../java.util.concurrent/Executor.md) on which the [OutcomeReceiver](../android.os/OutcomeReceiver.md) callback will be called on. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. This value cannot be`null`. |
| `callback` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [Void](../java.lang/Void.md)!, [CallException](CallException.md)!\>:that will be completed on the Telecom side that details success or failure of the requested operation. [OutcomeReceiver.onResult](../android.os/OutcomeReceiver.md))will be called if Telecom has successfully started the call streaming. [OutcomeReceiver.onError](../android.os/OutcomeReceiver.md))will be called if Telecom has failed to start the call streaming. A [CallException](CallException.md) will be passed that details why the operation failed. This value cannot be`null`. |
