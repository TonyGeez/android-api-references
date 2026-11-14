# MessageQueue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MessageQueue

Kotlin| [Java](MessageQueue.md) 
| --- | --- |

```
class MessageQueue
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.MessageQueue](MessageQueue.md) |

Low-level class holding the list of messages to be dispatched by a [Looper](Looper.md). Messages are not added directly to a MessageQueue, but rather through [Handler](Handler.md) objects associated with the Looper.

You can retrieve the MessageQueue for the current thread with [Looper.myQueue()](Looper.md)).

## Summary

| Nested classes ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [IdleHandler](../android/os/MessageQueue.IdleHandler.md) Callback interface for discovering when a thread is going to block waiting for more messages. |
| abstract | [OnFileDescriptorEventListener](../android/os/MessageQueue.OnFileDescriptorEventListener.md) A listener which is invoked when file descriptor related events occur. |

| Public methods ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addIdleHandler](MessageQueue.md))`(`handler:` ` [MessageQueue.IdleHandler](../android/os/MessageQueue.IdleHandler.md)`)` Add a new [IdleHandler](../android/os/MessageQueue.IdleHandler.md) to this message queue. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addOnFileDescriptorEventListener](MessageQueue.md))`(`fd:` ` [FileDescriptor](../java.io/FileDescriptor.md)`, `events:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `listener:` ` [MessageQueue.OnFileDescriptorEventListener](../android/os/MessageQueue.OnFileDescriptorEventListener.md)`)` Adds a file descriptor listener to receive notification when file descriptor related events occur. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isIdle](MessageQueue.md))`()` Returns true if the looper has no pending messages which are due to be processed and is not blocked on a sync barrier. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeIdleHandler](MessageQueue.md))`(`handler:` ` [MessageQueue.IdleHandler](../android/os/MessageQueue.IdleHandler.md)`)` Remove an [IdleHandler](../android/os/MessageQueue.IdleHandler.md) from the queue that was previously added with [addIdleHandler](MessageQueue.md)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeOnFileDescriptorEventListener](MessageQueue.md))`(`fd:` ` [FileDescriptor](../java.io/FileDescriptor.md)`)` Removes a file descriptor listener. |

| Protected methods ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](MessageQueue.md))`()` <br /> |

## Public methods

### addIdleHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addIdleHandler(handler: MessageQueue.IdleHandler): Unit
```

Add a new [IdleHandler](../android/os/MessageQueue.IdleHandler.md) to this message queue. This may be removed automatically for you by returning false from [IdleHandler.queueIdle()](../android/os/MessageQueue.IdleHandler.md))when it is invoked, or explicitly removing it with [removeIdleHandler](MessageQueue.md)).

This method is safe to call from any thread.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `handler` | [MessageQueue.IdleHandler](../android/os/MessageQueue.IdleHandler.md):The IdleHandler to be added. This value cannot be`null`. |

### addOnFileDescriptorEventListener

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addOnFileDescriptorEventListener(
    fd: FileDescriptor, 
    events: Int, 
    listener: MessageQueue.OnFileDescriptorEventListener
): Unit
```

Adds a file descriptor listener to receive notification when file descriptor related events occur.

If the file descriptor has already been registered, the specified events and listener will replace any that were previously associated with it. It is not possible to set more than one listener per file descriptor.

It is important to always unregister the listener when the file descriptor is no longer of use.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fd` | [FileDescriptor](../java.io/FileDescriptor.md):The file descriptor for which a listener will be registered. This value cannot be`null`. |
| `events` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The set of events to receive: a combination of the [OnFileDescriptorEventListener.EVENT_INPUT](../android/os/MessageQueue.OnFileDescriptorEventListener.md), [OnFileDescriptorEventListener.EVENT_OUTPUT](../android/os/MessageQueue.OnFileDescriptorEventListener.md), and [OnFileDescriptorEventListener.EVENT_ERROR](../android/os/MessageQueue.OnFileDescriptorEventListener.md) event masks. If the requested set of events is zero, then the listener is unregistered. Value is either`0`or a combination of [android.os.MessageQueue.OnFileDescriptorEventListener#EVENT_INPUT](../android/os/MessageQueue.OnFileDescriptorEventListener.md), [android.os.MessageQueue.OnFileDescriptorEventListener#EVENT_OUTPUT](../android/os/MessageQueue.OnFileDescriptorEventListener.md), and [android.os.MessageQueue.OnFileDescriptorEventListener#EVENT_ERROR](../android/os/MessageQueue.OnFileDescriptorEventListener.md) |
| `listener` | [MessageQueue.OnFileDescriptorEventListener](../android/os/MessageQueue.OnFileDescriptorEventListener.md):The listener to invoke when file descriptor events occur. This value cannot be`null`. |
| --- | --- |

**See Also**

- [android.os.MessageQueue.OnFileDescriptorEventListener](../android/os/MessageQueue.OnFileDescriptorEventListener.md)
- [#removeOnFileDescriptorEventListener](MessageQueue.md)) 

### isIdle

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isIdle(): Boolean
```

Returns true if the looper has no pending messages which are due to be processed and is not blocked on a sync barrier.

This method is safe to call from any thread.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the looper is idle. |

### removeIdleHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeIdleHandler(handler: MessageQueue.IdleHandler): Unit
```

Remove an [IdleHandler](../android/os/MessageQueue.IdleHandler.md) from the queue that was previously added with [addIdleHandler](MessageQueue.md)). If the given object is not currently in the idle list, nothing is done.

This method is safe to call from any thread.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `handler` | [MessageQueue.IdleHandler](../android/os/MessageQueue.IdleHandler.md):The IdleHandler to be removed. This value cannot be`null`. |

### removeOnFileDescriptorEventListener

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeOnFileDescriptorEventListener(fd: FileDescriptor): Unit
```

Removes a file descriptor listener.

This method does nothing if no listener has been registered for the specified file descriptor.

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fd` | [FileDescriptor](../java.io/FileDescriptor.md):The file descriptor whose listener will be unregistered. This value cannot be`null`. |

**See Also**

- [android.os.MessageQueue.OnFileDescriptorEventListener](../android/os/MessageQueue.OnFileDescriptorEventListener.md)
- [#addOnFileDescriptorEventListener](MessageQueue.md))

## Protected methods

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
