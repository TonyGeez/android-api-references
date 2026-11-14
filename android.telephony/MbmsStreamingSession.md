# MbmsStreamingSession

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MbmsStreamingSession

Kotlin| [Java](https://developer.android.com/reference/android/telephony/MbmsStreamingSession "View this page in Java") 

```
open class MbmsStreamingSession : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.telephony.MbmsStreamingSession](https://developer.android.com/reference/kotlin/android/telephony/MbmsStreamingSession#) |

This class provides functionality for streaming media over MBMS.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/telephony/MbmsStreamingSession#close())`()` Terminates this instance. |
| openstatic [MbmsStreamingSession](https://developer.android.com/reference/kotlin/android/telephony/MbmsStreamingSession#)! | [create](https://developer.android.com/reference/kotlin/android/telephony/MbmsStreamingSession#create(android.content.Context,%20java.util.concurrent.Executor,%20android.telephony.mbms.MbmsStreamingSessionCallback))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [MbmsStreamingSessionCallback](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsStreamingSessionCallback)`)` Create a new [MbmsStreamingSession](https://developer.android.com/reference/kotlin/android/telephony/MbmsStreamingSession#) using the system default data subscription ID. |
| openstatic [MbmsStreamingSession](https://developer.android.com/reference/kotlin/android/telephony/MbmsStreamingSession#)? | [create](https://developer.android.com/reference/kotlin/android/telephony/MbmsStreamingSession#create(android.content.Context,%20java.util.concurrent.Executor,%20kotlin.Int,%20android.telephony.mbms.MbmsStreamingSessionCallback))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `subscriptionId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `callback:` ` [MbmsStreamingSessionCallback](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsStreamingSessionCallback)`)` Create a new [MbmsStreamingSession](https://developer.android.com/reference/kotlin/android/telephony/MbmsStreamingSession#) using the given subscription ID. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestUpdateStreamingServices](https://developer.android.com/reference/kotlin/android/telephony/MbmsStreamingSession#requestUpdateStreamingServices(kotlin.collections.MutableList))`(`serviceClassList:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` An inspection API to retrieve the list of streaming media currently be advertised. |
| open [StreamingService](https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingService)? | [startStreaming](https://developer.android.com/reference/kotlin/android/telephony/MbmsStreamingSession#startStreaming(android.telephony.mbms.StreamingServiceInfo,%20java.util.concurrent.Executor,%20android.telephony.mbms.StreamingServiceCallback))`(`serviceInfo:` ` [StreamingServiceInfo](https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingServiceInfo)!`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [StreamingServiceCallback](https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingServiceCallback)!`)` Starts streaming a requested service, reporting status to the indicated callback. |

## Public methods

### close

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Terminates this instance. Also terminates any streaming services spawned from this instance as if [StreamingService.close()](https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingService#close())had been called on them. After this method returns, no further callbacks originating from the middleware will be enqueued on the provided instance of [MbmsStreamingSessionCallback](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsStreamingSessionCallback), but callbacks that have already been enqueued will still be delivered. It is safe to call [create(android.content.Context,java.util.concurrent.Executor,int,android.telephony.mbms.MbmsStreamingSessionCallback)](https://developer.android.com/reference/kotlin/android/telephony/MbmsStreamingSession#create(android.content.Context,%20java.util.concurrent.Executor,%20kotlin.Int,%20android.telephony.mbms.MbmsStreamingSessionCallback))to obtain another instance of [MbmsStreamingSession](https://developer.android.com/reference/kotlin/android/telephony/MbmsStreamingSession#) immediately after this method returns. May throw an [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#)

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

Create a new [MbmsStreamingSession](https://developer.android.com/reference/kotlin/android/telephony/MbmsStreamingSession#) using the system default data subscription ID. See [create(android.content.Context,java.util.concurrent.Executor,int,android.telephony.mbms.MbmsStreamingSessionCallback)](https://developer.android.com/reference/kotlin/android/telephony/MbmsStreamingSession#create(android.content.Context,%20java.util.concurrent.Executor,%20kotlin.Int,%20android.telephony.mbms.MbmsStreamingSessionCallback)).

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):This value cannot be`null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):This value cannot be`null`. |
| `callback` | [MbmsStreamingSessionCallback](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsStreamingSessionCallback):This value cannot be`null`. |

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

Create a new [MbmsStreamingSession](https://developer.android.com/reference/kotlin/android/telephony/MbmsStreamingSession#) using the given subscription ID. Note that this call will bind a remote service. You may not call this method on your app's main thread. You may only have one instance of [MbmsStreamingSession](https://developer.android.com/reference/kotlin/android/telephony/MbmsStreamingSession#) per UID. If you call this method while there is an active instance of [MbmsStreamingSession](https://developer.android.com/reference/kotlin/android/telephony/MbmsStreamingSession#) in your process (in other words, one that has not had [close()](https://developer.android.com/reference/kotlin/android/telephony/MbmsStreamingSession#close())called on it), this method will throw an [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#). If you call this method in a different process running under the same UID, an error will be indicated via [MbmsStreamingSessionCallback.onError(int, String)](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsStreamingSessionCallback#onError(kotlin.Int,%20kotlin.String)). Note that initialization may fail asynchronously. If you wish to try again after you receive such an asynchronous error, you must call [close()](https://developer.android.com/reference/kotlin/android/telephony/MbmsStreamingSession#close())on the instance of [MbmsStreamingSession](https://developer.android.com/reference/kotlin/android/telephony/MbmsStreamingSession#) that you received before calling this method again.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):The [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) to use. This value cannot be`null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):The executor on which you wish to execute callbacks. This value cannot be`null`. |
| `subscriptionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The subscription ID to use. |
| `callback` | [MbmsStreamingSessionCallback](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsStreamingSessionCallback):A callback object on which you wish to receive results of asynchronous operations. This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MbmsStreamingSession](https://developer.android.com/reference/kotlin/android/telephony/MbmsStreamingSession#)? | An instance of [MbmsStreamingSession](https://developer.android.com/reference/kotlin/android/telephony/MbmsStreamingSession#), or null if an error occurred. |

### requestUpdateStreamingServices

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requestUpdateStreamingServices(serviceClassList: MutableList<String!>!): Unit
```

An inspection API to retrieve the list of streaming media currently be advertised. The results are returned asynchronously via [MbmsStreamingSessionCallback.onStreamingServicesUpdated(List)](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsStreamingSessionCallback#onStreamingServicesUpdated(kotlin.collections.MutableList))on the callback provided upon creation. Multiple calls replace the list of service classes of interest. May throw an [IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#) or an [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#).

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

Starts streaming a requested service, reporting status to the indicated callback. Returns an object used to control that stream. The stream may not be ready for consumption immediately upon return from this method -- wait until the streaming state has been reported via [android.telephony.mbms.StreamingServiceCallback#onStreamStateUpdated(int, int)](https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingServiceCallback#onStreamStateUpdated(kotlin.Int,%20kotlin.Int))May throw an [IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#) or an [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#) Asynchronous errors through the callback include any of the errors in [MbmsErrors.GeneralErrors](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors.GeneralErrors) or [MbmsErrors.StreamingErrors](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors.StreamingErrors).

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `serviceInfo` | [StreamingServiceInfo](https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingServiceInfo)!:The information about the service to stream. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):The executor on which you wish to execute callbacks for this stream. This value cannot be`null`. |
| `callback` | [StreamingServiceCallback](https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingServiceCallback)!:A callback that'll be called when something about the stream changes. |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [StreamingService](https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingService)? | An instance of [StreamingService](https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingService) through which the stream can be controlled. May be`null`if an error occurred. |
