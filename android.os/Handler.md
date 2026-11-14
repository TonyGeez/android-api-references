Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Handler

Kotlin | [Java](https://developer.android.com/reference/android/os/Handler "View this page in Java")
| --- | --- |

```
open class Handler
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.Handler](https://developer.android.com/reference/kotlin/android/os/Handler#) |

| Known Direct Subclasses [AsyncQueryHandler](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler.html#), [AsyncQueryHandler.WorkerHandler](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler.WorkerHandler.html#), [HttpAuthHandler](https://developer.android.com/reference/kotlin/android/webkit/HttpAuthHandler.html#), [SslErrorHandler](https://developer.android.com/reference/kotlin/android/webkit/SslErrorHandler.html#) |---|---| | [AsyncQueryHandler](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler.html#) | A helper class to help make handling asynchronous `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#` queries easier. | | [AsyncQueryHandler.WorkerHandler](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler.WorkerHandler.html#) | <br /> | | [HttpAuthHandler](https://developer.android.com/reference/kotlin/android/webkit/HttpAuthHandler.html#) | Represents a request for HTTP authentication. | | [SslErrorHandler](https://developer.android.com/reference/kotlin/android/webkit/SslErrorHandler.html#) | Represents a request for handling an SSL error. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A Handler allows you to send and process `https://developer.android.com/reference/kotlin/android/os/Message` and Runnable objects associated with a thread's `https://developer.android.com/reference/kotlin/android/os/MessageQueue`. Each Handler instance is associated with a single thread and that thread's message queue. When you create a new Handler it is bound to a `https://developer.android.com/reference/kotlin/android/os/Looper`. It will deliver messages and runnables to that Looper's message queue and execute them on that Looper's thread.

There are two main uses for a Handler: (1) to schedule messages and runnables to be executed at some point in the future; and (2) to enqueue an action to be performed on a different thread than your own.

Scheduling messages is accomplished with the `https://developer.android.com/reference/kotlin/android/os/Handler#post(java.lang.Runnable)`, `https://developer.android.com/reference/kotlin/android/os/Handler#postAtTime(java.lang.Runnable,%20kotlin.Long)`, #postDelayed, `https://developer.android.com/reference/kotlin/android/os/Handler#sendEmptyMessage(kotlin.Int)`, `https://developer.android.com/reference/kotlin/android/os/Handler#sendMessage(android.os.Message)`, `https://developer.android.com/reference/kotlin/android/os/Handler#sendMessageAtTime(android.os.Message,%20kotlin.Long)`, and `https://developer.android.com/reference/kotlin/android/os/Handler#sendMessageDelayed(android.os.Message,%20kotlin.Long)` methods. The *post* versions allow you to enqueue Runnable objects to be called by the message queue when they are received; the *sendMessage* versions allow you to enqueue a `https://developer.android.com/reference/kotlin/android/os/Message` object containing a bundle of data that will be processed by the Handler's `https://developer.android.com/reference/kotlin/android/os/Handler#handleMessage(android.os.Message)` method (requiring that you implement a subclass of Handler).

When posting or sending to a Handler, you can either allow the item to be processed as soon as the message queue is ready to do so, or specify a delay before it gets processed or absolute time for it to be processed. The latter two allow you to implement timeouts, ticks, and other timing-based behavior.

When a process is created for your application, its main thread is dedicated to running a message queue that takes care of managing the top-level application objects (activities, broadcast receivers, etc) and any windows they create. You can create your own threads, and communicate back with the main application thread through a Handler. This is done by calling the same *post* or *sendMessage* methods as before, but from your new thread. The given Runnable or Message will then be scheduled in the Handler's message queue and processed when appropriate.

## Performance considerations when using `Handler`

Beware that the "has" and "remove" methods of `Handler` can be very slow because these operations scan the entire queue of pending messages. If the underlying `https://developer.android.com/reference/kotlin/android/os/Looper`'s `https://developer.android.com/reference/kotlin/android/os/MessageQueue` has many pending messages, this can be expensive.

- Instead of removing a message or a callback to cancel a pending operation, consider setting a flag to indicate cancellation and having the operation check the flag before proceeding.
- Instead of checking if the queue has a message or a callback to find if a pending operation has not yet occurred, consider having that operation set a flag to indicate that it has begun.

See `java.util.concurrent` for standard concurrency primitives.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/os/Handler.Callback` Callback interface you can use when instantiating a Handler to avoid having to implement your own subclass of Handler. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Handler#Handler()()` Default constructor associates this handler with the `https://developer.android.com/reference/kotlin/android/os/Looper` for the current thread. |
| `https://developer.android.com/reference/kotlin/android/os/Handler#Handler(android.os.Handler.Callback)(callback: https://developer.android.com/reference/kotlin/android/os/Handler.Callback?)` Constructor associates this handler with the `https://developer.android.com/reference/kotlin/android/os/Looper` for the current thread and takes a callback interface in which you can handle messages. |
| `https://developer.android.com/reference/kotlin/android/os/Handler#Handler(android.os.Looper)(looper: https://developer.android.com/reference/kotlin/android/os/Looper)` Use the provided `https://developer.android.com/reference/kotlin/android/os/Looper` instead of the default one. |
| `https://developer.android.com/reference/kotlin/android/os/Handler#Handler(android.os.Looper,%20android.os.Handler.Callback)(looper: https://developer.android.com/reference/kotlin/android/os/Looper, callback: https://developer.android.com/reference/kotlin/android/os/Handler.Callback?)` Use the provided `https://developer.android.com/reference/kotlin/android/os/Looper` instead of the default one and take a callback interface in which to handle messages. |

| Public methods ||
|---|---|
| open static [Handler](https://developer.android.com/reference/kotlin/android/os/Handler#) | `https://developer.android.com/reference/kotlin/android/os/Handler#createAsync(android.os.Looper)(looper: https://developer.android.com/reference/kotlin/android/os/Looper)` Create a new Handler whose posted messages and runnables are not subject to synchronization barriers such as display vsync. |
| open static [Handler](https://developer.android.com/reference/kotlin/android/os/Handler#) | `https://developer.android.com/reference/kotlin/android/os/Handler#createAsync(android.os.Looper,%20android.os.Handler.Callback)(looper: https://developer.android.com/reference/kotlin/android/os/Looper, callback: https://developer.android.com/reference/kotlin/android/os/Handler.Callback)` Create a new Handler whose posted messages and runnables are not subject to synchronization barriers such as display vsync. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Handler#dispatchMessage(android.os.Message)(msg: https://developer.android.com/reference/kotlin/android/os/Message)` Handle system messages here. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Handler#dump(android.util.Printer,%20kotlin.String)(pw: https://developer.android.com/reference/kotlin/android/util/Printer.html#, prefix: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` <br /> |
| [Looper](https://developer.android.com/reference/kotlin/android/os/Looper) | `https://developer.android.com/reference/kotlin/android/os/Handler#getLooper()()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/Handler#getMessageName(android.os.Message)(message: https://developer.android.com/reference/kotlin/android/os/Message)` Returns a string representing the name of the specified message. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Handler#handleMessage(android.os.Message)(msg: https://developer.android.com/reference/kotlin/android/os/Message)` Subclasses must implement this to receive messages. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/Handler#hasCallbacks(java.lang.Runnable)(r: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)` Check if there are any pending posts of messages with callback r in the message queue. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/Handler#hasMessages(kotlin.Int)(what: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Check if there are any pending posts of messages with code 'what' in the message queue. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/Handler#hasMessages(kotlin.Int,%20kotlin.Any)(what: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, object: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Check if there are any pending posts of messages with code 'what' and whose obj is 'object' in the message queue. |
| [Message](https://developer.android.com/reference/kotlin/android/os/Message) | `https://developer.android.com/reference/kotlin/android/os/Handler#obtainMessage()()` Returns a new `https://developer.android.com/reference/kotlin/android/os/Message` from the global message pool. |
| [Message](https://developer.android.com/reference/kotlin/android/os/Message) | `https://developer.android.com/reference/kotlin/android/os/Handler#obtainMessage(kotlin.Int)(what: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Same as `https://developer.android.com/reference/kotlin/android/os/Handler#obtainMessage()`, except that it also sets the what member of the returned Message. |
| --- | --- |
| [Message](https://developer.android.com/reference/kotlin/android/os/Message) | `https://developer.android.com/reference/kotlin/android/os/Handler#obtainMessage(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(what: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, arg1: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, arg2: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Same as `https://developer.android.com/reference/kotlin/android/os/Handler#obtainMessage()`, except that it also sets the what, arg1 and arg2 members of the returned Message. |
| [Message](https://developer.android.com/reference/kotlin/android/os/Message) | `https://developer.android.com/reference/kotlin/android/os/Handler#obtainMessage(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Any)(what: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, arg1: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, arg2: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, obj: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Same as `https://developer.android.com/reference/kotlin/android/os/Handler#obtainMessage()`, except that it also sets the what, obj, arg1,and arg2 values on the returned Message. |
| [Message](https://developer.android.com/reference/kotlin/android/os/Message) | `https://developer.android.com/reference/kotlin/android/os/Handler#obtainMessage(kotlin.Int,%20kotlin.Any)(what: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, obj: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Same as `https://developer.android.com/reference/kotlin/android/os/Handler#obtainMessage()`, except that it also sets the what and obj members of the returned Message. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/Handler#post(java.lang.Runnable)(r: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)` Causes the Runnable r to be added to the message queue. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/Handler#postAtFrontOfQueue(java.lang.Runnable)(r: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)` Posts a message to an object that implements Runnable. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/Handler#postAtTime(java.lang.Runnable,%20kotlin.Any,%20kotlin.Long)(r: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#, token: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?, uptimeMillis: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Causes the Runnable r to be added to the message queue, to be run at a specific time given by uptimeMillis. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/Handler#postAtTime(java.lang.Runnable,%20kotlin.Long)(r: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#, uptimeMillis: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Causes the Runnable r to be added to the message queue, to be run at a specific time given by uptimeMillis. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/Handler#postDelayed(java.lang.Runnable,%20kotlin.Any,%20kotlin.Long)(r: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#, token: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?, delayMillis: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Causes the Runnable r to be added to the message queue, to be run after the specified amount of time elapses. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/Handler#postDelayed(java.lang.Runnable,%20kotlin.Long)(r: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#, delayMillis: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Causes the Runnable r to be added to the message queue, to be run after the specified amount of time elapses. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Handler#removeCallbacks(java.lang.Runnable)(r: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)` Remove any pending posts of Runnable r that are in the message queue. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Handler#removeCallbacks(java.lang.Runnable,%20kotlin.Any)(r: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#, token: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Remove any pending posts of Runnable r with Object token that are in the message queue. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Handler#removeCallbacksAndMessages(kotlin.Any)(token: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Remove any pending posts of callbacks and sent messages whose obj is token. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Handler#removeMessages(kotlin.Int)(what: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Remove any pending posts of messages with code 'what' that are in the message queue. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Handler#removeMessages(kotlin.Int,%20kotlin.Any)(what: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, object: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Remove any pending posts of messages with code 'what' and whose obj is 'object' that are in the message queue. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/Handler#sendEmptyMessage(kotlin.Int)(what: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sends a Message containing only the what value. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/Handler#sendEmptyMessageAtTime(kotlin.Int,%20kotlin.Long)(what: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uptimeMillis: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Sends a Message containing only the what value, to be delivered at a specific time. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/Handler#sendEmptyMessageDelayed(kotlin.Int,%20kotlin.Long)(what: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, delayMillis: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Sends a Message containing only the what value, to be delivered after the specified amount of time elapses. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/Handler#sendMessage(android.os.Message)(msg: https://developer.android.com/reference/kotlin/android/os/Message)` Pushes a message onto the end of the message queue after all pending messages before the current time. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/Handler#sendMessageAtFrontOfQueue(android.os.Message)(msg: https://developer.android.com/reference/kotlin/android/os/Message)` Enqueue a message at the front of the message queue, to be processed on the next iteration of the message loop. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/Handler#sendMessageAtTime(android.os.Message,%20kotlin.Long)(msg: https://developer.android.com/reference/kotlin/android/os/Message, uptimeMillis: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Enqueue a message into the message queue after all pending messages before the absolute time (in milliseconds) uptimeMillis. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/Handler#sendMessageDelayed(android.os.Message,%20kotlin.Long)(msg: https://developer.android.com/reference/kotlin/android/os/Message, delayMillis: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Enqueue a message into the message queue after all pending messages before (current time + delayMillis). |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/Handler#toString()()` Returns a string representation of the object. |

## Public constructors

### Handler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Handler()
```

**Deprecated:** *Implicitly choosing a Looper during Handler construction can lead to bugs where operations are silently lost (if the Handler is not expecting new tasks and quits), crashes (if a handler is sometimes created on a thread without a Looper active), or race conditions, where the thread a handler is associated with is not what the author anticipated. Instead, use an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` or specify the Looper explicitly, using `https://developer.android.com/reference/kotlin/android/os/Looper#getMainLooper()`, `https://developer.android.com/reference/kotlin/android/view/View.html#getHandler()`, or similar. If the implicit thread local behavior is required for compatibility, use `new Handler(Looper.myLooper())` to make it clear to readers.*

Default constructor associates this handler with the `https://developer.android.com/reference/kotlin/android/os/Looper` for the current thread. If this thread does not have a looper, this handler won't be able to receive messages so an exception is thrown.

### Handler

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Handler(callback: Handler.Callback?)
```

**Deprecated:** *Implicitly choosing a Looper during Handler construction can lead to bugs where operations are silently lost (if the Handler is not expecting new tasks and quits), crashes (if a handler is sometimes created on a thread without a Looper active), or race conditions, where the thread a handler is associated with is not what the author anticipated. Instead, use an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` or specify the Looper explicitly, using `https://developer.android.com/reference/kotlin/android/os/Looper#getMainLooper()`, `https://developer.android.com/reference/kotlin/android/view/View.html#getHandler()`, or similar. If the implicit thread local behavior is required for compatibility, use `new Handler(Looper.myLooper(), callback)` to make it clear to readers.*

Constructor associates this handler with the `https://developer.android.com/reference/kotlin/android/os/Looper` for the current thread and takes a callback interface in which you can handle messages. If this thread does not have a looper, this handler won't be able to receive messages so an exception is thrown.

| Parameters ||
|---|---|
| `callback` | [Handler.Callback](https://developer.android.com/reference/kotlin/android/os/Handler.Callback)?: The callback interface in which to handle messages, or null. |

### Handler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Handler(looper: Looper)
```

Use the provided `https://developer.android.com/reference/kotlin/android/os/Looper` instead of the default one.

| Parameters ||
|---|---|
| `looper` | [Looper](https://developer.android.com/reference/kotlin/android/os/Looper): The looper, must not be null. |

### Handler

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Handler(
    looper: Looper, 
    callback: Handler.Callback?)
```

Use the provided `https://developer.android.com/reference/kotlin/android/os/Looper` instead of the default one and take a callback interface in which to handle messages.

| Parameters ||
|---|---|
| `looper` | [Looper](https://developer.android.com/reference/kotlin/android/os/Looper): The looper, must not be null. |
| `callback` | [Handler.Callback](https://developer.android.com/reference/kotlin/android/os/Handler.Callback)?: The callback interface in which to handle messages, or null. |

## Public methods

### createAsync

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createAsync(looper: Looper): Handler
```

Create a new Handler whose posted messages and runnables are not subject to synchronization barriers such as display vsync.

Messages sent to an async handler are guaranteed to be ordered with respect to one another, but not necessarily with respect to messages from other Handlers.

| Parameters ||
|---|---|
| `looper` | [Looper](https://developer.android.com/reference/kotlin/android/os/Looper): the Looper that the new Handler should be bound to. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Handler#` | a new async Handler instance. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/Handler#createAsync(android.os.Looper,%20android.os.Handler.Callback)`

### createAsync

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createAsync(
    looper: Looper, 
    callback: Handler.Callback
): Handler
```

Create a new Handler whose posted messages and runnables are not subject to synchronization barriers such as display vsync.

Messages sent to an async handler are guaranteed to be ordered with respect to one another, but not necessarily with respect to messages from other Handlers.

| Parameters ||
|---|---|
| `looper` | [Looper](https://developer.android.com/reference/kotlin/android/os/Looper): the Looper that the new Handler should be bound to. This value cannot be `null`. |
| `callback` | [Handler.Callback](https://developer.android.com/reference/kotlin/android/os/Handler.Callback): This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Handler#` | a new async Handler instance. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/Handler#createAsync(android.os.Looper)`

### dispatchMessage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchMessage(msg: Message): Unit
```

Handle system messages here.

| Parameters ||
|---|---|
| `msg` | [Message](https://developer.android.com/reference/kotlin/android/os/Message): This value cannot be `null`. |

### dump

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun dump(
    pw: Printer, 
    prefix: String
): Unit
```

| Parameters ||
|---|---|
| `pw` | [Printer](https://developer.android.com/reference/kotlin/android/util/Printer.html#): This value cannot be `null`. |
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

### getLooper

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLooper(): Looper
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Looper` | This value cannot be `null`. |

### getMessageName

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMessageName(message: Message): String
```

Returns a string representing the name of the specified message. The default implementation will either return the class name of the message callback if any, or the hexadecimal representation of the message "what" field.

| Parameters ||
|---|---|
| `message` | [Message](https://developer.android.com/reference/kotlin/android/os/Message): The message whose name is being queried. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### handleMessage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun handleMessage(msg: Message): Unit
```

Subclasses must implement this to receive messages.

| Parameters ||
|---|---|
| `msg` | [Message](https://developer.android.com/reference/kotlin/android/os/Message): This value cannot be `null`. |

### hasCallbacks

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasCallbacks(r: Runnable): Boolean
```

Check if there are any pending posts of messages with callback r in the message queue.

This operation is worst case O(n) in the number of messages in the queue, and should be avoided. Instead consider another mechanism outside of the queue to track if messages were enqueued and dispatched. For instance, maintain a counter, incrementing it when enqueuing a message and decrementing it when handling a message.

| Parameters ||
|---|---|
| `r` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#): This value cannot be `null`. |

### hasMessages

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasMessages(what: Int): Boolean
```

Check if there are any pending posts of messages with code 'what' in the message queue.

This operation is worst case O(n) in the number of messages in the queue, and should be avoided. Instead consider another mechanism outside of the queue to track if messages were enqueued and dispatched. For instance, maintain a counter, incrementing it when enqueuing a message and decrementing it when handling a message.

### hasMessages

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasMessages(
    what: Int, 
    object: Any?
): Boolean
```

Check if there are any pending posts of messages with code 'what' and whose obj is 'object' in the message queue.

This operation is worst case O(n) in the number of messages in the queue, and should be avoided. Instead consider another mechanism outside of the queue to track if messages were enqueued and dispatched. For instance, maintain a counter, incrementing it when enqueuing a message and decrementing it when handling a message.

| Parameters ||
|---|---|
| `object` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: This value may be `null`. |

### obtainMessage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun obtainMessage(): Message
```

Returns a new `https://developer.android.com/reference/kotlin/android/os/Message` from the global message pool. More efficient than creating and allocating new instances. The retrieved message has its handler set to this instance (Message.target == this). If you don't want that facility, just call Message.obtain() instead.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Message` | This value cannot be `null`. |

### obtainMessage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun obtainMessage(what: Int): Message
```

Same as `https://developer.android.com/reference/kotlin/android/os/Handler#obtainMessage()`, except that it also sets the what member of the returned Message.

| Parameters ||
|---|---|
| `what` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value to assign to the returned Message.what field. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Message` | A Message from the global message pool. This value cannot be `null`. |

### obtainMessage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun obtainMessage(
    what: Int, 
    arg1: Int, 
    arg2: Int
): Message
```

Same as `https://developer.android.com/reference/kotlin/android/os/Handler#obtainMessage()`, except that it also sets the what, arg1 and arg2 members of the returned Message.

| Parameters ||
|---|---|
| `what` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value to assign to the returned Message.what field. |
| `arg1` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value to assign to the returned Message.arg1 field. |
| `arg2` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value to assign to the returned Message.arg2 field. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Message` | A Message from the global message pool. This value cannot be `null`. |

### obtainMessage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun obtainMessage(
    what: Int, 
    arg1: Int, 
    arg2: Int, 
    obj: Any?
): Message
```

Same as `https://developer.android.com/reference/kotlin/android/os/Handler#obtainMessage()`, except that it also sets the what, obj, arg1,and arg2 values on the returned Message.

| Parameters ||
|---|---|
| `what` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value to assign to the returned Message.what field. |
| `arg1` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value to assign to the returned Message.arg1 field. |
| `arg2` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value to assign to the returned Message.arg2 field. |
| --- | --- |
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: Value to assign to the returned Message.obj field. This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Message` | A Message from the global message pool. This value cannot be `null`. |

### obtainMessage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun obtainMessage(
    what: Int, 
    obj: Any?
): Message
```

Same as `https://developer.android.com/reference/kotlin/android/os/Handler#obtainMessage()`, except that it also sets the what and obj members of the returned Message.

| Parameters ||
|---|---|
| `what` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value to assign to the returned Message.what field. |
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: Value to assign to the returned Message.obj field. This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Message` | A Message from the global message pool. This value cannot be `null`. |

### post

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun post(r: Runnable): Boolean
```

Causes the Runnable r to be added to the message queue. The runnable will be run on the thread to which this handler is attached.

| Parameters ||
|---|---|
| `r` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#): The Runnable that will be executed. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the Runnable was successfully placed in to the message queue. Returns false on failure, usually because the looper processing the message queue is exiting. |

### postAtFrontOfQueue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun postAtFrontOfQueue(r: Runnable): Boolean
```

Posts a message to an object that implements Runnable. Causes the Runnable r to executed on the next iteration through the message queue. The runnable will be run on the thread to which this handler is attached. **This method is only for use in very special circumstances -- it can easily starve the message queue, cause ordering problems, or have other unexpected side-effects.**

| Parameters ||
|---|---|
| `r` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#): The Runnable that will be executed. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the message was successfully placed in to the message queue. Returns false on failure, usually because the looper processing the message queue is exiting. |

### postAtTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun postAtTime(
    r: Runnable, 
    token: Any?, 
    uptimeMillis: Long
): Boolean
```

Causes the Runnable r to be added to the message queue, to be run at a specific time given by uptimeMillis. **The time-base is `https://developer.android.com/reference/kotlin/android/os/SystemClock#uptimeMillis()`.** Time spent in deep sleep will add an additional delay to execution. The runnable will be run on the thread to which this handler is attached.

| Parameters ||
|---|---|
| `r` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#): The Runnable that will be executed. This value cannot be `null`. |
| `token` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: An instance which can be used to cancel `r` via `https://developer.android.com/reference/kotlin/android/os/Handler#removeCallbacksAndMessages(kotlin.Any)`. This value may be `null`. |
| `uptimeMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The absolute time at which the callback should run, using the `https://developer.android.com/reference/kotlin/android/os/SystemClock#uptimeMillis()` time-base. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the Runnable was successfully placed in to the message queue. Returns false on failure, usually because the looper processing the message queue is exiting. Note that a result of true does not mean the Runnable will be processed -- if the looper is quit before the delivery time of the message occurs then the message will be dropped. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/SystemClock#uptimeMillis()`

### postAtTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun postAtTime(
    r: Runnable, 
    uptimeMillis: Long
): Boolean
```

Causes the Runnable r to be added to the message queue, to be run at a specific time given by uptimeMillis. **The time-base is `https://developer.android.com/reference/kotlin/android/os/SystemClock#uptimeMillis()`.** Time spent in deep sleep will add an additional delay to execution. The runnable will be run on the thread to which this handler is attached.

| Parameters ||
|---|---|
| `r` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#): The Runnable that will be executed. This value cannot be `null`. |
| `uptimeMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The absolute time at which the callback should run, using the `https://developer.android.com/reference/kotlin/android/os/SystemClock#uptimeMillis()` time-base. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the Runnable was successfully placed in to the message queue. Returns false on failure, usually because the looper processing the message queue is exiting. Note that a result of true does not mean the Runnable will be processed -- if the looper is quit before the delivery time of the message occurs then the message will be dropped. |

### postDelayed

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun postDelayed(
    r: Runnable, 
    token: Any?, 
    delayMillis: Long
): Boolean
```

Causes the Runnable r to be added to the message queue, to be run after the specified amount of time elapses. The runnable will be run on the thread to which this handler is attached. **The time-base is `https://developer.android.com/reference/kotlin/android/os/SystemClock#uptimeMillis()`.** Time spent in deep sleep will add an additional delay to execution.

| Parameters ||
|---|---|
| `r` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#): The Runnable that will be executed. This value cannot be `null`. |
| `token` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: An instance which can be used to cancel `r` via `https://developer.android.com/reference/kotlin/android/os/Handler#removeCallbacksAndMessages(kotlin.Any)`. This value may be `null`. |
| `delayMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The delay (in milliseconds) until the Runnable will be executed. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the Runnable was successfully placed in to the message queue. Returns false on failure, usually because the looper processing the message queue is exiting. Note that a result of true does not mean the Runnable will be processed -- if the looper is quit before the delivery time of the message occurs then the message will be dropped. |

### postDelayed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun postDelayed(
    r: Runnable, 
    delayMillis: Long
): Boolean
```

Causes the Runnable r to be added to the message queue, to be run after the specified amount of time elapses. The runnable will be run on the thread to which this handler is attached. **The time-base is `https://developer.android.com/reference/kotlin/android/os/SystemClock#uptimeMillis()`.** Time spent in deep sleep will add an additional delay to execution.

| Parameters ||
|---|---|
| `r` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#): The Runnable that will be executed. This value cannot be `null`. |
| `delayMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The delay (in milliseconds) until the Runnable will be executed. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the Runnable was successfully placed in to the message queue. Returns false on failure, usually because the looper processing the message queue is exiting. Note that a result of true does not mean the Runnable will be processed -- if the looper is quit before the delivery time of the message occurs then the message will be dropped. |

### removeCallbacks

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeCallbacks(r: Runnable): Unit
```

Remove any pending posts of Runnable r that are in the message queue.

This operation is worst case O(n) in the number of messages in the queue, and should be avoided. Instead consider another mechanism outside of the queue to cancel a pending operation. For instance, maintain a flag to indicate whether the operation should be performed differently or not at all once it is dispatched.

| Parameters ||
|---|---|
| `r` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#): This value cannot be `null`. |

### removeCallbacks

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeCallbacks(
    r: Runnable, 
    token: Any?
): Unit
```

Remove any pending posts of Runnable r with Object token that are in the message queue. If token is null, all callbacks will be removed.

This operation is worst case O(n) in the number of messages in the queue, and should be avoided. Instead consider another mechanism outside of the queue to cancel a pending operation. For instance, maintain a flag to indicate whether the operation should be performed differently or not at all once it is dispatched.

| Parameters ||
|---|---|
| `r` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#): This value cannot be `null`. |
| `token` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: This value may be `null`. |

### removeCallbacksAndMessages

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeCallbacksAndMessages(token: Any?): Unit
```

Remove any pending posts of callbacks and sent messages whose obj is token. If token is null, all callbacks and messages will be removed.

| Parameters ||
|---|---|
| `token` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: This value may be `null`. |

### removeMessages

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeMessages(what: Int): Unit
```

Remove any pending posts of messages with code 'what' that are in the message queue. Note that \`Message#what\` is 0 unless otherwise set. When calling \`postMessage(Runnable)\` or \`postAtTime(Runnable, long)\`, the \`Runnable\` is internally wrapped with a \`Message\` whose \`what\` is 0. Calling \`removeMessages(0)\` will remove all messages without a \`what\`, including posted \`Runnable\`s.

This operation is worst case O(n) in the number of messages in the queue, and should be avoided. Instead consider another mechanism outside of the queue to cancel a pending operation. For instance, maintain a flag to indicate whether the operation should be performed differently or not at all once it is dispatched.

### removeMessages

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeMessages(
    what: Int, 
    object: Any?
): Unit
```

Remove any pending posts of messages with code 'what' and whose obj is 'object' that are in the message queue. If object is null, all messages will be removed.

This operation is worst case O(n) in the number of messages in the queue, and should be avoided. Instead consider another mechanism outside of the queue to cancel a pending operation. For instance, maintain a flag to indicate whether the operation should be performed differently or not at all once it is dispatched.

| Parameters ||
|---|---|
| `object` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: This value may be `null`. |

### sendEmptyMessage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun sendEmptyMessage(what: Int): Boolean
```

Sends a Message containing only the what value.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the message was successfully placed in to the message queue. Returns false on failure, usually because the looper processing the message queue is exiting. |

### sendEmptyMessageAtTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun sendEmptyMessageAtTime(
    what: Int, 
    uptimeMillis: Long
): Boolean
```

Sends a Message containing only the what value, to be delivered at a specific time.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the message was successfully placed in to the message queue. Returns false on failure, usually because the looper processing the message queue is exiting. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/Handler#sendMessageAtTime(android.os.Message,%20kotlin.Long)`

### sendEmptyMessageDelayed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun sendEmptyMessageDelayed(
    what: Int, 
    delayMillis: Long
): Boolean
```

Sends a Message containing only the what value, to be delivered after the specified amount of time elapses.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the message was successfully placed in to the message queue. Returns false on failure, usually because the looper processing the message queue is exiting. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/Handler#sendMessageDelayed(android.os.Message,%20kotlin.Long)`

### sendMessage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun sendMessage(msg: Message): Boolean
```

Pushes a message onto the end of the message queue after all pending messages before the current time. It will be received in `https://developer.android.com/reference/kotlin/android/os/Handler#handleMessage(android.os.Message)`, in the thread attached to this handler.

| Parameters ||
|---|---|
| `msg` | [Message](https://developer.android.com/reference/kotlin/android/os/Message): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the message was successfully placed in to the message queue. Returns false on failure, usually because the looper processing the message queue is exiting. |

### sendMessageAtFrontOfQueue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun sendMessageAtFrontOfQueue(msg: Message): Boolean
```

Enqueue a message at the front of the message queue, to be processed on the next iteration of the message loop. You will receive it in `https://developer.android.com/reference/kotlin/android/os/Handler#handleMessage(android.os.Message)`, in the thread attached to this handler. **This method is only for use in very special circumstances -- it can easily starve the message queue, cause ordering problems, or have other unexpected side-effects.**

| Parameters ||
|---|---|
| `msg` | [Message](https://developer.android.com/reference/kotlin/android/os/Message): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the message was successfully placed in to the message queue. Returns false on failure, usually because the looper processing the message queue is exiting. |

### sendMessageAtTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendMessageAtTime(
    msg: Message, 
    uptimeMillis: Long
): Boolean
```

Enqueue a message into the message queue after all pending messages before the absolute time (in milliseconds) uptimeMillis. **The time-base is `https://developer.android.com/reference/kotlin/android/os/SystemClock#uptimeMillis()`.** Time spent in deep sleep will add an additional delay to execution. You will receive it in `https://developer.android.com/reference/kotlin/android/os/Handler#handleMessage(android.os.Message)`, in the thread attached to this handler.

| Parameters ||
|---|---|
| `msg` | [Message](https://developer.android.com/reference/kotlin/android/os/Message): This value cannot be `null`. |
| `uptimeMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The absolute time at which the message should be delivered, using the `https://developer.android.com/reference/kotlin/android/os/SystemClock#uptimeMillis()` time-base. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the message was successfully placed in to the message queue. Returns false on failure, usually because the looper processing the message queue is exiting. Note that a result of true does not mean the message will be processed -- if the looper is quit before the delivery time of the message occurs then the message will be dropped. |

### sendMessageDelayed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun sendMessageDelayed(
    msg: Message, 
    delayMillis: Long
): Boolean
```

Enqueue a message into the message queue after all pending messages before (current time + delayMillis). You will receive it in `https://developer.android.com/reference/kotlin/android/os/Handler#handleMessage(android.os.Message)`, in the thread attached to this handler.

| Parameters ||
|---|---|
| `msg` | [Message](https://developer.android.com/reference/kotlin/android/os/Message): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the message was successfully placed in to the message queue. Returns false on failure, usually because the looper processing the message queue is exiting. Note that a result of true does not mean the message will be processed -- if the looper is quit before the delivery time of the message occurs then the message will be dropped. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |
