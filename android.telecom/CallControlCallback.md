# CallControlCallback

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CallControlCallback

Kotlin| [Java](../android/telecom/CallControlCallback.md) 
| --- | --- |

```
interface CallControlCallback
```

| [android.telecom.CallControlCallback](../android/telecom/CallControlCallback.md) |

CallControlCallback relays call updates (that require a response) from the Telecom framework out to the application.This can include operations which the app must implement on a Call due to the presence of other calls on the device, requests relayed from a Bluetooth device, or from another calling surface.

All CallControlCallbacks are transactional, meaning that a client must complete the [Consumer](../java/util/function/Consumer.md) via [Consumer.accept(Object)](../java/util/function/Consumer.md))in order to complete the CallControlCallbacks. If a CallControlCallbacks can be completed, the [Consumer.accept(Object)](../java/util/function/Consumer.md))should be called with [Boolean.TRUE](../java/lang/Boolean.md). Otherwise, [Consumer.accept(Object)](../java/util/function/Consumer.md))should be called with [Boolean.FALSE](../java/lang/Boolean.md) to represent the CallControlCallbacks cannot be completed on the client side.

Note: Each CallEventCallback has a timeout of 5000 milliseconds. Failing to complete the [Consumer](../java/util/function/Consumer.md) before the timeout will result in a failed transaction.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAnswer](../android/telecom/CallControlCallback.md))`(`videoState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `wasCompleted:` ` [Consumer](../java/util/function/Consumer.md)< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!>`)` Telecom is informing the client to answer an incoming call and set it to active. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCallStreamingStarted](../android/telecom/CallControlCallback.md))`(`wasCompleted:` ` [Consumer](../java/util/function/Consumer.md)< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!>`)` Telecom is informing the client to set the call in streaming. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDisconnect](../android/telecom/CallControlCallback.md))`(`disconnectCause:` ` [DisconnectCause](../android/telecom/DisconnectCause.md)`, `wasCompleted:` ` [Consumer](../java/util/function/Consumer.md)< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!>`)` Telecom is informing the client to disconnect the call |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSetActive](../android/telecom/CallControlCallback.md))`(`wasCompleted:` ` [Consumer](../java/util/function/Consumer.md)< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!>`)` Telecom is informing the client to set the call active |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSetInactive](../android/telecom/CallControlCallback.md))`(`wasCompleted:` ` [Consumer](../java/util/function/Consumer.md)< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!>`)` Telecom is informing the client to set the call inactive. |

## Public methods

### onAnswer

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onAnswer(
    videoState: Int, 
    wasCompleted: Consumer<Boolean!>
): Unit
```

Telecom is informing the client to answer an incoming call and set it to active.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `videoState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the video state Value is [android.telecom.CallAttributes#AUDIO_CALL](../android/telecom/CallAttributes.md), or [android.telecom.CallAttributes#VIDEO_CALL](../android/telecom/CallAttributes.md) |
| `wasCompleted` | [Consumer](../java/util/function/Consumer.md)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\>:The [Consumer](../java/util/function/Consumer.md) to be completed. If the client can answer the call on their end, [Consumer.accept(Object)](../java/util/function/Consumer.md))should be called with [Boolean.TRUE](../java/lang/Boolean.md). Otherwise, [Consumer.accept(Object)](../java/util/function/Consumer.md))should be called with [Boolean.FALSE](../java/lang/Boolean.md). However, Telecom will still disconnect the call and remove it from tracking. This value cannot be`null`. |

### onCallStreamingStarted

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onCallStreamingStarted(wasCompleted: Consumer<Boolean!>): Unit
```

Telecom is informing the client to set the call in streaming.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `wasCompleted` | [Consumer](../java/util/function/Consumer.md)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\>:The [Consumer](../java/util/function/Consumer.md) to be completed. If the client can stream the call on their end, [Consumer.accept(Object)](../java/util/function/Consumer.md))should be called with [Boolean.TRUE](../java/lang/Boolean.md). Otherwise, [Consumer.accept(Object)](../java/util/function/Consumer.md))should be called with [Boolean.FALSE](../java/lang/Boolean.md). This value cannot be`null`. |

### onDisconnect

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDisconnect(
    disconnectCause: DisconnectCause, 
    wasCompleted: Consumer<Boolean!>
): Unit
```

Telecom is informing the client to disconnect the call

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `disconnectCause` | [DisconnectCause](../android/telecom/DisconnectCause.md):represents the cause for disconnecting the call. This value cannot be`null`. |
| `wasCompleted` | [Consumer](../java/util/function/Consumer.md)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\>:The [Consumer](../java/util/function/Consumer.md) to be completed. If the client can disconnect the call on their end, [Consumer.accept(Object)](../java/util/function/Consumer.md))should be called with [Boolean.TRUE](../java/lang/Boolean.md). Otherwise, [Consumer.accept(Object)](../java/util/function/Consumer.md))should be called with [Boolean.FALSE](../java/lang/Boolean.md). However, Telecom will still disconnect the call and remove it from tracking. This value cannot be`null`. |

### onSetActive

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSetActive(wasCompleted: Consumer<Boolean!>): Unit
```

Telecom is informing the client to set the call active

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `wasCompleted` | [Consumer](../java/util/function/Consumer.md)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\>:The [Consumer](../java/util/function/Consumer.md) to be completed. If the client can set the call active on their end, the [Consumer.accept(Object)](../java/util/function/Consumer.md))should be called with [Boolean.TRUE](../java/lang/Boolean.md). Otherwise, [Consumer.accept(Object)](../java/util/function/Consumer.md))should be called with [Boolean.FALSE](../java/lang/Boolean.md). Telecom will effectively ignore the remote setActive request and the call will remain in whatever state it is in. This value cannot be`null`. |

### onSetInactive

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSetInactive(wasCompleted: Consumer<Boolean!>): Unit
```

Telecom is informing the client to set the call inactive. This is the same as holding a call for two endpoints but can be extended to setting a meeting inactive.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `wasCompleted` | [Consumer](../java/util/function/Consumer.md)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\>:The [Consumer](../java/util/function/Consumer.md) to be completed. If the client can set the call inactive on their end, the [Consumer.accept(Object)](../java/util/function/Consumer.md))should be called with [Boolean.TRUE](../java/lang/Boolean.md). Otherwise, [Consumer.accept(Object)](../java/util/function/Consumer.md))should be called with [Boolean.FALSE](../java/lang/Boolean.md). Telecom will effectively ignore the remote setInactive request and the call will remain in whatever state it is in. This value cannot be`null`. |
