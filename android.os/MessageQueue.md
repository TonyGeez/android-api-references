# MessageQueue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MessageQueue

Kotlin| [Java](https://developer.android.com/reference/android/os/MessageQueue "View this page in Java") 
| --- | --- |

```
class MessageQueue
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.MessageQueue](https://developer.android.com/reference/kotlin/android/os/MessageQueue#) |

Low-level class holding the list of messages to be dispatched by a [Looper](https://developer.android.com/reference/kotlin/android/os/Looper). Messages are not added directly to a MessageQueue, but rather through [Handler](https://developer.android.com/reference/kotlin/android/os/Handler) objects associated with the Looper.

You can retrieve the MessageQueue for the current thread with [Looper.myQueue()](https://developer.android.com/reference/kotlin/android/os/Looper#myQueue()).

## Summary

| Nested classes ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [IdleHandler](https://developer.android.com/reference/kotlin/android/os/MessageQueue.IdleHandler) Callback interface for discovering when a thread is going to block waiting for more messages. |
| abstract | [OnFileDescriptorEventListener](https://developer.android.com/reference/kotlin/android/os/MessageQueue.OnFileDescriptorEventListener) A listener which is invoked when file descriptor related events occur. |

| Public methods ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addIdleHandler](https://developer.android.com/reference/kotlin/android/os/MessageQueue#addIdleHandler(android.os.MessageQueue.IdleHandler))`(`handler:` ` [MessageQueue.IdleHandler](https://developer.android.com/reference/kotlin/android/os/MessageQueue.IdleHandler)`)` Add a new [IdleHandler](https://developer.android.com/reference/kotlin/android/os/MessageQueue.IdleHandler) to this message queue. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addOnFileDescriptorEventListener](https://developer.android.com/reference/kotlin/android/os/MessageQueue#addOnFileDescriptorEventListener(java.io.FileDescriptor,%20kotlin.Int,%20android.os.MessageQueue.OnFileDescriptorEventListener))`(`fd:` ` [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)`, `events:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `listener:` ` [MessageQueue.OnFileDescriptorEventListener](https://developer.android.com/reference/kotlin/android/os/MessageQueue.OnFileDescriptorEventListener)`)` Adds a file descriptor listener to receive notification when file descriptor related events occur. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isIdle](https://developer.android.com/reference/kotlin/android/os/MessageQueue#isIdle())`()` Returns true if the looper has no pending messages which are due to be processed and is not blocked on a sync barrier. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeIdleHandler](https://developer.android.com/reference/kotlin/android/os/MessageQueue#removeIdleHandler(android.os.MessageQueue.IdleHandler))`(`handler:` ` [MessageQueue.IdleHandler](https://developer.android.com/reference/kotlin/android/os/MessageQueue.IdleHandler)`)` Remove an [IdleHandler](https://developer.android.com/reference/kotlin/android/os/MessageQueue.IdleHandler) from the queue that was previously added with [addIdleHandler](https://developer.android.com/reference/kotlin/android/os/MessageQueue#addIdleHandler(android.os.MessageQueue.IdleHandler)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeOnFileDescriptorEventListener](https://developer.android.com/reference/kotlin/android/os/MessageQueue#removeOnFileDescriptorEventListener(java.io.FileDescriptor))`(`fd:` ` [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)`)` Removes a file descriptor listener. |

| Protected methods ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/os/MessageQueue#finalize())`()` <br /> |

## Public methods

### addIdleHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addIdleHandler(handler: MessageQueue.IdleHandler): Unit
```

Add a new [IdleHandler](https://developer.android.com/reference/kotlin/android/os/MessageQueue.IdleHandler) to this message queue. This may be removed automatically for you by returning false from [IdleHandler.queueIdle()](https://developer.android.com/reference/kotlin/android/os/MessageQueue.IdleHandler#queueIdle())when it is invoked, or explicitly removing it with [removeIdleHandler](https://developer.android.com/reference/kotlin/android/os/MessageQueue#removeIdleHandler(android.os.MessageQueue.IdleHandler)).

This method is safe to call from any thread.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `handler` | [MessageQueue.IdleHandler](https://developer.android.com/reference/kotlin/android/os/MessageQueue.IdleHandler):The IdleHandler to be added. This value cannot be`null`. |

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
| `fd` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#):The file descriptor for which a listener will be registered. This value cannot be`null`. |
| `events` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The set of events to receive: a combination of the [OnFileDescriptorEventListener.EVENT_INPUT](https://developer.android.com/reference/kotlin/android/os/MessageQueue.OnFileDescriptorEventListener#EVENT_INPUT:kotlin.Int), [OnFileDescriptorEventListener.EVENT_OUTPUT](https://developer.android.com/reference/kotlin/android/os/MessageQueue.OnFileDescriptorEventListener#EVENT_OUTPUT:kotlin.Int), and [OnFileDescriptorEventListener.EVENT_ERROR](https://developer.android.com/reference/kotlin/android/os/MessageQueue.OnFileDescriptorEventListener#EVENT_ERROR:kotlin.Int) event masks. If the requested set of events is zero, then the listener is unregistered. Value is either`0`or a combination of [android.os.MessageQueue.OnFileDescriptorEventListener#EVENT_INPUT](https://developer.android.com/reference/kotlin/android/os/MessageQueue.OnFileDescriptorEventListener#EVENT_INPUT:kotlin.Int), [android.os.MessageQueue.OnFileDescriptorEventListener#EVENT_OUTPUT](https://developer.android.com/reference/kotlin/android/os/MessageQueue.OnFileDescriptorEventListener#EVENT_OUTPUT:kotlin.Int), and [android.os.MessageQueue.OnFileDescriptorEventListener#EVENT_ERROR](https://developer.android.com/reference/kotlin/android/os/MessageQueue.OnFileDescriptorEventListener#EVENT_ERROR:kotlin.Int) |
| `listener` | [MessageQueue.OnFileDescriptorEventListener](https://developer.android.com/reference/kotlin/android/os/MessageQueue.OnFileDescriptorEventListener):The listener to invoke when file descriptor events occur. This value cannot be`null`. |
| --- | --- |

**See Also**

- [android.os.MessageQueue.OnFileDescriptorEventListener](https://developer.android.com/reference/kotlin/android/os/MessageQueue.OnFileDescriptorEventListener)
- [#removeOnFileDescriptorEventListener](https://developer.android.com/reference/kotlin/android/os/MessageQueue#removeOnFileDescriptorEventListener(java.io.FileDescriptor)) 

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

Remove an [IdleHandler](https://developer.android.com/reference/kotlin/android/os/MessageQueue.IdleHandler) from the queue that was previously added with [addIdleHandler](https://developer.android.com/reference/kotlin/android/os/MessageQueue#addIdleHandler(android.os.MessageQueue.IdleHandler)). If the given object is not currently in the idle list, nothing is done.

This method is safe to call from any thread.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `handler` | [MessageQueue.IdleHandler](https://developer.android.com/reference/kotlin/android/os/MessageQueue.IdleHandler):The IdleHandler to be removed. This value cannot be`null`. |

### removeOnFileDescriptorEventListener

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeOnFileDescriptorEventListener(fd: FileDescriptor): Unit
```

Removes a file descriptor listener.

This method does nothing if no listener has been registered for the specified file descriptor.

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fd` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#):The file descriptor whose listener will be unregistered. This value cannot be`null`. |

**See Also**

- [android.os.MessageQueue.OnFileDescriptorEventListener](https://developer.android.com/reference/kotlin/android/os/MessageQueue.OnFileDescriptorEventListener)
- [#addOnFileDescriptorEventListener](https://developer.android.com/reference/kotlin/android/os/MessageQueue#addOnFileDescriptorEventListener(java.io.FileDescriptor,%20kotlin.Int,%20android.os.MessageQueue.OnFileDescriptorEventListener))

## Protected methods

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
