# MbmsStreamingSession

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MbmsStreamingSession

Kotlin| [Java](../android/telephony/MbmsStreamingSession.md) 
| --- | --- |

```
open class MbmsStreamingSession : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.MbmsStreamingSession](../android/telephony/MbmsStreamingSession.md) |

This class provides functionality for streaming media over MBMS.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../android/telephony/MbmsStreamingSession.md))`()` Terminates this instance. |
| openstatic [MbmsStreamingSession](../android/telephony/MbmsStreamingSession.md)! | [create](../android/telephony/MbmsStreamingSession.md))`(`context:` ` [Context](../android/content/Context.md)`, `executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `callback:` ` [MbmsStreamingSessionCallback](../android/telephony/mbms/MbmsStreamingSessionCallback.md)`)` Create a new [MbmsStreamingSession](../android/telephony/MbmsStreamingSession.md) using the system default data subscription ID. |
| openstatic [MbmsStreamingSession](../android/telephony/MbmsStreamingSession.md)? | [create](../android/telephony/MbmsStreamingSession.md))`(`context:` ` [Context](../android/content/Context.md)`, `executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `subscriptionId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `callback:` ` [MbmsStreamingSessionCallback](../android/telephony/mbms/MbmsStreamingSessionCallback.md)`)` Create a new [MbmsStreamingSession](../android/telephony/MbmsStreamingSession.md) using the given subscription ID. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestUpdateStreamingServices](../android/telephony/MbmsStreamingSession.md))`(`serviceClassList:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` An inspection API to retrieve the list of streaming media currently be advertised. |
| open [StreamingService](../android/telephony/mbms/StreamingService.md)? | [startStreaming](../android/telephony/MbmsStreamingSession.md))`(`serviceInfo:` ` [StreamingServiceInfo](../android/telephony/mbms/StreamingServiceInfo.md)!`, `executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `callback:` ` [StreamingServiceCallback](../android/telephony/mbms/StreamingServiceCallback.md)!`)` Starts streaming a requested service, reporting status to the indicated callback. |

## Public methods

### close

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Terminates this instance. Also terminates any streaming services spawned from this instance as if [StreamingService.close()](../android/telephony/mbms/StreamingService.md))had been called on them. After this method returns, no further callbacks originating from the middleware will be enqueued on the provided instance of [MbmsStreamingSessionCallback](../android/telephony/mbms/MbmsStreamingSessionCallback.md), but callbacks that have already been enqueued will still be delivered. It is safe to call [create(android.content.Context,java.util.concurrent.Executor,int,android.telephony.mbms.MbmsStreamingSessionCallback)](../android/telephony/MbmsStreamingSession.md))to obtain another instance of [MbmsStreamingSession](../android/telephony/MbmsStreamingSession.md) immediately after this method returns. May throw an [IllegalStateException](../java/lang/IllegalStateException.md)

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |

### create

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun create(
    context: Context, 
    executor: Executor, 
    callback: MbmsStreamingSessionCallback
): MbmsStreamingSession!
```

Create a new [MbmsStreamingSession](../android/telephony/MbmsStreamingSession.md) using the system default data subscription ID. See [create(android.content.Context,java.util.concurrent.Executor,int,android.telephony.mbms.MbmsStreamingSessionCallback)](../android/telephony/MbmsStreamingSession.md)).

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md):This value cannot be`null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md):This value cannot be`null`. |
| `callback` | [MbmsStreamingSessionCallback](../android/telephony/mbms/MbmsStreamingSessionCallback.md):This value cannot be`null`. |
| --- | --- |

### create

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun create(
    context: Context, 
    executor: Executor, 
    subscriptionId: Int, 
    callback: MbmsStreamingSessionCallback
): MbmsStreamingSession?
```

Create a new [MbmsStreamingSession](../android/telephony/MbmsStreamingSession.md) using the given subscription ID. Note that this call will bind a remote service. You may not call this method on your app's main thread. You may only have one instance of [MbmsStreamingSession](../android/telephony/MbmsStreamingSession.md) per UID. If you call this method while there is an active instance of [MbmsStreamingSession](../android/telephony/MbmsStreamingSession.md) in your process (in other words, one that has not had [close()](../android/telephony/MbmsStreamingSession.md))called on it), this method will throw an [IllegalStateException](../java/lang/IllegalStateException.md). If you call this method in a different process running under the same UID, an error will be indicated via [MbmsStreamingSessionCallback.onError(int, String)](../android/telephony/mbms/MbmsStreamingSessionCallback.md)). Note that initialization may fail asynchronously. If you wish to try again after you receive such an asynchronous error, you must call [close()](../android/telephony/MbmsStreamingSession.md))on the instance of [MbmsStreamingSession](../android/telephony/MbmsStreamingSession.md) that you received before calling this method again.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md):The [Context](../android/content/Context.md) to use. This value cannot be`null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md):The executor on which you wish to execute callbacks. This value cannot be`null`. |
| `subscriptionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The subscription ID to use. |
| --- | --- |
| `callback` | [MbmsStreamingSessionCallback](../android/telephony/mbms/MbmsStreamingSessionCallback.md):A callback object on which you wish to receive results of asynchronous operations. This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MbmsStreamingSession](../android/telephony/MbmsStreamingSession.md)? | An instance of [MbmsStreamingSession](../android/telephony/MbmsStreamingSession.md), or null if an error occurred. |

### requestUpdateStreamingServices

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requestUpdateStreamingServices(serviceClassList: MutableList<String!>!): Unit
```

An inspection API to retrieve the list of streaming media currently be advertised. The results are returned asynchronously via [MbmsStreamingSessionCallback.onStreamingServicesUpdated(List)](../android/telephony/mbms/MbmsStreamingSessionCallback.md))on the callback provided upon creation. Multiple calls replace the list of service classes of interest. May throw an [IllegalArgumentException](../java/lang/IllegalArgumentException.md) or an [IllegalStateException](../java/lang/IllegalStateException.md).

| Parameters ||
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `serviceClassList` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:A list of streaming service classes that the app would like updates on. The exact names of these classes should be negotiated with the wireless carrier separately. |

### startStreaming

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startStreaming(
    serviceInfo: StreamingServiceInfo!, 
    executor: Executor, 
    callback: StreamingServiceCallback!
): StreamingService?
```

Starts streaming a requested service, reporting status to the indicated callback. Returns an object used to control that stream. The stream may not be ready for consumption immediately upon return from this method -- wait until the streaming state has been reported via [android.telephony.mbms.StreamingServiceCallback#onStreamStateUpdated(int, int)](../android/telephony/mbms/StreamingServiceCallback.md))May throw an [IllegalArgumentException](../java/lang/IllegalArgumentException.md) or an [IllegalStateException](../java/lang/IllegalStateException.md) Asynchronous errors through the callback include any of the errors in [MbmsErrors.GeneralErrors](../android/telephony/mbms/MbmsErrors.GeneralErrors.md) or [MbmsErrors.StreamingErrors](../android/telephony/mbms/MbmsErrors.StreamingErrors.md).

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `serviceInfo` | [StreamingServiceInfo](../android/telephony/mbms/StreamingServiceInfo.md)!:The information about the service to stream. |
| `executor` | [Executor](../java/util/concurrent/Executor.md):The executor on which you wish to execute callbacks for this stream. This value cannot be`null`. |
| `callback` | [StreamingServiceCallback](../android/telephony/mbms/StreamingServiceCallback.md)!:A callback that'll be called when something about the stream changes. |
| --- | --- |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [StreamingService](../android/telephony/mbms/StreamingService.md)? | An instance of [StreamingService](../android/telephony/mbms/StreamingService.md) through which the stream can be controlled. May be`null`if an error occurred. |
