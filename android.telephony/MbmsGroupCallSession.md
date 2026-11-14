# MbmsGroupCallSession

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MbmsGroupCallSession

Kotlin| [Java](MbmsGroupCallSession.md) 
| --- | --- |

```
open class MbmsGroupCallSession : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.MbmsGroupCallSession](MbmsGroupCallSession.md) |

This class provides functionality for accessing group call functionality over MBMS.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](MbmsGroupCallSession.md))`()` Terminates this instance. |
| openstatic [MbmsGroupCallSession](MbmsGroupCallSession.md)? | [create](MbmsGroupCallSession.md))`(`context:` ` [Context](../android.content/Context.md)`, `subscriptionId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `callback:` ` [MbmsGroupCallSessionCallback](../android.telephony.mbms/MbmsGroupCallSessionCallback.md)`)` Create a new [MbmsGroupCallSession](MbmsGroupCallSession.md) using the given subscription ID. |
| openstatic [MbmsGroupCallSession](MbmsGroupCallSession.md)? | [create](MbmsGroupCallSession.md))`(`context:` ` [Context](../android.content/Context.md)`, `executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `callback:` ` [MbmsGroupCallSessionCallback](../android.telephony.mbms/MbmsGroupCallSessionCallback.md)`)` Create a new [MbmsGroupCallSession](MbmsGroupCallSession.md) using the system default data subscription ID. |
| --- | --- |
| open [GroupCall](../android.telephony.mbms/GroupCall.md)? | [startGroupCall](MbmsGroupCallSession.md))`(`tmgi:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `saiList:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!>`, `frequencyList:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!>`, `executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `callback:` ` [GroupCallCallback](../android.telephony.mbms/GroupCallCallback.md)`)` Starts the requested group call, reporting status to the indicated callback. |

## Public methods

### close

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Terminates this instance. Also terminates any group calls spawned from this instance as if [GroupCall.close()](../android.telephony.mbms/GroupCall.md))had been called on them. After this method returns, no further callbacks originating from the middleware will be enqueued on the provided instance of [MbmsGroupCallSessionCallback](../android.telephony.mbms/MbmsGroupCallSessionCallback.md), but callbacks that have already been enqueued will still be delivered. It is safe to call [create(android.content.Context,int,java.util.concurrent.Executor,android.telephony.mbms.MbmsGroupCallSessionCallback)](MbmsGroupCallSession.md))to obtain another instance of [MbmsGroupCallSession](MbmsGroupCallSession.md) immediately after this method returns. May throw an [IllegalStateException](../java.lang/IllegalStateException.md)

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |

### create

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun create(
    context: Context, 
    subscriptionId: Int, 
    executor: Executor, 
    callback: MbmsGroupCallSessionCallback
): MbmsGroupCallSession?
```

Create a new [MbmsGroupCallSession](MbmsGroupCallSession.md) using the given subscription ID. You may only have one instance of [MbmsGroupCallSession](MbmsGroupCallSession.md) per UID. If you call this method while there is an active instance of [MbmsGroupCallSession](MbmsGroupCallSession.md) in your process (in other words, one that has not had [close()](MbmsGroupCallSession.md))called on it), this method will throw an [IllegalStateException](../java.lang/IllegalStateException.md). If you call this method in a different process running under the same UID, an error will be indicated via [MbmsGroupCallSessionCallback.onError(int, String)](../android.telephony.mbms/MbmsGroupCallSessionCallback.md)). Note that initialization may fail asynchronously. If you wish to try again after you receive such an asynchronous error, you must call [close()](MbmsGroupCallSession.md))on the instance of [MbmsGroupCallSession](MbmsGroupCallSession.md) that you received before calling this method again.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md):The [Context](../android.content/Context.md) to use. This value cannot be`null`. |
| `subscriptionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The subscription ID to use. |
| `executor` | [Executor](../java.util.concurrent/Executor.md):The executor on which you wish to execute callbacks. This value cannot be`null`. |
| --- | --- |
| `callback` | [MbmsGroupCallSessionCallback](../android.telephony.mbms/MbmsGroupCallSessionCallback.md):A callback object on which you wish to receive results of asynchronous operations. This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MbmsGroupCallSession](MbmsGroupCallSession.md)? | An instance of [MbmsGroupCallSession](MbmsGroupCallSession.md), or null if an error occurred. |

### create

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun create(
    context: Context, 
    executor: Executor, 
    callback: MbmsGroupCallSessionCallback
): MbmsGroupCallSession?
```

Create a new [MbmsGroupCallSession](MbmsGroupCallSession.md) using the system default data subscription ID. See [create(android.content.Context,int,java.util.concurrent.Executor,android.telephony.mbms.MbmsGroupCallSessionCallback)](MbmsGroupCallSession.md)).

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md):This value cannot be`null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md):This value cannot be`null`. |
| `callback` | [MbmsGroupCallSessionCallback](../android.telephony.mbms/MbmsGroupCallSessionCallback.md):This value cannot be`null`. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|--------------------------|
| [MbmsGroupCallSession](MbmsGroupCallSession.md)? | This value may be`null`. |

### startGroupCall

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startGroupCall(
    tmgi: Long, 
    saiList: MutableList<Int!>, 
    frequencyList: MutableList<Int!>, 
    executor: Executor, 
    callback: GroupCallCallback
): GroupCall?
```

Starts the requested group call, reporting status to the indicated callback. Returns an object used to control that call. May throw an [IllegalArgumentException](../java.lang/IllegalArgumentException.md) or an [IllegalStateException](../java.lang/IllegalStateException.md) Asynchronous errors through the callback include any of the errors in [MbmsErrors.GeneralErrors](../android/telephony/mbms/MbmsErrors.GeneralErrors.md).

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tmgi` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The TMGI, an identifier for the group call you want to join. |
| `saiList` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>:A list of SAIs for the group call that should be negotiated separately with the carrier. This value cannot be`null`. |
| `frequencyList` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>:A lost of frequencies for the group call that should be negotiated separately with the carrier. This value cannot be`null`. |
| --- | --- |
| `executor` | [Executor](../java.util.concurrent/Executor.md):The executor on which you wish to execute callbacks for this stream. This value cannot be`null`. |
| `callback` | [GroupCallCallback](../android.telephony.mbms/GroupCallCallback.md):The callback that you want to receive information about the call on. This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [GroupCall](../android.telephony.mbms/GroupCall.md)? | An instance of [GroupCall](../android.telephony.mbms/GroupCall.md) through which the call can be controlled. May be`null`if an error occurred. |
