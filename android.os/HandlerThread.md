Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HandlerThread

```
open class HandlerThread : Thread
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.lang.Thread](../java/lang/Thread.md) ||
| | ↳ | [android.os.HandlerThread](../android/os/HandlerThread.md) |

A `https://developer.android.com/reference/kotlin/java/lang/Thread.html#` that has a `https://developer.android.com/reference/kotlin/android/os/Looper`. The `https://developer.android.com/reference/kotlin/android/os/Looper` can then be used to create `https://developer.android.com/reference/kotlin/android/os/Handler`s. Just like with a regular `https://developer.android.com/reference/kotlin/java/lang/Thread.html#`, `https://developer.android.com/reference/kotlin/java/lang/Thread.html#start()` must still be called.

*Use this class only if you must work with the `https://developer.android.com/reference/kotlin/android/os/Handler` API and need a `https://developer.android.com/reference/kotlin/java/lang/Thread.html#` to do the handling on that is not an existing `https://developer.android.com/reference/kotlin/android/os/Looper` thread, such as `https://developer.android.com/reference/kotlin/android/os/Looper#getMainLooper()`.* Otherwise, prefer `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` or `https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService.html#`, or Kotlin [coroutines](https://developer.android.com/topic/libraries/architecture/coroutines).

Note that many APIs that required a `https://developer.android.com/reference/kotlin/android/os/Handler` in older SDK versions offer a newer alternative that accepts an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` instead. Always prefer to use the newer API if available.

## Alternatives to `HandlerThread`

`https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`s offer more flexibility with regards to threading. Work submitted to an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` can be set to run on another thread, on one of several threads from a static or dynamic pool, or on the caller's thread, depending on your needs.

{link @link java.util.concurrent.Executor} offers a simpler API that is easier to use compared to `https://developer.android.com/reference/kotlin/android/os/Handler`. {link @link java.util.concurrent.ExecutorService} offers the richer `https://developer.android.com/reference/kotlin/java/util/concurrent/Future.html#` API, which you can use to monitor task status, cancel tasks, propagate exceptions, and chain multiple pending tasks.

{link @link java.util.concurrent.Executors} is a factory for various `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`s that meet common concurrency needs. These `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`s use work queues that offer better concurrency and reduced contention than `HandlerThread`.

On Kotlin, [coroutines](https://developer.android.com/topic/libraries/architecture/coroutines) may be used to handle concurrency.

## Common `HandlerThread` performance issues

Apps that use `HandlerThread` may encounter the following performance issues:

- **Excessive thread creation** : A `HandlerThread` is a `https://developer.android.com/reference/kotlin/java/lang/Thread.html#`. Every system thread costs some resident memory, whether it is working or if it's idle. If your app has a large number of `HandlerThread`s each dedicated to a single type of task, rather than for instance a `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor.html#` that can grow and shrink in size according to demand, then the additional idle `HandlerThread`s will be wasting memory.
- **Lock contention** : `HandlerThread` uses a `https://developer.android.com/reference/kotlin/android/os/Looper` which in turn uses a `https://developer.android.com/reference/kotlin/android/os/MessageQueue`. `https://developer.android.com/reference/kotlin/android/os/MessageQueue` uses a single lock to synchronize access to its underlying queue. Any threads attempting to enqueue messages at the same time, and the `HandlerThread` itself when attempting to dequeue the next message to handle, will block each other.
- **Priority inversion** : A high-priority `HandlerThread` can become blocked by a lower-priority thread, for instance if the former is trying to enqueue a message while the latter is trying to dequeue the next message to handle, or vice versa.

The best way to avoid these issues is to use `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`s or [Kotlin coroutines](https://developer.android.com/topic/libraries/architecture/coroutines) instead of `HandlerThread`.

## Summary

Inherited constants From class `https://developer.android.com/reference/kotlin/java/lang/Thread.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#MAX_PRIORITY:kotlin.Int`

The maximum priority that a thread can have.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#MIN_PRIORITY:kotlin.Int`

The minimum priority that a thread can have.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#NORM_PRIORITY:kotlin.Int`

The default priority that is assigned to a thread.

<br />

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/HandlerThread#HandlerThread(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` <br /> |
| `https://developer.android.com/reference/kotlin/android/os/HandlerThread#HandlerThread(kotlin.String,%20kotlin.Int)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, linuxPriority: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Constructs a HandlerThread. |

| Public methods ||
|---|---|
| open [Looper](../android/os/Looper.md)! | `https://developer.android.com/reference/kotlin/android/os/HandlerThread#getLooper()()` This method returns the Looper associated with this thread. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/HandlerThread#getThreadId()()` Returns the identifier of this thread. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/HandlerThread#quit()()` Quits the handler thread's looper. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/HandlerThread#quitSafely()()` Quits the handler thread's looper safely. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/HandlerThread#run()()` If this thread was constructed using a separate `Runnable` run object, then that `Runnable` object's `run` method is called; otherwise, this method does nothing and returns. |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/HandlerThread#onLooperPrepared()()` Call back method that can be explicitly overridden if needed to execute some setup before Looper loops. |

Inherited functions From class `https://developer.android.com/reference/kotlin/java/lang/Thread.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#activeCount()()`

Returns an estimate of the number of active threads in the current thread's [thread group](../java/lang/ThreadGroup.md) and its subgroups. Recursively iterates over all subgroups in the current thread's thread group.

The value returned is only an estimate because the number of threads may change dynamically while this method traverses internal data structures, and might be affected by the presence of certain system threads. This method is intended primarily for debugging and monitoring purposes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#checkAccess()()`

Determines if the currently running thread has permission to modify this thread.

If there is a security manager, its `checkAccess` method is called with this thread as its argument. This may result in throwing a `SecurityException`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#clone()()`

Throws CloneNotSupportedException as a Thread can not be meaningfully cloned. Construct a new Thread instead.

<br />

`https://developer.android.com/reference/kotlin/java/lang/Thread.html#` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#currentThread()()`

Returns a reference to the currently executing thread object.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#dumpStack()()`

Prints a stack trace of the current thread to the standard error stream. This method is used only for debugging.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#enumerate(kotlin.Array)(tarray: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/lang/Thread.html#!>!)`

Copies into the specified array every active thread in the current thread's thread group and its subgroups. This method simply invokes the `https://developer.android.com/reference/kotlin/java/lang/ThreadGroup.html#enumerate(kotlin.Array)` method of the current thread's thread group.

An application might use the [activeCount](../java/lang/Thread.md)) method to get an estimate of how big the array should be, however *if the array is too short to hold all the threads, the extra threads are silently ignored.* If it is critical to obtain every active thread in the current thread's thread group and its subgroups, the invoker should verify that the returned int value is strictly less than the length of `tarray`.

Due to the inherent race condition in this method, it is recommended that the method only be used for debugging and monitoring purposes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://developer.android.com/reference/kotlin/java/lang/Thread.html#!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/lang/StackTraceElement.html#!>!>` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#getAllStackTraces()()`

Returns a map of stack traces for all live threads. The map keys are threads and each map value is an array of `StackTraceElement` that represents the stack dump of the corresponding `Thread`. The returned stack traces are in the format specified for the `https://developer.android.com/reference/kotlin/java/lang/Thread.html#getStackTrace()` method.

The threads may be executing while this method is called. The stack trace of each thread only represents a snapshot and each stack trace may be obtained at different time. A zero-length array will be returned in the map value if the virtual machine has no stack trace information about a thread.

<br />

`https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#?` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#getContextClassLoader()()`

Returns the context `ClassLoader` for this thread. The context `ClassLoader` is provided by the creator of the thread for use by code running in this thread when loading classes and resources. If not [set](../java/lang/Thread.md)), the default is the `ClassLoader` context of the parent thread. The context `ClassLoader` of the primordial thread is typically set to the class loader used to load the application.

<br />

`https://developer.android.com/reference/kotlin/java/lang/Thread.UncaughtExceptionHandler.html#?` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#getDefaultUncaughtExceptionHandler()()`

Returns the default handler invoked when a thread abruptly terminates due to an uncaught exception. If the returned value is `null`, there is no default.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#getId()()`

Returns the identifier of this Thread. The thread ID is a positive `long` number generated when this thread was created. The thread ID is unique and remains unchanged during its lifetime. When a thread is terminated, this thread ID may be reused.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#getName()()`

Returns this thread's name.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#getPriority()()`

Returns this thread's priority.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/lang/StackTraceElement.html#!>` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#getStackTrace()()`

Returns an array of stack trace elements representing the stack dump of this thread. This method will return a zero-length array if this thread has not started, has started but has not yet been scheduled to run by the system, or has terminated. If the returned array is of non-zero length then the first element of the array represents the top of the stack, which is the most recent method invocation in the sequence. The last element of the array represents the bottom of the stack, which is the least recent method invocation in the sequence.

If there is a security manager, and this thread is not the current thread, then the security manager's `checkPermission` method is called with a `RuntimePermission("getStackTrace")` permission to see if it's ok to get the stack trace.

Some virtual machines may, under some circumstances, omit one or more stack frames from the stack trace. In the extreme case, a virtual machine that has no stack trace information concerning this thread is permitted to return a zero-length array from this method.

<br />

`https://developer.android.com/reference/kotlin/java/lang/Thread.State.html#` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#getState()()`

Returns the state of this thread. This method is designed for use in monitoring of the system state, not for synchronization control.

<br />

`https://developer.android.com/reference/kotlin/java/lang/ThreadGroup.html#?` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#getThreadGroup()()`

Returns the thread group to which this thread belongs. This method returns null if this thread has died (been stopped).

<br />

`https://developer.android.com/reference/kotlin/java/lang/Thread.UncaughtExceptionHandler.html#?` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#getUncaughtExceptionHandler()()`

Returns the handler invoked when this thread abruptly terminates due to an uncaught exception. If this thread has not had an uncaught exception handler explicitly set then this thread's `ThreadGroup` object is returned, unless this thread has terminated, in which case `null` is returned.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#holdsLock(kotlin.Any)(obj: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`

Returns `true` if and only if the current thread holds the monitor lock on the specified object.

This method is designed to allow a program to assert that the current thread already holds a specified lock:

```kotlin
assert Thread.holdsLock(obj);
  
```

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#interrupt()()`

Interrupts this thread.

Unless the current thread is interrupting itself, which is always permitted, the `https://developer.android.com/reference/kotlin/java/lang/Thread.html#checkAccess()` method of this thread is invoked, which may cause a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` to be thrown.

If this thread is blocked in an invocation of the `https://developer.android.com/reference/kotlin/java/lang/Object.html#wait()`, `https://developer.android.com/reference/kotlin/java/lang/Object.html#wait(kotlin.Long)`, or `https://developer.android.com/reference/kotlin/java/lang/Object.html#wait(kotlin.Long,%20kotlin.Int)` methods of the `https://developer.android.com/reference/kotlin/java/lang/Object.html#` class, or of the `https://developer.android.com/reference/kotlin/java/lang/Thread.html#join()`, `https://developer.android.com/reference/kotlin/java/lang/Thread.html#join(kotlin.Long)`, `https://developer.android.com/reference/kotlin/java/lang/Thread.html#join(kotlin.Long,%20kotlin.Int)`, `https://developer.android.com/reference/kotlin/java/lang/Thread.html#sleep(kotlin.Long)`, or `https://developer.android.com/reference/kotlin/java/lang/Thread.html#sleep(kotlin.Long,%20kotlin.Int)` methods of this class, then its interrupt status will be cleared and it will receive an `https://developer.android.com/reference/kotlin/java/lang/InterruptedException.html#`.

If this thread is blocked in an I/O operation upon an `https://developer.android.com/reference/kotlin/java/nio/channels/InterruptibleChannel.html#` then the channel will be closed, the thread's interrupt status will be set, and the thread will receive a `https://developer.android.com/reference/kotlin/java/nio/channels/ClosedByInterruptException.html#`.

If this thread is blocked in a `https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#` then the thread's interrupt status will be set and it will return immediately from the selection operation, possibly with a non-zero value, just as if the selector's `https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#wakeup()` method were invoked.

If none of the previous conditions hold then this thread's interrupt status will be set.

Interrupting a thread that is not alive need not have any effect.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#interrupted()()`

Tests whether the current thread has been interrupted. The *interrupted status* of the thread is cleared by this method. In other words, if this method were to be called twice in succession, the second call would return false (unless the current thread were interrupted again, after the first call had cleared its interrupted status and before the second call had examined it).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#isAlive()()`

Tests if this thread is alive. A thread is alive if it has been started and has not yet terminated.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#isDaemon()()`

Tests if this thread is a daemon thread.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#isInterrupted()()`

Tests whether this thread has been interrupted. The *interrupted status* of the thread is unaffected by this method.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#isVirtual()()`

Returns `true` if this thread is a virtual thread. A virtual thread is scheduled by the Java virtual machine rather than the operating system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#join()()`

Waits for this thread to die.

An invocation of this method behaves in exactly the same way as the invocation
[join](../java/lang/Thread.md))`(0)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#join(java.time.Duration)(duration: https://developer.android.com/reference/kotlin/java/time/Duration.html#!)`

Waits for this thread to terminate for up to the given waiting duration.

This method does not wait if the duration to wait is less than or equal to zero. In this case, the method just tests if the thread has terminated.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#join(kotlin.Long)(millis: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`

Waits at most `millis` milliseconds for this thread to die. A timeout of `0` means to wait forever.

This implementation uses a loop of `this.wait` calls conditioned on `this.isAlive`. As a thread terminates the `this.notifyAll` method is invoked. It is recommended that applications not use `wait`, `notify`, or `notifyAll` on `Thread` instances.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#join(kotlin.Long,%20kotlin.Int)(millis: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, nanos: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Waits at most `millis` milliseconds plus `nanos` nanoseconds for this thread to die. If both arguments are `0`, it means to wait forever.

This implementation uses a loop of `this.wait` calls conditioned on `this.isAlive`. As a thread terminates the `this.notifyAll` method is invoked. It is recommended that applications not use `wait`, `notify`, or `notifyAll` on `Thread` instances.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#onSpinWait()()`

Indicates that the caller is momentarily unable to progress, until the occurrence of one or more actions on the part of other activities. By invoking this method within each iteration of a spin-wait loop construct, the calling thread indicates to the runtime that it is busy-waiting. The runtime may take action to improve the performance of invoking spin-wait loop constructions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#setContextClassLoader(java.lang.ClassLoader)(cl: https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#?)`

Sets the context ClassLoader for this Thread. The context ClassLoader can be set when a thread is created, and allows the creator of the thread to provide the appropriate class loader, through `getContextClassLoader`, to code running in the thread when loading classes and resources.

If a security manager is present, its `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkPermission(java.security.Permission)` method is invoked with a `https://developer.android.com/reference/kotlin/java/lang/RuntimePermission.html#``("setContextClassLoader")` permission to see if setting the context ClassLoader is permitted.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#setDaemon(kotlin.Boolean)(on: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Marks this thread as either a [daemon](../java/lang/Thread.md)) thread or a user thread. The Java Virtual Machine exits when the only threads running are all daemon threads.

This method must be invoked before the thread is started.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#setDefaultUncaughtExceptionHandler(java.lang.Thread.UncaughtExceptionHandler)(eh: https://developer.android.com/reference/kotlin/java/lang/Thread.UncaughtExceptionHandler.html#?)`

Set the default handler invoked when a thread abruptly terminates due to an uncaught exception, and no other handler has been defined for that thread.

Uncaught exception handling is controlled first by the thread, then by the thread's `https://developer.android.com/reference/kotlin/java/lang/ThreadGroup.html#` object and finally by the default uncaught exception handler. If the thread does not have an explicit uncaught exception handler set, and the thread's thread group (including parent thread groups) does not specialize its `uncaughtException` method, then the default handler's `uncaughtException` method will be invoked.

By setting the default uncaught exception handler, an application can change the way in which uncaught exceptions are handled (such as logging to a specific device, or file) for those threads that would already accept whatever "default" behavior the system provided.

Note that the default uncaught exception handler should not usually defer to the thread's `ThreadGroup` object, as that could cause infinite recursion.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#setName(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Changes the name of this thread to be equal to the argument `name`.

First the `checkAccess` method of this thread is called with no arguments. This may result in throwing a `SecurityException`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#setPriority(kotlin.Int)(newPriority: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Changes the priority of this thread.

First the `checkAccess` method of this thread is called with no arguments. This may result in throwing a `SecurityException`.

Otherwise, the priority of this thread is set to the smaller of the specified `newPriority` and the maximum permitted priority of the thread's thread group.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#setUncaughtExceptionHandler(java.lang.Thread.UncaughtExceptionHandler)(eh: https://developer.android.com/reference/kotlin/java/lang/Thread.UncaughtExceptionHandler.html#?)`

Set the handler invoked when this thread abruptly terminates due to an uncaught exception.

A thread can take full control of how it responds to uncaught exceptions by having its uncaught exception handler explicitly set. If no such handler is set then the thread's `ThreadGroup` object acts as its handler.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#sleep(java.time.Duration)(duration: https://developer.android.com/reference/kotlin/java/time/Duration.html#!)`

Causes the currently executing thread to sleep (temporarily cease execution) for the specified duration, subject to the precision and accuracy of system timers and schedulers. This method is a no-op if the duration is [negative](../java/time/Duration.md)).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#sleep(kotlin.Long)(millis: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`

Causes the currently executing thread to sleep (temporarily cease execution) for the specified number of milliseconds, subject to the precision and accuracy of system timers and schedulers. The thread does not lose ownership of any monitors.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#sleep(kotlin.Long,%20kotlin.Int)(millis: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, nanos: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Causes the currently executing thread to sleep (temporarily cease execution) for the specified number of milliseconds plus the specified number of nanoseconds, subject to the precision and accuracy of system timers and schedulers. The thread does not lose ownership of any monitors.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#start()()`

Causes this thread to begin execution; the Java Virtual Machine calls the `run` method of this thread.

The result is that two threads are running concurrently: the current thread (which returns from the call to the `start` method) and the other thread (which executes its `run` method).

It is never legal to start a thread more than once. In particular, a thread may not be restarted once it has completed execution.

**WARNING:** Do not override this method, because the runtime may treat this method `final` in the future, because it works closely with the runtime.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#stop()()`

Throws `UnsupportedOperationException`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#threadId()()`

Returns the identifier of this Thread. The thread ID is a positive `long` number generated when this thread was created. The thread ID is unique and remains unchanged during its lifetime.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#toString()()`

Returns a string representation of this thread, including the thread's name, priority, and thread group.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#yield()()`

A hint to the scheduler that the current thread is willing to yield its current use of a processor. The scheduler is free to ignore this hint.

Yield is a heuristic attempt to improve relative progression between threads that would otherwise over-utilise a CPU. Its use should be combined with detailed profiling and benchmarking to ensure that it actually has the desired effect.

It is rarely appropriate to use this method. It may be useful for debugging or testing purposes, where it may help to reproduce bugs due to race conditions. It may also be useful when designing concurrency control constructs such as the ones in the `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/package-summary.html` package.

<br />

## Public constructors

### HandlerThread

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
HandlerThread(name: String!)
```

### HandlerThread

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
HandlerThread(
    name: String!, 
    linuxPriority: Int)
```

Constructs a HandlerThread.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the thread. |
| `linuxPriority` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A Linux priority (niceness) value from -20 to 19, such as the `THREAD_PRIORITY_*` constants in `https://developer.android.com/reference/kotlin/android/os/Process`. Do not pass `https://developer.android.com/reference/kotlin/java/lang/Thread.html#` priorities (such as the inherited `https://developer.android.com/reference/kotlin/java/lang/Thread.html#MIN_PRIORITY:kotlin.Int`), which use an incompatible scale. |

## Public methods

### getLooper

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLooper(): Looper!
```

This method returns the Looper associated with this thread. If this thread not been started or for any reason isAlive() returns false, this method will return null. If this thread has been started, this method will block until the looper has been initialized.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Looper!` | The looper. |

### getThreadId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getThreadId(): Int
```

Returns the identifier of this thread. See Process.myTid().

### quit

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun quit(): Boolean
```

Quits the handler thread's looper.

Causes the handler thread's looper to terminate without processing any more messages in the message queue.

Any attempt to post messages to the queue after the looper is asked to quit will fail. For example, the `https://developer.android.com/reference/kotlin/android/os/Handler#sendMessage(android.os.Message)` method will return false.

If `https://developer.android.com/reference/kotlin/android/os/HandlerThread#quit()` or `https://developer.android.com/reference/kotlin/android/os/HandlerThread#quitSafely()` is called multiple times, the first call will have an effect and the subsequent calls will be no-ops.

Using this method may be unsafe because some messages may not be delivered before the looper terminates. Consider using `https://developer.android.com/reference/kotlin/android/os/HandlerThread#quitSafely()` instead to ensure that all pending work is completed in an orderly manner.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the looper looper has been asked to quit or false if the thread had not yet started running. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/HandlerThread#quitSafely()`

### quitSafely

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun quitSafely(): Boolean
```

Quits the handler thread's looper safely.

Causes the handler thread's looper to terminate as soon as all remaining messages in the message queue that are already due to be delivered have been handled. Pending delayed messages with due times in the future will not be delivered.

Any attempt to post messages to the queue after the looper is asked to quit will fail. For example, the `https://developer.android.com/reference/kotlin/android/os/Handler#sendMessage(android.os.Message)` method will return false.

If the thread has not been started or has finished (that is if `https://developer.android.com/reference/kotlin/android/os/HandlerThread#getLooper()` returns null), then false is returned. Otherwise the looper is asked to quit and true is returned.

If `https://developer.android.com/reference/kotlin/android/os/HandlerThread#quit()` or `https://developer.android.com/reference/kotlin/android/os/HandlerThread#quitSafely()` is called multiple times, the first call will have an effect and the subsequent calls will be no-ops.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the looper looper has been asked to quit or false if the thread had not yet started running. |

### run

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun run(): Unit
```

If this thread was constructed using a separate `Runnable` run object, then that `Runnable` object's `run` method is called; otherwise, this method does nothing and returns.

Subclasses of `Thread` should override this method.

## Protected methods

### onLooperPrepared

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onLooperPrepared(): Unit
```

Call back method that can be explicitly overridden if needed to execute some setup before Looper loops.
