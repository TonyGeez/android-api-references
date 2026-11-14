# AsyncQueryHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AsyncQueryHandler

Kotlin| [Java](../android/content/AsyncQueryHandler.md) 
| --- | --- |

```
abstract class AsyncQueryHandler : Handler
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.os.Handler](../android/os/Handler.md) ||
| | ↳ | [android.content.AsyncQueryHandler](../android/content/AsyncQueryHandler.md) |

A helper class to help make handling asynchronous [ContentResolver](../android/content/ContentResolver.md) queries easier.

## Summary

| Nested classes ||
|------|------------------------------------------------------------------------------------------------------------------------|
| | [WorkerArgs](../android/content/AsyncQueryHandler.WorkerArgs.md) <br /> |
| open | [WorkerHandler](../android/content/AsyncQueryHandler.WorkerHandler.md) <br /> |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AsyncQueryHandler](../android/content/AsyncQueryHandler.md))`(`cr:` ` [ContentResolver](../android/content/ContentResolver.md)!`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancelOperation](../android/content/AsyncQueryHandler.md))`(`token:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Attempts to cancel operation that has not already started. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [handleMessage](../android/content/AsyncQueryHandler.md))`(`msg:` ` [Message](../android/os/Message.md)`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startDelete](../android/content/AsyncQueryHandler.md))`(`token:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cookie:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `uri:` ` [Uri](../android/net/Uri.md)!`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` This method begins an asynchronous delete. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startInsert](../android/content/AsyncQueryHandler.md))`(`token:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cookie:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `uri:` ` [Uri](../android/net/Uri.md)!`, `initialValues:` ` [ContentValues](../android/content/ContentValues.md)!`)` This method begins an asynchronous insert. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startQuery](../android/content/AsyncQueryHandler.md))`(`token:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cookie:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `uri:` ` [Uri](../android/net/Uri.md)!`, `projection:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `orderBy:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` This method begins an asynchronous query. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startUpdate](../android/content/AsyncQueryHandler.md))`(`token:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cookie:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `uri:` ` [Uri](../android/net/Uri.md)!`, `values:` ` [ContentValues](../android/content/ContentValues.md)!`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` This method begins an asynchronous update. |
| --- | --- |

| Protected methods ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Handler](../android/os/Handler.md)! | [createHandler](../android/content/AsyncQueryHandler.md))`(`looper:` ` [Looper](../android/os/Looper.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDeleteComplete](../android/content/AsyncQueryHandler.md))`(`token:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cookie:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `result:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when an asynchronous delete is completed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onInsertComplete](../android/content/AsyncQueryHandler.md))`(`token:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cookie:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `uri:` ` [Uri](../android/net/Uri.md)!`)` Called when an asynchronous insert is completed. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onQueryComplete](../android/content/AsyncQueryHandler.md))`(`token:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cookie:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `cursor:` ` [Cursor](../android/database/Cursor.md)!`)` Called when an asynchronous query is completed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onUpdateComplete](../android/content/AsyncQueryHandler.md))`(`token:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cookie:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `result:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when an asynchronous update is completed. |

| Inherited functions ||
|---|---|
| From class [Handler](../android/os/Handler.md) |------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Handler](../android/os/Handler.md) | [createAsync](../android/os/Handler.md))`(`looper:` ` [Looper](../android/os/Looper.md)`)` <br /> Create a new Handler whose posted messages and runnables are not subject to synchronization barriers such as display vsync. Messages sent to an async handler are guaranteed to be ordered with respect to one another, but not necessarily with respect to messages from other Handlers. <br /> | | [Handler](../android/os/Handler.md) | [createAsync](../android/os/Handler.md))`(`looper:` ` [Looper](../android/os/Looper.md)`, `callback:` ` [Handler.Callback](../android/os/Handler.Callback.md)`)` <br /> Create a new Handler whose posted messages and runnables are not subject to synchronization barriers such as display vsync. Messages sent to an async handler are guaranteed to be ordered with respect to one another, but not necessarily with respect to messages from other Handlers. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchMessage](../android/os/Handler.md))`(`msg:` ` [Message](../android/os/Message.md)`)` <br /> Handle system messages here. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dump](../android/os/Handler.md))`(`pw:` ` [Printer](../android/util/Printer.md)`, `prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` <br /> | | [Looper](../android/os/Looper.md) | [getLooper](../android/os/Handler.md))`()` <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getMessageName](../android/os/Handler.md))`(`message:` ` [Message](../android/os/Message.md)`)` <br /> Returns a string representing the name of the specified message. The default implementation will either return the class name of the message callback if any, or the hexadecimal representation of the message "what" field. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasCallbacks](../android/os/Handler.md))`(`r:` ` [Runnable](../java/lang/Runnable.md)`)` <br /> Check if there are any pending posts of messages with callback r in the message queue. This operation is worst case O(n) in the number of messages in the queue, and should be avoided. Instead consider another mechanism outside of the queue to track if messages were enqueued and dispatched. For instance, maintain a counter, incrementing it when enqueuing a message and decrementing it when handling a message. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasMessages](../android/os/Handler.md))`(`what:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Check if there are any pending posts of messages with code 'what' in the message queue. This operation is worst case O(n) in the number of messages in the queue, and should be avoided. Instead consider another mechanism outside of the queue to track if messages were enqueued and dispatched. For instance, maintain a counter, incrementing it when enqueuing a message and decrementing it when handling a message. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasMessages](../android/os/Handler.md))`(`what:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `object:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Check if there are any pending posts of messages with code 'what' and whose obj is 'object' in the message queue. This operation is worst case O(n) in the number of messages in the queue, and should be avoided. Instead consider another mechanism outside of the queue to track if messages were enqueued and dispatched. For instance, maintain a counter, incrementing it when enqueuing a message and decrementing it when handling a message. <br /> | | [Message](../android/os/Message.md) | [obtainMessage](../android/os/Handler.md))`()` <br /> Returns a new [Message](../android/os/Message.md) from the global message pool. More efficient than creating and allocating new instances. The retrieved message has its handler set to this instance (Message.target == this). If you don't want that facility, just call Message.obtain() instead. <br /> | | [Message](../android/os/Message.md) | [obtainMessage](../android/os/Handler.md))`(`what:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Same as [obtainMessage()](../android/os/Handler.md)), except that it also sets the what member of the returned Message. <br /> | | [Message](../android/os/Message.md) | [obtainMessage](../android/os/Handler.md))`(`what:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `arg1:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `arg2:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Same as [obtainMessage()](../android/os/Handler.md)), except that it also sets the what, arg1 and arg2 members of the returned Message. <br /> | | [Message](../android/os/Message.md) | [obtainMessage](../android/os/Handler.md))`(`what:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `arg1:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `arg2:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Same as [obtainMessage()](../android/os/Handler.md)), except that it also sets the what, obj, arg1,and arg2 values on the returned Message. <br /> | | [Message](../android/os/Message.md) | [obtainMessage](../android/os/Handler.md))`(`what:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Same as [obtainMessage()](../android/os/Handler.md)), except that it also sets the what and obj members of the returned Message. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [post](../android/os/Handler.md))`(`r:` ` [Runnable](../java/lang/Runnable.md)`)` <br /> Causes the Runnable r to be added to the message queue. The runnable will be run on the thread to which this handler is attached. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [postAtFrontOfQueue](../android/os/Handler.md))`(`r:` ` [Runnable](../java/lang/Runnable.md)`)` <br /> Posts a message to an object that implements Runnable. Causes the Runnable r to executed on the next iteration through the message queue. The runnable will be run on the thread to which this handler is attached.**This method is only for use in very special circumstances -- it can easily starve the message queue, cause ordering problems, or have other unexpected side-effects.** <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [postAtTime](../android/os/Handler.md))`(`r:` ` [Runnable](../java/lang/Runnable.md)`, `token:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`, `uptimeMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Causes the Runnable r to be added to the message queue, to be run at a specific time given by uptimeMillis.**The time-base is [android.os.SystemClock#uptimeMillis](../android/os/SystemClock.md)).**Time spent in deep sleep will add an additional delay to execution. The runnable will be run on the thread to which this handler is attached. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [postAtTime](../android/os/Handler.md))`(`r:` ` [Runnable](../java/lang/Runnable.md)`, `uptimeMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Causes the Runnable r to be added to the message queue, to be run at a specific time given by uptimeMillis.**The time-base is [android.os.SystemClock#uptimeMillis](../android/os/SystemClock.md)).**Time spent in deep sleep will add an additional delay to execution. The runnable will be run on the thread to which this handler is attached. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [postDelayed](../android/os/Handler.md))`(`r:` ` [Runnable](../java/lang/Runnable.md)`, `token:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`, `delayMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Causes the Runnable r to be added to the message queue, to be run after the specified amount of time elapses. The runnable will be run on the thread to which this handler is attached.**The time-base is [android.os.SystemClock#uptimeMillis](../android/os/SystemClock.md)).**Time spent in deep sleep will add an additional delay to execution. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [postDelayed](../android/os/Handler.md))`(`r:` ` [Runnable](../java/lang/Runnable.md)`, `delayMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Causes the Runnable r to be added to the message queue, to be run after the specified amount of time elapses. The runnable will be run on the thread to which this handler is attached.**The time-base is [android.os.SystemClock#uptimeMillis](../android/os/SystemClock.md)).**Time spent in deep sleep will add an additional delay to execution. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeCallbacks](../android/os/Handler.md))`(`r:` ` [Runnable](../java/lang/Runnable.md)`)` <br /> Remove any pending posts of Runnable r that are in the message queue. This operation is worst case O(n) in the number of messages in the queue, and should be avoided. Instead consider another mechanism outside of the queue to cancel a pending operation. For instance, maintain a flag to indicate whether the operation should be performed differently or not at all once it is dispatched. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeCallbacks](../android/os/Handler.md))`(`r:` ` [Runnable](../java/lang/Runnable.md)`, `token:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Remove any pending posts of Runnable r with Object token that are in the message queue. If token is null, all callbacks will be removed. This operation is worst case O(n) in the number of messages in the queue, and should be avoided. Instead consider another mechanism outside of the queue to cancel a pending operation. For instance, maintain a flag to indicate whether the operation should be performed differently or not at all once it is dispatched. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeCallbacksAndMessages](../android/os/Handler.md))`(`token:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Remove any pending posts of callbacks and sent messages whose obj is token. If token is null, all callbacks and messages will be removed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeMessages](../android/os/Handler.md))`(`what:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Remove any pending posts of messages with code 'what' that are in the message queue. Note that \`Message#what\` is 0 unless otherwise set. When calling \`postMessage(Runnable)\` or \`postAtTime(Runnable, long)\`, the \`Runnable\` is internally wrapped with a \`Message\` whose \`what\` is 0. Calling \`removeMessages(0)\` will remove all messages without a \`what\`, including posted \`Runnable\`s. This operation is worst case O(n) in the number of messages in the queue, and should be avoided. Instead consider another mechanism outside of the queue to cancel a pending operation. For instance, maintain a flag to indicate whether the operation should be performed differently or not at all once it is dispatched. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeMessages](../android/os/Handler.md))`(`what:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `object:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Remove any pending posts of messages with code 'what' and whose obj is 'object' that are in the message queue. If object is null, all messages will be removed. This operation is worst case O(n) in the number of messages in the queue, and should be avoided. Instead consider another mechanism outside of the queue to cancel a pending operation. For instance, maintain a flag to indicate whether the operation should be performed differently or not at all once it is dispatched. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [sendEmptyMessage](../android/os/Handler.md))`(`what:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sends a Message containing only the what value. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [sendEmptyMessageAtTime](../android/os/Handler.md))`(`what:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `uptimeMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Sends a Message containing only the what value, to be delivered at a specific time. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [sendEmptyMessageDelayed](../android/os/Handler.md))`(`what:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `delayMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Sends a Message containing only the what value, to be delivered after the specified amount of time elapses. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [sendMessage](../android/os/Handler.md))`(`msg:` ` [Message](../android/os/Message.md)`)` <br /> Pushes a message onto the end of the message queue after all pending messages before the current time. It will be received in [handleMessage](../android/os/Handler.md)), in the thread attached to this handler. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [sendMessageAtFrontOfQueue](../android/os/Handler.md))`(`msg:` ` [Message](../android/os/Message.md)`)` <br /> Enqueue a message at the front of the message queue, to be processed on the next iteration of the message loop. You will receive it in [handleMessage](../android/os/Handler.md)), in the thread attached to this handler.**This method is only for use in very special circumstances -- it can easily starve the message queue, cause ordering problems, or have other unexpected side-effects.** <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [sendMessageAtTime](../android/os/Handler.md))`(`msg:` ` [Message](../android/os/Message.md)`, `uptimeMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Enqueue a message into the message queue after all pending messages before the absolute time (in milliseconds) uptimeMillis.**The time-base is [android.os.SystemClock#uptimeMillis](../android/os/SystemClock.md)).** Time spent in deep sleep will add an additional delay to execution. You will receive it in [handleMessage](../android/os/Handler.md)), in the thread attached to this handler. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [sendMessageDelayed](../android/os/Handler.md))`(`msg:` ` [Message](../android/os/Message.md)`, `delayMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Enqueue a message into the message queue after all pending messages before (current time + delayMillis). You will receive it in [handleMessage](../android/os/Handler.md)), in the thread attached to this handler. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/os/Handler.md))`()` <br /> | ||

## Public constructors

### AsyncQueryHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AsyncQueryHandler(cr: ContentResolver!)
```

## Public methods

### cancelOperation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun cancelOperation(token: Int): Unit
```

Attempts to cancel operation that has not already started. Note that there is no guarantee that the operation will be canceled. They still may result in a call to on\[Query/Insert/Update/Delete\]Complete after this call has completed.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `token` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The token representing the operation to be canceled. If multiple operations have the same token they will all be canceled. |

### handleMessage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun handleMessage(msg: Message): Unit
```

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------|
| `msg` | [Message](../android/os/Message.md):This value cannot be`null`. |

### startDelete

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun startDelete(
    token: Int, 
    cookie: Any!, 
    uri: Uri!, 
    selection: String!, 
    selectionArgs: Array<String!>!
): Unit
```

This method begins an asynchronous delete. When the delete operation is done [onDeleteComplete](../android/content/AsyncQueryHandler.md))is called.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `token` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A token passed into [onDeleteComplete](../android/content/AsyncQueryHandler.md))to identify the delete operation. |
| `cookie` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:An object that gets passed into [onDeleteComplete](../android/content/AsyncQueryHandler.md)) |
| `uri` | [Uri](../android/net/Uri.md)!:the Uri passed to the delete operation. |
| --- | --- |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the where clause. |

### startInsert

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun startInsert(
    token: Int, 
    cookie: Any!, 
    uri: Uri!, 
    initialValues: ContentValues!
): Unit
```

This method begins an asynchronous insert. When the insert operation is done [onInsertComplete](../android/content/AsyncQueryHandler.md))is called.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `token` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A token passed into [onInsertComplete](../android/content/AsyncQueryHandler.md))to identify the insert operation. |
| `cookie` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:An object that gets passed into [onInsertComplete](../android/content/AsyncQueryHandler.md)) |
| `uri` | [Uri](../android/net/Uri.md)!:the Uri passed to the insert operation. |
| --- | --- |
| `initialValues` | [ContentValues](../android/content/ContentValues.md)!:the ContentValues parameter passed to the insert operation. |

### startQuery

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startQuery(
    token: Int, 
    cookie: Any!, 
    uri: Uri!, 
    projection: Array<String!>!, 
    selection: String!, 
    selectionArgs: Array<String!>!, 
    orderBy: String!
): Unit
```

This method begins an asynchronous query. When the query is done [onQueryComplete](../android/content/AsyncQueryHandler.md))is called.

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `token` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A token passed into [onQueryComplete](../android/content/AsyncQueryHandler.md))to identify the query. |
| `cookie` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:An object that gets passed into [onQueryComplete](../android/content/AsyncQueryHandler.md)) |
| `uri` | [Uri](../android/net/Uri.md)!:The URI, using the content:// scheme, for the content to retrieve. |
| --- | --- |
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:A list of which columns to return. Passing null will return all columns, which is discouraged to prevent reading data from storage that isn't going to be used. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A filter declaring which rows to return, formatted as an SQL WHERE clause (excluding the WHERE itself). Passing null will return all rows for the given URI. |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:You may include ?s in selection, which will be replaced by the values from selectionArgs, in the order that they appear in the selection. The values will be bound as Strings. |
| --- | --- |
| `orderBy` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:How to order the rows, formatted as an SQL ORDER BY clause (excluding the ORDER BY itself). Passing null will use the default sort order, which may be unordered. |

### startUpdate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun startUpdate(
    token: Int, 
    cookie: Any!, 
    uri: Uri!, 
    values: ContentValues!, 
    selection: String!, 
    selectionArgs: Array<String!>!
): Unit
```

This method begins an asynchronous update. When the update operation is done [onUpdateComplete](../android/content/AsyncQueryHandler.md))is called.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `token` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A token passed into [onUpdateComplete](../android/content/AsyncQueryHandler.md))to identify the update operation. |
| `cookie` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:An object that gets passed into [onUpdateComplete](../android/content/AsyncQueryHandler.md)) |
| `uri` | [Uri](../android/net/Uri.md)!:the Uri passed to the update operation. |
| --- | --- |
| `values` | [ContentValues](../android/content/ContentValues.md)!:the ContentValues parameter passed to the update operation. |

## Protected methods

### createHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun createHandler(looper: Looper!): Handler!
```  

### onDeleteComplete

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onDeleteComplete(
    token: Int, 
    cookie: Any!, 
    result: Int
): Unit
```

Called when an asynchronous delete is completed.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `token` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the token to identify the query, passed in from [startDelete](../android/content/AsyncQueryHandler.md)). |
| `cookie` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the cookie object that's passed in from [startDelete](../android/content/AsyncQueryHandler.md)). |
| `result` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the result returned from the delete operation |
| --- | --- |

### onInsertComplete

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onInsertComplete(
    token: Int, 
    cookie: Any!, 
    uri: Uri!
): Unit
```

Called when an asynchronous insert is completed.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `token` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the token to identify the query, passed in from [startInsert](../android/content/AsyncQueryHandler.md)). |
| `cookie` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the cookie object that's passed in from [startInsert](../android/content/AsyncQueryHandler.md)). |
| `uri` | [Uri](../android/net/Uri.md)!:the uri returned from the insert operation. |
| --- | --- |

### onQueryComplete

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onQueryComplete(
    token: Int, 
    cookie: Any!, 
    cursor: Cursor!
): Unit
```

Called when an asynchronous query is completed.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `token` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the token to identify the query, passed in from [startQuery](../android/content/AsyncQueryHandler.md)). |
| `cookie` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the cookie object passed in from [startQuery](../android/content/AsyncQueryHandler.md)). |
| `cursor` | [Cursor](../android/database/Cursor.md)!:The cursor holding the results from the query. |
| --- | --- |

### onUpdateComplete

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onUpdateComplete(
    token: Int, 
    cookie: Any!, 
    result: Int
): Unit
```

Called when an asynchronous update is completed.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `token` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the token to identify the query, passed in from [startUpdate](../android/content/AsyncQueryHandler.md)). |
| `cookie` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the cookie object that's passed in from [startUpdate](../android/content/AsyncQueryHandler.md)). |
| `result` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the result returned from the update operation |
| --- | --- |
