# Looper

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Looper

Kotlin| [Java](https://developer.android.com/reference/android/os/Looper "View this page in Java") 
| --- | --- |

```
class Looper
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.Looper](https://developer.android.com/reference/kotlin/android/os/Looper#) |

Class used to run a message loop for a thread. Threads by default do not have a message loop associated with them; to create one, call [prepare](https://developer.android.com/reference/kotlin/android/os/Looper#prepare())in the thread that is to run the loop, and then [loop](https://developer.android.com/reference/kotlin/android/os/Looper#loop())to have it process messages until the loop is stopped.

Most interaction with a message loop is through the [Handler](https://developer.android.com/reference/kotlin/android/os/Handler) class.

This is a typical example of the implementation of a Looper thread, using the separation of [prepare](https://developer.android.com/reference/kotlin/android/os/Looper#prepare())and [loop](https://developer.android.com/reference/kotlin/android/os/Looper#loop())to create an initial Handler to communicate with the Looper. 

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
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dump](https://developer.android.com/reference/kotlin/android/os/Looper#dump(android.util.Printer,%20kotlin.String))`(`pw:` ` [Printer](https://developer.android.com/reference/kotlin/android/util/Printer.html#)`, `prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Dumps the state of the looper for debugging purposes. |
| static [Looper](https://developer.android.com/reference/kotlin/android/os/Looper#)! | [getMainLooper](https://developer.android.com/reference/kotlin/android/os/Looper#getMainLooper())`()` Returns the application's main looper, which lives in the main thread of the application. |
| [MessageQueue](https://developer.android.com/reference/kotlin/android/os/MessageQueue) | [getQueue](https://developer.android.com/reference/kotlin/android/os/Looper#getQueue())`()` Gets this looper's message queue. |
| --- | --- |
| [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread.html#) | [getThread](https://developer.android.com/reference/kotlin/android/os/Looper#getThread())`()` Gets the Thread associated with this Looper. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCurrentThread](https://developer.android.com/reference/kotlin/android/os/Looper#isCurrentThread())`()` Returns true if the current thread is this looper's thread. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [loop](https://developer.android.com/reference/kotlin/android/os/Looper#loop())`()` Run the message queue in this thread. |
| --- | --- |
| static [Looper](https://developer.android.com/reference/kotlin/android/os/Looper#)? | [myLooper](https://developer.android.com/reference/kotlin/android/os/Looper#myLooper())`()` Return the Looper object associated with the current thread. |
| static [MessageQueue](https://developer.android.com/reference/kotlin/android/os/MessageQueue) | [myQueue](https://developer.android.com/reference/kotlin/android/os/Looper#myQueue())`()` Return the [MessageQueue](https://developer.android.com/reference/kotlin/android/os/MessageQueue) object associated with the current thread. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [prepare](https://developer.android.com/reference/kotlin/android/os/Looper#prepare())`()` Initialize the current thread as a looper. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [prepareMainLooper](https://developer.android.com/reference/kotlin/android/os/Looper#prepareMainLooper())`()` Initialize the current thread as a looper, marking it as an application's main looper. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [quit](https://developer.android.com/reference/kotlin/android/os/Looper#quit())`()` Quits the looper. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [quitSafely](https://developer.android.com/reference/kotlin/android/os/Looper#quitSafely())`()` Quits the looper safely. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMessageLogging](https://developer.android.com/reference/kotlin/android/os/Looper#setMessageLogging(android.util.Printer))`(`printer:` ` [Printer](https://developer.android.com/reference/kotlin/android/util/Printer.html#)?`)` Control logging of messages as they are processed by this Looper. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/os/Looper#toString())`()` <br /> |

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
| `pw` | [Printer](https://developer.android.com/reference/kotlin/android/util/Printer.html#):A printer to receive the contents of the dump. This value cannot be`null`. |
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
| [MessageQueue](https://developer.android.com/reference/kotlin/android/os/MessageQueue) | The looper's message queue. This value cannot be`null`. |

### getThread

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getThread(): Thread
```

Gets the Thread associated with this Looper.

| Return ||
|---------------------------------------------------------------------------------|--------------------------------------------------|
| [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread.html#) | The looper's thread. This value cannot be`null`. |

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

Run the message queue in this thread. Be sure to call [quit()](https://developer.android.com/reference/kotlin/android/os/Looper#quit())to end the loop. 

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

Return the [MessageQueue](https://developer.android.com/reference/kotlin/android/os/MessageQueue) object associated with the current thread. This must be called from a thread running a Looper, or a NullPointerException will be thrown.

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [MessageQueue](https://developer.android.com/reference/kotlin/android/os/MessageQueue) | This value cannot be`null`. |

### prepare

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun prepare(): Unit
```

Initialize the current thread as a looper. This gives you a chance to create handlers that then reference this looper, before actually starting the loop. Be sure to call [loop()](https://developer.android.com/reference/kotlin/android/os/Looper#loop())after calling this method, and end it by calling [quit()](https://developer.android.com/reference/kotlin/android/os/Looper#quit()). 

### prepareMainLooper

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun prepareMainLooper(): Unit
```

**Deprecated:** *The main looper for your application is created by the Android environment, so you should never need to call this function yourself.*

Initialize the current thread as a looper, marking it as an application's main looper. See also: [prepare()](https://developer.android.com/reference/kotlin/android/os/Looper#prepare()) 

### quit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun quit(): Unit
```

Quits the looper.

Causes the [loop](https://developer.android.com/reference/kotlin/android/os/Looper#loop())method to terminate without processing any more messages in the message queue.

Any attempt to post messages to the queue after the looper is asked to quit will fail. For example, the [Handler.sendMessage(Message)](https://developer.android.com/reference/kotlin/android/os/Handler#sendMessage(android.os.Message))method will return false.

If [quit](https://developer.android.com/reference/kotlin/android/os/Looper#quit())or [quitSafely](https://developer.android.com/reference/kotlin/android/os/Looper#quitSafely())is called multiple times, the first call will have an effect and the subsequent calls will be no-ops.

Using this method may be unsafe because some messages may not be delivered before the looper terminates. Consider using [quitSafely](https://developer.android.com/reference/kotlin/android/os/Looper#quitSafely())instead to ensure that all pending work is completed in an orderly manner. 
**See Also**

- [#quitSafely](https://developer.android.com/reference/kotlin/android/os/Looper#quitSafely()) 

### quitSafely

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun quitSafely(): Unit
```

Quits the looper safely.

Causes the [loop](https://developer.android.com/reference/kotlin/android/os/Looper#loop())method to terminate as soon as all remaining messages in the message queue that are already due to be delivered have been handled. However pending delayed messages with due times in the future will not be delivered before the loop terminates.

Any attempt to post messages to the queue after the looper is asked to quit will fail. For example, the [Handler.sendMessage(Message)](https://developer.android.com/reference/kotlin/android/os/Handler#sendMessage(android.os.Message))method will return false.

If [quit](https://developer.android.com/reference/kotlin/android/os/Looper#quit())or [quitSafely](https://developer.android.com/reference/kotlin/android/os/Looper#quitSafely())is called multiple times, the first call will have an effect and the subsequent calls will be no-ops. 

### setMessageLogging

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setMessageLogging(printer: Printer?): Unit
```

Control logging of messages as they are processed by this Looper. If enabled, a log message will be written to printer at the beginning and ending of each message dispatch, identifying the target Handler and message contents. Message logging introduces a performance penalty, and is disabled by default.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `printer` | [Printer](https://developer.android.com/reference/kotlin/android/util/Printer.html#)?:A Printer object that will receive log messages, or null to disable message logging. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
