# MbmsGroupCallSession

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MbmsGroupCallSession

Kotlin| [Java](https://developer.android.com/reference/android/telephony/MbmsGroupCallSession "View this page in Java") 
| --- | --- |

```
open class MbmsGroupCallSession : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.MbmsGroupCallSession](https://developer.android.com/reference/kotlin/android/telephony/MbmsGroupCallSession#) |

This class provides functionality for accessing group call functionality over MBMS.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/telephony/MbmsGroupCallSession#close())`()` Terminates this instance. |
| openstatic [MbmsGroupCallSession](https://developer.android.com/reference/kotlin/android/telephony/MbmsGroupCallSession#)? | [create](https://developer.android.com/reference/kotlin/android/telephony/MbmsGroupCallSession#create(android.content.Context,%20kotlin.Int,%20java.util.concurrent.Executor,%20android.telephony.mbms.MbmsGroupCallSessionCallback))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`, `subscriptionId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [MbmsGroupCallSessionCallback](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsGroupCallSessionCallback)`)` Create a new [MbmsGroupCallSession](https://developer.android.com/reference/kotlin/android/telephony/MbmsGroupCallSession#) using the given subscription ID. |
| openstatic [MbmsGroupCallSession](https://developer.android.com/reference/kotlin/android/telephony/MbmsGroupCallSession#)? | [create](https://developer.android.com/reference/kotlin/android/telephony/MbmsGroupCallSession#create(android.content.Context,%20java.util.concurrent.Executor,%20android.telephony.mbms.MbmsGroupCallSessionCallback))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [MbmsGroupCallSessionCallback](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsGroupCallSessionCallback)`)` Create a new [MbmsGroupCallSession](https://developer.android.com/reference/kotlin/android/telephony/MbmsGroupCallSession#) using the system default data subscription ID. |
| --- | --- |
| open [GroupCall](https://developer.android.com/reference/kotlin/android/telephony/mbms/GroupCall)? | [startGroupCall](https://developer.android.com/reference/kotlin/android/telephony/MbmsGroupCallSession#startGroupCall(kotlin.Long,%20kotlin.collections.MutableList,%20kotlin.collections.MutableList,%20java.util.concurrent.Executor,%20android.telephony.mbms.GroupCallCallback))`(`tmgi:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `saiList:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!>`, `frequencyList:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!>`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [GroupCallCallback](https://developer.android.com/reference/kotlin/android/telephony/mbms/GroupCallCallback)`)` Starts the requested group call, reporting status to the indicated callback. |

## Public methods

### close

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Terminates this instance. Also terminates any group calls spawned from this instance as if [GroupCall.close()](https://developer.android.com/reference/kotlin/android/telephony/mbms/GroupCall#close())had been called on them. After this method returns, no further callbacks originating from the middleware will be enqueued on the provided instance of [MbmsGroupCallSessionCallback](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsGroupCallSessionCallback), but callbacks that have already been enqueued will still be delivered. It is safe to call [create(android.content.Context,int,java.util.concurrent.Executor,android.telephony.mbms.MbmsGroupCallSessionCallback)](https://developer.android.com/reference/kotlin/android/telephony/MbmsGroupCallSession#create(android.content.Context,%20kotlin.Int,%20java.util.concurrent.Executor,%20android.telephony.mbms.MbmsGroupCallSessionCallback))to obtain another instance of [MbmsGroupCallSession](https://developer.android.com/reference/kotlin/android/telephony/MbmsGroupCallSession#) immediately after this method returns. May throw an [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#)

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

Create a new [MbmsGroupCallSession](https://developer.android.com/reference/kotlin/android/telephony/MbmsGroupCallSession#) using the given subscription ID. You may only have one instance of [MbmsGroupCallSession](https://developer.android.com/reference/kotlin/android/telephony/MbmsGroupCallSession#) per UID. If you call this method while there is an active instance of [MbmsGroupCallSession](https://developer.android.com/reference/kotlin/android/telephony/MbmsGroupCallSession#) in your process (in other words, one that has not had [close()](https://developer.android.com/reference/kotlin/android/telephony/MbmsGroupCallSession#close())called on it), this method will throw an [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#). If you call this method in a different process running under the same UID, an error will be indicated via [MbmsGroupCallSessionCallback.onError(int, String)](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsGroupCallSessionCallback#onError(kotlin.Int,%20kotlin.String)). Note that initialization may fail asynchronously. If you wish to try again after you receive such an asynchronous error, you must call [close()](https://developer.android.com/reference/kotlin/android/telephony/MbmsGroupCallSession#close())on the instance of [MbmsGroupCallSession](https://developer.android.com/reference/kotlin/android/telephony/MbmsGroupCallSession#) that you received before calling this method again.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):The [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) to use. This value cannot be`null`. |
| `subscriptionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The subscription ID to use. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):The executor on which you wish to execute callbacks. This value cannot be`null`. |
| --- | --- |
| `callback` | [MbmsGroupCallSessionCallback](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsGroupCallSessionCallback):A callback object on which you wish to receive results of asynchronous operations. This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MbmsGroupCallSession](https://developer.android.com/reference/kotlin/android/telephony/MbmsGroupCallSession#)? | An instance of [MbmsGroupCallSession](https://developer.android.com/reference/kotlin/android/telephony/MbmsGroupCallSession#), or null if an error occurred. |

### create

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun create(
    context: Context, 
    executor: Executor, 
    callback: MbmsGroupCallSessionCallback
): MbmsGroupCallSession?
```

Create a new [MbmsGroupCallSession](https://developer.android.com/reference/kotlin/android/telephony/MbmsGroupCallSession#) using the system default data subscription ID. See [create(android.content.Context,int,java.util.concurrent.Executor,android.telephony.mbms.MbmsGroupCallSessionCallback)](https://developer.android.com/reference/kotlin/android/telephony/MbmsGroupCallSession#create(android.content.Context,%20kotlin.Int,%20java.util.concurrent.Executor,%20android.telephony.mbms.MbmsGroupCallSessionCallback)).

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):This value cannot be`null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):This value cannot be`null`. |
| `callback` | [MbmsGroupCallSessionCallback](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsGroupCallSessionCallback):This value cannot be`null`. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|--------------------------|
| [MbmsGroupCallSession](https://developer.android.com/reference/kotlin/android/telephony/MbmsGroupCallSession#)? | This value may be`null`. |

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

Starts the requested group call, reporting status to the indicated callback. Returns an object used to control that call. May throw an [IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#) or an [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#) Asynchronous errors through the callback include any of the errors in [MbmsErrors.GeneralErrors](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors.GeneralErrors).

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tmgi` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The TMGI, an identifier for the group call you want to join. |
| `saiList` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>:A list of SAIs for the group call that should be negotiated separately with the carrier. This value cannot be`null`. |
| `frequencyList` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>:A lost of frequencies for the group call that should be negotiated separately with the carrier. This value cannot be`null`. |
| --- | --- |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):The executor on which you wish to execute callbacks for this stream. This value cannot be`null`. |
| `callback` | [GroupCallCallback](https://developer.android.com/reference/kotlin/android/telephony/mbms/GroupCallCallback):The callback that you want to receive information about the call on. This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [GroupCall](https://developer.android.com/reference/kotlin/android/telephony/mbms/GroupCall)? | An instance of [GroupCall](https://developer.android.com/reference/kotlin/android/telephony/mbms/GroupCall) through which the call can be controlled. May be`null`if an error occurred. |
