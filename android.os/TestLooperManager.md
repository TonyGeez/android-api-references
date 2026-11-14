# TestLooperManager

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TestLooperManager

Kotlin| [Java](https://developer.android.com/reference/android/os/TestLooperManager "View this page in Java") 
| --- | --- |

```
open class TestLooperManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.TestLooperManager](https://developer.android.com/reference/kotlin/android/os/TestLooperManager#) |

Blocks a looper from executing any messages, and allows the holder of this object to control when and which messages get executed until it is released.

A TestLooperManager should be acquired using [android.app.Instrumentation#acquireLooperManager](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#acquireLooperManager(android.os.Looper)). Until [release()](https://developer.android.com/reference/kotlin/android/os/TestLooperManager#release())is called, the Looper thread will not execute any messages except when [execute(android.os.Message)](https://developer.android.com/reference/kotlin/android/os/TestLooperManager#execute(android.os.Message))is called. The test code may use [next()](https://developer.android.com/reference/kotlin/android/os/TestLooperManager#next())to acquire messages that have been queued to this [Looper](https://developer.android.com/reference/kotlin/android/os/Looper)/ [MessageQueue](https://developer.android.com/reference/kotlin/android/os/MessageQueue) and then [execute](https://developer.android.com/reference/kotlin/android/os/TestLooperManager#execute(android.os.Message))to run any that desires.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [execute](https://developer.android.com/reference/kotlin/android/os/TestLooperManager#execute(android.os.Message))`(`message:` ` [Message](https://developer.android.com/reference/kotlin/android/os/Message)!`)` Executes the given message on the Looper thread this wrapper is attached to. |
| open [MessageQueue](https://developer.android.com/reference/kotlin/android/os/MessageQueue)! | [getMessageQueue](https://developer.android.com/reference/kotlin/android/os/TestLooperManager#getMessageQueue())`()` Returns the [MessageQueue](https://developer.android.com/reference/kotlin/android/os/MessageQueue) this object is wrapping. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasMessages](https://developer.android.com/reference/kotlin/android/os/TestLooperManager#hasMessages(android.os.Handler,%20kotlin.Any,%20kotlin.Int))`(`h:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler)!`, `object:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `what:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns true if there are any queued messages that match the parameters. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasMessages](https://developer.android.com/reference/kotlin/android/os/TestLooperManager#hasMessages(android.os.Handler,%20kotlin.Any,%20java.lang.Runnable))`(`h:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler)!`, `object:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `r:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`)` Returns true if there are any queued messages that match the parameters. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBlockedOnSyncBarrier](https://developer.android.com/reference/kotlin/android/os/TestLooperManager#isBlockedOnSyncBarrier())`()` Checks whether the Looper is currently blocked on a sync barrier. |
| open [Message](https://developer.android.com/reference/kotlin/android/os/Message)! | [next](https://developer.android.com/reference/kotlin/android/os/TestLooperManager#next())`()` Returns the next message that should be executed by this queue, may block if no messages are ready. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)? | [peekWhen](https://developer.android.com/reference/kotlin/android/os/TestLooperManager#peekWhen())`()` Retrieves, but does not remove, the values of android. |
| open [Message](https://developer.android.com/reference/kotlin/android/os/Message)? | [poll](https://developer.android.com/reference/kotlin/android/os/TestLooperManager#poll())`()` Retrieves and removes the next message in this queue. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [recycle](https://developer.android.com/reference/kotlin/android/os/TestLooperManager#recycle(android.os.Message))`(`msg:` ` [Message](https://developer.android.com/reference/kotlin/android/os/Message)!`)` Called to indicate that a Message returned by [next()](https://developer.android.com/reference/kotlin/android/os/TestLooperManager#next())has been parsed and should be recycled. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](https://developer.android.com/reference/kotlin/android/os/TestLooperManager#release())`()` Releases the looper to continue standard looping and processing of messages, no further interactions with TestLooperManager will be allowed after release() has been called. |

## Public methods

### execute

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun execute(message: Message!): Unit
```

Executes the given message on the Looper thread this wrapper is attached to.

Execution will happen on the Looper's thread (whether it is the current thread or not), but all RuntimeExceptions encountered while executing the message will be thrown on the calling thread. 

### getMessageQueue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMessageQueue(): MessageQueue!
```

Returns the [MessageQueue](https://developer.android.com/reference/kotlin/android/os/MessageQueue) this object is wrapping. 

### hasMessages

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasMessages(
    h: Handler!, 
    object: Any!, 
    what: Int
): Boolean
```

Returns true if there are any queued messages that match the parameters.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `h` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler)!:the value of [Message.getTarget()](https://developer.android.com/reference/kotlin/android/os/Message#getTarget()) |
| `what` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value of [Message.what](https://developer.android.com/reference/kotlin/android/os/Message#what:kotlin.Int) |
| `object` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the value of [Message.obj](https://developer.android.com/reference/kotlin/android/os/Message#obj:kotlin.Any), null for any |
| --- | --- |

### hasMessages

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasMessages(
    h: Handler!, 
    object: Any!, 
    r: Runnable!
): Boolean
```

Returns true if there are any queued messages that match the parameters.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `h` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler)!:the value of [Message.getTarget()](https://developer.android.com/reference/kotlin/android/os/Message#getTarget()) |
| `r` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!:the value of [Message.getCallback()](https://developer.android.com/reference/kotlin/android/os/Message#getCallback()) |
| `object` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the value of [Message.obj](https://developer.android.com/reference/kotlin/android/os/Message#obj:kotlin.Any), null for any |
| --- | --- |

### isBlockedOnSyncBarrier

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isBlockedOnSyncBarrier(): Boolean
```

Checks whether the Looper is currently blocked on a sync barrier. 

### next

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun next(): Message!
```

Returns the next message that should be executed by this queue, may block if no messages are ready.

Callers should always call [recycle(android.os.Message)](https://developer.android.com/reference/kotlin/android/os/TestLooperManager#recycle(android.os.Message))on the message when all interactions with it have completed. 

### peekWhen

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun peekWhen(): Long?
```

Retrieves, but does not remove, the values of android.os.Message#when of next message in the queue. If the queue is empty, returns null. This method never blocks. 

### poll

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun poll(): Message?
```

Retrieves and removes the next message in this queue. If the queue is empty, returns null. This method never blocks.

Callers should always call [recycle(android.os.Message)](https://developer.android.com/reference/kotlin/android/os/TestLooperManager#recycle(android.os.Message))on the message when all interactions with it have completed. 

### recycle

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun recycle(msg: Message!): Unit
```

Called to indicate that a Message returned by [next()](https://developer.android.com/reference/kotlin/android/os/TestLooperManager#next())has been parsed and should be recycled. 

### release

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun release(): Unit
```

Releases the looper to continue standard looping and processing of messages, no further interactions with TestLooperManager will be allowed after release() has been called.
