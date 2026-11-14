# TestLooperManager

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TestLooperManager

Kotlin| [Java](../android/os/TestLooperManager.md) 
| --- | --- |

```
open class TestLooperManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.TestLooperManager](../android/os/TestLooperManager.md) |

Blocks a looper from executing any messages, and allows the holder of this object to control when and which messages get executed until it is released.

A TestLooperManager should be acquired using [android.app.Instrumentation#acquireLooperManager](../android/app/Instrumentation.md)). Until [release()](../android/os/TestLooperManager.md))is called, the Looper thread will not execute any messages except when [execute(android.os.Message)](../android/os/TestLooperManager.md))is called. The test code may use [next()](../android/os/TestLooperManager.md))to acquire messages that have been queued to this [Looper](../android/os/Looper.md)/ [MessageQueue](../android/os/MessageQueue.md) and then [execute](../android/os/TestLooperManager.md))to run any that desires.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [execute](../android/os/TestLooperManager.md))`(`message:` ` [Message](../android/os/Message.md)!`)` Executes the given message on the Looper thread this wrapper is attached to. |
| open [MessageQueue](../android/os/MessageQueue.md)! | [getMessageQueue](../android/os/TestLooperManager.md))`()` Returns the [MessageQueue](../android/os/MessageQueue.md) this object is wrapping. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasMessages](../android/os/TestLooperManager.md))`(`h:` ` [Handler](../android/os/Handler.md)!`, `object:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `what:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns true if there are any queued messages that match the parameters. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasMessages](../android/os/TestLooperManager.md))`(`h:` ` [Handler](../android/os/Handler.md)!`, `object:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `r:` ` [Runnable](../java/lang/Runnable.md)!`)` Returns true if there are any queued messages that match the parameters. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBlockedOnSyncBarrier](../android/os/TestLooperManager.md))`()` Checks whether the Looper is currently blocked on a sync barrier. |
| open [Message](../android/os/Message.md)! | [next](../android/os/TestLooperManager.md))`()` Returns the next message that should be executed by this queue, may block if no messages are ready. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)? | [peekWhen](../android/os/TestLooperManager.md))`()` Retrieves, but does not remove, the values of android. |
| open [Message](../android/os/Message.md)? | [poll](../android/os/TestLooperManager.md))`()` Retrieves and removes the next message in this queue. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [recycle](../android/os/TestLooperManager.md))`(`msg:` ` [Message](../android/os/Message.md)!`)` Called to indicate that a Message returned by [next()](../android/os/TestLooperManager.md))has been parsed and should be recycled. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](../android/os/TestLooperManager.md))`()` Releases the looper to continue standard looping and processing of messages, no further interactions with TestLooperManager will be allowed after release() has been called. |

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

Returns the [MessageQueue](../android/os/MessageQueue.md) this object is wrapping. 

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
| `h` | [Handler](../android/os/Handler.md)!:the value of [Message.getTarget()](../android/os/Message.md)) |
| `what` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value of [Message.what](../android/os/Message.md) |
| `object` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the value of [Message.obj](../android/os/Message.md), null for any |
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
| `h` | [Handler](../android/os/Handler.md)!:the value of [Message.getTarget()](../android/os/Message.md)) |
| `r` | [Runnable](../java/lang/Runnable.md)!:the value of [Message.getCallback()](../android/os/Message.md)) |
| `object` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the value of [Message.obj](../android/os/Message.md), null for any |
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

Callers should always call [recycle(android.os.Message)](../android/os/TestLooperManager.md))on the message when all interactions with it have completed. 

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

Callers should always call [recycle(android.os.Message)](../android/os/TestLooperManager.md))on the message when all interactions with it have completed. 

### recycle

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun recycle(msg: Message!): Unit
```

Called to indicate that a Message returned by [next()](../android/os/TestLooperManager.md))has been parsed and should be recycled. 

### release

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun release(): Unit
```

Releases the looper to continue standard looping and processing of messages, no further interactions with TestLooperManager will be allowed after release() has been called.
