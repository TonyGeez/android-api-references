# Looper

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Looper

Kotlin| [Java](Looper.md) 
| --- | --- |

```
class Looper
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.Looper](Looper.md) |

Class used to run a message loop for a thread. Threads by default do not have a message loop associated with them; to create one, call [prepare](Looper.md))in the thread that is to run the loop, and then [loop](Looper.md))to have it process messages until the loop is stopped.

Most interaction with a message loop is through the [Handler](Handler.md) class.

This is a typical example of the implementation of a Looper thread, using the separation of [prepare](Looper.md))and [loop](Looper.md))to create an initial Handler to communicate with the Looper. 

```kotlin
class LooperThread extends Thread {
       public Handler mHandler;
 
       public void run() {
           Looper.prepare();
 
           mHandler = new Handler(Looper.myLooper()) {
               public void handleMessage(Message msg) {
                   // process incoming messages here
               }
           };
 
           Looper.loop();
       }
   }
```

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dump](Looper.md))`(`pw:` ` [Printer](../android.util/Printer.md)`, `prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Dumps the state of the looper for debugging purposes. |
| static [Looper](Looper.md)! | [getMainLooper](Looper.md))`()` Returns the application's main looper, which lives in the main thread of the application. |
| [MessageQueue](MessageQueue.md) | [getQueue](Looper.md))`()` Gets this looper's message queue. |
| --- | --- |
| [Thread](../java.lang/Thread.md) | [getThread](Looper.md))`()` Gets the Thread associated with this Looper. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCurrentThread](Looper.md))`()` Returns true if the current thread is this looper's thread. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [loop](Looper.md))`()` Run the message queue in this thread. |
| --- | --- |
| static [Looper](Looper.md)? | [myLooper](Looper.md))`()` Return the Looper object associated with the current thread. |
| static [MessageQueue](MessageQueue.md) | [myQueue](Looper.md))`()` Return the [MessageQueue](MessageQueue.md) object associated with the current thread. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [prepare](Looper.md))`()` Initialize the current thread as a looper. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [prepareMainLooper](Looper.md))`()` Initialize the current thread as a looper, marking it as an application's main looper. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [quit](Looper.md))`()` Quits the looper. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [quitSafely](Looper.md))`()` Quits the looper safely. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMessageLogging](Looper.md))`(`printer:` ` [Printer](../android.util/Printer.md)?`)` Control logging of messages as they are processed by this Looper. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](Looper.md))`()` <br /> |

## Public methods

### dump

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun dump(
    pw: Printer, 
    prefix: String
): Unit
```

Dumps the state of the looper for debugging purposes.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pw` | [Printer](../android.util/Printer.md):A printer to receive the contents of the dump. This value cannot be`null`. |
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):A prefix to prepend to each line which is printed. This value cannot be`null`. |

### getMainLooper

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getMainLooper(): Looper!
```

Returns the application's main looper, which lives in the main thread of the application. 

### getQueue

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getQueue(): MessageQueue
```

Gets this looper's message queue.

| Return ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------|
| [MessageQueue](MessageQueue.md) | The looper's message queue. This value cannot be`null`. |

### getThread

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getThread(): Thread
```

Gets the Thread associated with this Looper.

| Return ||
|---------------------------------------------------------------------------------|--------------------------------------------------|
| [Thread](../java.lang/Thread.md) | The looper's thread. This value cannot be`null`. |

### isCurrentThread

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isCurrentThread(): Boolean
```

Returns true if the current thread is this looper's thread. 

### loop

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun loop(): Unit
```

Run the message queue in this thread. Be sure to call [quit()](Looper.md))to end the loop. 

### myLooper

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun myLooper(): Looper?
```

Return the Looper object associated with the current thread. Returns null if the calling thread is not associated with a Looper. 

### myQueue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun myQueue(): MessageQueue
```

Return the [MessageQueue](MessageQueue.md) object associated with the current thread. This must be called from a thread running a Looper, or a NullPointerException will be thrown.

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [MessageQueue](MessageQueue.md) | This value cannot be`null`. |

### prepare

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun prepare(): Unit
```

Initialize the current thread as a looper. This gives you a chance to create handlers that then reference this looper, before actually starting the loop. Be sure to call [loop()](Looper.md))after calling this method, and end it by calling [quit()](Looper.md)). 

### prepareMainLooper

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun prepareMainLooper(): Unit
```

**Deprecated:** *The main looper for your application is created by the Android environment, so you should never need to call this function yourself.*

Initialize the current thread as a looper, marking it as an application's main looper. See also: [prepare()](Looper.md)) 

### quit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun quit(): Unit
```

Quits the looper.

Causes the [loop](Looper.md))method to terminate without processing any more messages in the message queue.

Any attempt to post messages to the queue after the looper is asked to quit will fail. For example, the [Handler.sendMessage(Message)](Handler.md))method will return false.

If [quit](Looper.md))or [quitSafely](Looper.md))is called multiple times, the first call will have an effect and the subsequent calls will be no-ops.

Using this method may be unsafe because some messages may not be delivered before the looper terminates. Consider using [quitSafely](Looper.md))instead to ensure that all pending work is completed in an orderly manner. 
**See Also**

- [#quitSafely](Looper.md)) 

### quitSafely

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun quitSafely(): Unit
```

Quits the looper safely.

Causes the [loop](Looper.md))method to terminate as soon as all remaining messages in the message queue that are already due to be delivered have been handled. However pending delayed messages with due times in the future will not be delivered before the loop terminates.

Any attempt to post messages to the queue after the looper is asked to quit will fail. For example, the [Handler.sendMessage(Message)](Handler.md))method will return false.

If [quit](Looper.md))or [quitSafely](Looper.md))is called multiple times, the first call will have an effect and the subsequent calls will be no-ops. 

### setMessageLogging

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setMessageLogging(printer: Printer?): Unit
```

Control logging of messages as they are processed by this Looper. If enabled, a log message will be written to printer at the beginning and ending of each message dispatch, identifying the target Handler and message contents. Message logging introduces a performance penalty, and is disabled by default.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `printer` | [Printer](../android.util/Printer.md)?:A Printer object that will receive log messages, or null to disable message logging. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
