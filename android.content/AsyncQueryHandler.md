# AsyncQueryHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AsyncQueryHandler

Kotlin| [Java](https://developer.android.com/reference/android/content/AsyncQueryHandler "View this page in Java") 

```
abstract class AsyncQueryHandler : Handler
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.os.Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#) ||
| | ↳ | [android.content.AsyncQueryHandler](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler#) |

A helper class to help make handling asynchronous [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver) queries easier.

## Summary

| Nested classes ||
|------|------------------------------------------------------------------------------------------------------------------------|
| | [WorkerArgs](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler.WorkerArgs) <br /> |
| open | [WorkerHandler](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler.WorkerHandler) <br /> |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AsyncQueryHandler](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler#AsyncQueryHandler(android.content.ContentResolver))`(`cr:` ` [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver)!`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancelOperation](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler#cancelOperation(kotlin.Int))`(`token:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Attempts to cancel operation that has not already started. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [handleMessage](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler#handleMessage(android.os.Message))`(`msg:` ` [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#)`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startDelete](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler#startDelete(kotlin.Int,%20kotlin.Any,%20android.net.Uri,%20kotlin.String,%20kotlin.Array))`(`token:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cookie:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` This method begins an asynchronous delete. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startInsert](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler#startInsert(kotlin.Int,%20kotlin.Any,%20android.net.Uri,%20android.content.ContentValues))`(`token:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cookie:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`, `initialValues:` ` [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)!`)` This method begins an asynchronous insert. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startQuery](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler#startQuery(kotlin.Int,%20kotlin.Any,%20android.net.Uri,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String))`(`token:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cookie:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`, `projection:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `orderBy:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` This method begins an asynchronous query. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startUpdate](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler#startUpdate(kotlin.Int,%20kotlin.Any,%20android.net.Uri,%20android.content.ContentValues,%20kotlin.String,%20kotlin.Array))`(`token:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cookie:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`, `values:` ` [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)!`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` This method begins an asynchronous update. |

| Protected methods ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)! | [createHandler](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler#createHandler(android.os.Looper))`(`looper:` ` [Looper](https://developer.android.com/reference/kotlin/android/os/Looper.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDeleteComplete](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler#onDeleteComplete(kotlin.Int,%20kotlin.Any,%20kotlin.Int))`(`token:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cookie:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `result:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when an asynchronous delete is completed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onInsertComplete](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler#onInsertComplete(kotlin.Int,%20kotlin.Any,%20android.net.Uri))`(`token:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cookie:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`)` Called when an asynchronous insert is completed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onQueryComplete](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler#onQueryComplete(kotlin.Int,%20kotlin.Any,%20android.database.Cursor))`(`token:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cookie:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `cursor:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`)` Called when an asynchronous query is completed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onUpdateComplete](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler#onUpdateComplete(kotlin.Int,%20kotlin.Any,%20kotlin.Int))`(`token:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cookie:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `result:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when an asynchronous update is completed. |

| Inherited functions ||
|---|---|
| From class [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#) |------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#) | [createAsync](https://developer.android.com/reference/kotlin/android/os/Handler.html#createAsync(android.os.Looper))`(`looper:` ` [Looper](https://developer.android.com/reference/kotlin/android/os/Looper.html#)`)` <br /> Create a new Handler whose posted messages and runnables are not subject to synchronization barriers such as display vsync. Messages sent to an async handler are guaranteed to be ordered with respect to one another, but not necessarily with respect to messages from other Handlers. <br /> | | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#) | [createAsync](https://developer.android.com/reference/kotlin/android/os/Handler.html#createAsync(android.os.Looper,%20android.os.Handler.Callback))`(`looper:` ` [Looper](https://developer.android.com/reference/kotlin/android/os/Looper.html#)`, `callback:` ` [Handler.Callback](https://developer.android.com/reference/kotlin/android/os/Handler.Callback.html#)`)` <br /> Create a new Handler whose posted messages and runnables are not subject to synchronization barriers such as display vsync. Messages sent to an async handler are guaranteed to be ordered with respect to one another, but not necessarily with respect to messages from other Handlers. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchMessage](https://developer.android.com/reference/kotlin/android/os/Handler.html#dispatchMessage(android.os.Message))`(`msg:` ` [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#)`)` <br /> Handle system messages here. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dump](https://developer.android.com/reference/kotlin/android/os/Handler.html#dump(android.util.Printer,%20kotlin.String))`(`pw:` ` [Printer](https://developer.android.com/reference/kotlin/android/util/Printer.html#)`, `prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` <br /> | | [Looper](https://developer.android.com/reference/kotlin/android/os/Looper.html#) | [getLooper](https://developer.android.com/reference/kotlin/android/os/Handler.html#getLooper())`()` <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getMessageName](https://developer.android.com/reference/kotlin/android/os/Handler.html#getMessageName(android.os.Message))`(`message:` ` [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#)`)` <br /> Returns a string representing the name of the specified message. The default implementation will either return the class name of the message callback if any, or the hexadecimal representation of the message "what" field. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasCallbacks](https://developer.android.com/reference/kotlin/android/os/Handler.html#hasCallbacks(java.lang.Runnable))`(`r:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)`)` <br /> Check if there are any pending posts of messages with callback r in the message queue. This operation is worst case O(n) in the number of messages in the queue, and should be avoided. Instead consider another mechanism outside of the queue to track if messages were enqueued and dispatched. For instance, maintain a counter, incrementing it when enqueuing a message and decrementing it when handling a message. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasMessages](https://developer.android.com/reference/kotlin/android/os/Handler.html#hasMessages(kotlin.Int))`(`what:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Check if there are any pending posts of messages with code 'what' in the message queue. This operation is worst case O(n) in the number of messages in the queue, and should be avoided. Instead consider another mechanism outside of the queue to track if messages were enqueued and dispatched. For instance, maintain a counter, incrementing it when enqueuing a message and decrementing it when handling a message. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasMessages](https://developer.android.com/reference/kotlin/android/os/Handler.html#hasMessages(kotlin.Int,%20kotlin.Any))`(`what:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `object:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Check if there are any pending posts of messages with code 'what' and whose obj is 'object' in the message queue. This operation is worst case O(n) in the number of messages in the queue, and should be avoided. Instead consider another mechanism outside of the queue to track if messages were enqueued and dispatched. For instance, maintain a counter, incrementing it when enqueuing a message and decrementing it when handling a message. <br /> | | [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#) | [obtainMessage](https://developer.android.com/reference/kotlin/android/os/Handler.html#obtainMessage())`()` <br /> Returns a new [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#) from the global message pool. More efficient than creating and allocating new instances. The retrieved message has its handler set to this instance (Message.target == this). If you don't want that facility, just call Message.obtain() instead. <br /> | | [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#) | [obtainMessage](https://developer.android.com/reference/kotlin/android/os/Handler.html#obtainMessage(kotlin.Int))`(`what:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Same as [obtainMessage()](https://developer.android.com/reference/kotlin/android/os/Handler.html#obtainMessage()), except that it also sets the what member of the returned Message. <br /> | | [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#) | [obtainMessage](https://developer.android.com/reference/kotlin/android/os/Handler.html#obtainMessage(kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`what:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `arg1:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `arg2:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Same as [obtainMessage()](https://developer.android.com/reference/kotlin/android/os/Handler.html#obtainMessage()), except that it also sets the what, arg1 and arg2 members of the returned Message. <br /> | | [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#) | [obtainMessage](https://developer.android.com/reference/kotlin/android/os/Handler.html#obtainMessage(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Any))`(`what:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `arg1:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `arg2:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Same as [obtainMessage()](https://developer.android.com/reference/kotlin/android/os/Handler.html#obtainMessage()), except that it also sets the what, obj, arg1,and arg2 values on the returned Message. <br /> | | [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#) | [obtainMessage](https://developer.android.com/reference/kotlin/android/os/Handler.html#obtainMessage(kotlin.Int,%20kotlin.Any))`(`what:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Same as [obtainMessage()](https://developer.android.com/reference/kotlin/android/os/Handler.html#obtainMessage()), except that it also sets the what and obj members of the returned Message. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [post](https://developer.android.com/reference/kotlin/android/os/Handler.html#post(java.lang.Runnable))`(`r:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)`)` <br /> Causes the Runnable r to be added to the message queue. The runnable will be run on the thread to which this handler is attached. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [postAtFrontOfQueue](https://developer.android.com/reference/kotlin/android/os/Handler.html#postAtFrontOfQueue(java.lang.Runnable))`(`r:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)`)` <br /> Posts a message to an object that implements Runnable. Causes the Runnable r to executed on the next iteration through the message queue. The runnable will be run on the thread to which this handler is attached.**This method is only for use in very special circumstances -- it can easily starve the message queue, cause ordering problems, or have other unexpected side-effects.** <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [postAtTime](https://developer.android.com/reference/kotlin/android/os/Handler.html#postAtTime(java.lang.Runnable,%20kotlin.Any,%20kotlin.Long))`(`r:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)`, `token:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`, `uptimeMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Causes the Runnable r to be added to the message queue, to be run at a specific time given by uptimeMillis.**The time-base is [android.os.SystemClock#uptimeMillis](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()).**Time spent in deep sleep will add an additional delay to execution. The runnable will be run on the thread to which this handler is attached. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [postAtTime](https://developer.android.com/reference/kotlin/android/os/Handler.html#postAtTime(java.lang.Runnable,%20kotlin.Long))`(`r:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)`, `uptimeMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Causes the Runnable r to be added to the message queue, to be run at a specific time given by uptimeMillis.**The time-base is [android.os.SystemClock#uptimeMillis](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()).**Time spent in deep sleep will add an additional delay to execution. The runnable will be run on the thread to which this handler is attached. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [postDelayed](https://developer.android.com/reference/kotlin/android/os/Handler.html#postDelayed(java.lang.Runnable,%20kotlin.Any,%20kotlin.Long))`(`r:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)`, `token:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`, `delayMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Causes the Runnable r to be added to the message queue, to be run after the specified amount of time elapses. The runnable will be run on the thread to which this handler is attached.**The time-base is [android.os.SystemClock#uptimeMillis](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()).**Time spent in deep sleep will add an additional delay to execution. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [postDelayed](https://developer.android.com/reference/kotlin/android/os/Handler.html#postDelayed(java.lang.Runnable,%20kotlin.Long))`(`r:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)`, `delayMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Causes the Runnable r to be added to the message queue, to be run after the specified amount of time elapses. The runnable will be run on the thread to which this handler is attached.**The time-base is [android.os.SystemClock#uptimeMillis](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()).**Time spent in deep sleep will add an additional delay to execution. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeCallbacks](https://developer.android.com/reference/kotlin/android/os/Handler.html#removeCallbacks(java.lang.Runnable))`(`r:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)`)` <br /> Remove any pending posts of Runnable r that are in the message queue. This operation is worst case O(n) in the number of messages in the queue, and should be avoided. Instead consider another mechanism outside of the queue to cancel a pending operation. For instance, maintain a flag to indicate whether the operation should be performed differently or not at all once it is dispatched. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeCallbacks](https://developer.android.com/reference/kotlin/android/os/Handler.html#removeCallbacks(java.lang.Runnable,%20kotlin.Any))`(`r:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)`, `token:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Remove any pending posts of Runnable r with Object token that are in the message queue. If token is null, all callbacks will be removed. This operation is worst case O(n) in the number of messages in the queue, and should be avoided. Instead consider another mechanism outside of the queue to cancel a pending operation. For instance, maintain a flag to indicate whether the operation should be performed differently or not at all once it is dispatched. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeCallbacksAndMessages](https://developer.android.com/reference/kotlin/android/os/Handler.html#removeCallbacksAndMessages(kotlin.Any))`(`token:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Remove any pending posts of callbacks and sent messages whose obj is token. If token is null, all callbacks and messages will be removed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeMessages](https://developer.android.com/reference/kotlin/android/os/Handler.html#removeMessages(kotlin.Int))`(`what:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Remove any pending posts of messages with code 'what' that are in the message queue. Note that \`Message#what\` is 0 unless otherwise set. When calling \`postMessage(Runnable)\` or \`postAtTime(Runnable, long)\`, the \`Runnable\` is internally wrapped with a \`Message\` whose \`what\` is 0. Calling \`removeMessages(0)\` will remove all messages without a \`what\`, including posted \`Runnable\`s. This operation is worst case O(n) in the number of messages in the queue, and should be avoided. Instead consider another mechanism outside of the queue to cancel a pending operation. For instance, maintain a flag to indicate whether the operation should be performed differently or not at all once it is dispatched. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeMessages](https://developer.android.com/reference/kotlin/android/os/Handler.html#removeMessages(kotlin.Int,%20kotlin.Any))`(`what:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `object:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Remove any pending posts of messages with code 'what' and whose obj is 'object' that are in the message queue. If object is null, all messages will be removed. This operation is worst case O(n) in the number of messages in the queue, and should be avoided. Instead consider another mechanism outside of the queue to cancel a pending operation. For instance, maintain a flag to indicate whether the operation should be performed differently or not at all once it is dispatched. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [sendEmptyMessage](https://developer.android.com/reference/kotlin/android/os/Handler.html#sendEmptyMessage(kotlin.Int))`(`what:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sends a Message containing only the what value. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [sendEmptyMessageAtTime](https://developer.android.com/reference/kotlin/android/os/Handler.html#sendEmptyMessageAtTime(kotlin.Int,%20kotlin.Long))`(`what:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `uptimeMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Sends a Message containing only the what value, to be delivered at a specific time. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [sendEmptyMessageDelayed](https://developer.android.com/reference/kotlin/android/os/Handler.html#sendEmptyMessageDelayed(kotlin.Int,%20kotlin.Long))`(`what:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `delayMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Sends a Message containing only the what value, to be delivered after the specified amount of time elapses. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [sendMessage](https://developer.android.com/reference/kotlin/android/os/Handler.html#sendMessage(android.os.Message))`(`msg:` ` [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#)`)` <br /> Pushes a message onto the end of the message queue after all pending messages before the current time. It will be received in [handleMessage](https://developer.android.com/reference/kotlin/android/os/Handler.html#handleMessage(android.os.Message)), in the thread attached to this handler. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [sendMessageAtFrontOfQueue](https://developer.android.com/reference/kotlin/android/os/Handler.html#sendMessageAtFrontOfQueue(android.os.Message))`(`msg:` ` [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#)`)` <br /> Enqueue a message at the front of the message queue, to be processed on the next iteration of the message loop. You will receive it in [handleMessage](https://developer.android.com/reference/kotlin/android/os/Handler.html#handleMessage(android.os.Message)), in the thread attached to this handler.**This method is only for use in very special circumstances -- it can easily starve the message queue, cause ordering problems, or have other unexpected side-effects.** <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [sendMessageAtTime](https://developer.android.com/reference/kotlin/android/os/Handler.html#sendMessageAtTime(android.os.Message,%20kotlin.Long))`(`msg:` ` [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#)`, `uptimeMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Enqueue a message into the message queue after all pending messages before the absolute time (in milliseconds) uptimeMillis.**The time-base is [android.os.SystemClock#uptimeMillis](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()).** Time spent in deep sleep will add an additional delay to execution. You will receive it in [handleMessage](https://developer.android.com/reference/kotlin/android/os/Handler.html#handleMessage(android.os.Message)), in the thread attached to this handler. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [sendMessageDelayed](https://developer.android.com/reference/kotlin/android/os/Handler.html#sendMessageDelayed(android.os.Message,%20kotlin.Long))`(`msg:` ` [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#)`, `delayMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Enqueue a message into the message queue after all pending messages before (current time + delayMillis). You will receive it in [handleMessage](https://developer.android.com/reference/kotlin/android/os/Handler.html#handleMessage(android.os.Message)), in the thread attached to this handler. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/os/Handler.html#toString())`()` <br /> | ||

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
| `msg` | [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#):This value cannot be`null`. |

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

This method begins an asynchronous delete. When the delete operation is done [onDeleteComplete](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler#onDeleteComplete(kotlin.Int,%20kotlin.Any,%20kotlin.Int))is called.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `token` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A token passed into [onDeleteComplete](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler#onDeleteComplete(kotlin.Int,%20kotlin.Any,%20kotlin.Int))to identify the delete operation. |
| `cookie` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:An object that gets passed into [onDeleteComplete](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler#onDeleteComplete(kotlin.Int,%20kotlin.Any,%20kotlin.Int)) |
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!:the Uri passed to the delete operation. |
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

This method begins an asynchronous insert. When the insert operation is done [onInsertComplete](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler#onInsertComplete(kotlin.Int,%20kotlin.Any,%20android.net.Uri))is called.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `token` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A token passed into [onInsertComplete](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler#onInsertComplete(kotlin.Int,%20kotlin.Any,%20android.net.Uri))to identify the insert operation. |
| `cookie` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:An object that gets passed into [onInsertComplete](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler#onInsertComplete(kotlin.Int,%20kotlin.Any,%20android.net.Uri)) |
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!:the Uri passed to the insert operation. |
| `initialValues` | [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)!:the ContentValues parameter passed to the insert operation. |

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

This method begins an asynchronous query. When the query is done [onQueryComplete](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler#onQueryComplete(kotlin.Int,%20kotlin.Any,%20android.database.Cursor))is called.

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `token` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A token passed into [onQueryComplete](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler#onQueryComplete(kotlin.Int,%20kotlin.Any,%20android.database.Cursor))to identify the query. |
| `cookie` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:An object that gets passed into [onQueryComplete](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler#onQueryComplete(kotlin.Int,%20kotlin.Any,%20android.database.Cursor)) |
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!:The URI, using the content:// scheme, for the content to retrieve. |
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:A list of which columns to return. Passing null will return all columns, which is discouraged to prevent reading data from storage that isn't going to be used. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A filter declaring which rows to return, formatted as an SQL WHERE clause (excluding the WHERE itself). Passing null will return all rows for the given URI. |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:You may include ?s in selection, which will be replaced by the values from selectionArgs, in the order that they appear in the selection. The values will be bound as Strings. |
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

This method begins an asynchronous update. When the update operation is done [onUpdateComplete](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler#onUpdateComplete(kotlin.Int,%20kotlin.Any,%20kotlin.Int))is called.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `token` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A token passed into [onUpdateComplete](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler#onUpdateComplete(kotlin.Int,%20kotlin.Any,%20kotlin.Int))to identify the update operation. |
| `cookie` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:An object that gets passed into [onUpdateComplete](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler#onUpdateComplete(kotlin.Int,%20kotlin.Any,%20kotlin.Int)) |
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!:the Uri passed to the update operation. |
| `values` | [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)!:the ContentValues parameter passed to the update operation. |

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
| `token` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the token to identify the query, passed in from [startDelete](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler#startDelete(kotlin.Int,%20kotlin.Any,%20android.net.Uri,%20kotlin.String,%20kotlin.Array)). |
| `cookie` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the cookie object that's passed in from [startDelete](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler#startDelete(kotlin.Int,%20kotlin.Any,%20android.net.Uri,%20kotlin.String,%20kotlin.Array)). |
| `result` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the result returned from the delete operation |

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
| `token` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the token to identify the query, passed in from [startInsert](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler#startInsert(kotlin.Int,%20kotlin.Any,%20android.net.Uri,%20android.content.ContentValues)). |
| `cookie` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the cookie object that's passed in from [startInsert](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler#startInsert(kotlin.Int,%20kotlin.Any,%20android.net.Uri,%20android.content.ContentValues)). |
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!:the uri returned from the insert operation. |

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
| `token` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the token to identify the query, passed in from [startQuery](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler#startQuery(kotlin.Int,%20kotlin.Any,%20android.net.Uri,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String)). |
| `cookie` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the cookie object passed in from [startQuery](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler#startQuery(kotlin.Int,%20kotlin.Any,%20android.net.Uri,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String)). |
| `cursor` | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!:The cursor holding the results from the query. |

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
| `token` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the token to identify the query, passed in from [startUpdate](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler#startUpdate(kotlin.Int,%20kotlin.Any,%20android.net.Uri,%20android.content.ContentValues,%20kotlin.String,%20kotlin.Array)). |
| `cookie` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the cookie object that's passed in from [startUpdate](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler#startUpdate(kotlin.Int,%20kotlin.Any,%20android.net.Uri,%20android.content.ContentValues,%20kotlin.String,%20kotlin.Array)). |
| `result` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the result returned from the update operation |
