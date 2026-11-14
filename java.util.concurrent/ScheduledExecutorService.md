# ScheduledExecutorService

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScheduledExecutorService

```
interface ScheduledExecutorService : ExecutorService
```

| [java.util.concurrent.ScheduledExecutorService](../java/util/concurrent/ScheduledExecutorService.md) |

| Known Direct Subclasses [ScheduledThreadPoolExecutor](../java/util/concurrent/ScheduledThreadPoolExecutor.md) |--------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ScheduledThreadPoolExecutor](../java/util/concurrent/ScheduledThreadPoolExecutor.md) | A [ThreadPoolExecutor](../java/util/concurrent/ThreadPoolExecutor.md) that can additionally schedule commands to run after a given delay, or to execute periodically. | |
| --- | --- | --- | --- | --- | --- | --- |

An [ExecutorService](../java/util/concurrent/ExecutorService.md) that can schedule commands to run after a given delay, or to execute periodically.

The`schedule`methods create tasks with various delays and return a task object that can be used to cancel or check execution. The`scheduleAtFixedRate`and`scheduleWithFixedDelay`methods create and execute tasks that run periodically until cancelled.

Commands submitted using the [Executor.execute(Runnable)](../java/util/concurrent/Executor.md))and [ExecutorService](../java/util/concurrent/ExecutorService.md)`submit`methods are scheduled with a requested delay of zero. Zero and negative delays (but not periods) are also allowed in`schedule`methods, and are treated as requests for immediate execution.

All`schedule`methods accept*relative* delays and periods as arguments, not absolute times or dates. It is a simple matter to transform an absolute time represented as a to the required form. For example, to schedule at a certain future`date`, you can use:`schedule(task, date.getTime() - System.currentTimeMillis(), TimeUnit.MILLISECONDS)`. Beware however that expiration of a relative delay need not coincide with the current`Date`at which the task is enabled due to network time synchronization protocols, clock drift, or other factors.

The [Executors](../java/util/concurrent/Executors.md) class provides convenient factory methods for the ScheduledExecutorService implementations provided in this package.

## Usage Example

Here is a class with a method that sets up a ScheduledExecutorService to beep every ten seconds for an hour: 

```kotlin
<code>import static java.util.concurrent.TimeUnit.*;
  class BeeperControl {
    private final ScheduledExecutorService scheduler =
      Executors.newScheduledThreadPool(1);
 
    public void beepForAnHour() {
      Runnable beeper = () -&gt; System.out.println("beep");
      ScheduledFuture&lt;?&gt; beeperHandle =
        scheduler.scheduleAtFixedRate(beeper, 10, 10, SECONDS);
      Runnable canceller = () -&gt; beeperHandle.cancel(false);
      scheduler.schedule(canceller, 1, HOURS);
    }
  }</code>
```

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [ScheduledFuture](../java/util/concurrent/ScheduledFuture.md)\<\*\>! | [schedule](../java/util/concurrent/ScheduledExecutorService.md))`(`command:` ` [Runnable](../java/lang/Runnable.md)!`, `delay:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](../java/util/concurrent/TimeUnit.md)!`)` Submits a one-shot task that becomes enabled after the given delay. |
| abstract [ScheduledFuture](../java/util/concurrent/ScheduledFuture.md)\<V\>! | [schedule](../java/util/concurrent/ScheduledExecutorService.md))`(`callable:` ` [Callable](../java/util/concurrent/Callable.md)<V>!`, `delay:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](../java/util/concurrent/TimeUnit.md)!`)` Submits a value-returning one-shot task that becomes enabled after the given delay. |
| abstract [ScheduledFuture](../java/util/concurrent/ScheduledFuture.md)\<\*\>! | [scheduleAtFixedRate](../java/util/concurrent/ScheduledExecutorService.md))`(`command:` ` [Runnable](../java/lang/Runnable.md)!`, `initialDelay:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `period:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](../java/util/concurrent/TimeUnit.md)!`)` Submits a periodic action that becomes enabled first after the given initial delay, and subsequently with the given period; that is, executions will commence after`initialDelay`, then`initialDelay + period`, then`initialDelay + 2 * period`, and so on. |
| --- | --- |
| abstract [ScheduledFuture](../java/util/concurrent/ScheduledFuture.md)\<\*\>! | [scheduleWithFixedDelay](../java/util/concurrent/ScheduledExecutorService.md))`(`command:` ` [Runnable](../java/lang/Runnable.md)!`, `initialDelay:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `delay:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](../java/util/concurrent/TimeUnit.md)!`)` Submits a periodic action that becomes enabled first after the given initial delay, and subsequently with the given delay between the termination of one execution and the commencement of the next. |

| Inherited functions ||
|---|---|
| From class [ExecutorService](../java/util/concurrent/ExecutorService.md) |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [awaitTermination](../java/util/concurrent/ExecutorService.md))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](../java/util/concurrent/TimeUnit.md)!`)` <br /> Blocks until all tasks have completed execution after a shutdown request, or the timeout occurs, or the current thread is interrupted, whichever happens first. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../java/util/concurrent/ExecutorService.md))`()` <br /> Initiates an orderly shutdown in which previously submitted tasks are executed, but no new tasks will be accepted. This method waits until all tasks have completed execution and the executor has terminated. If interrupted while waiting, this method stops all executing tasks as if by invoking [shutdownNow()](../java/util/concurrent/ExecutorService.md)). It then continues to wait until all actively executing tasks have completed. Tasks that were awaiting execution are not executed. The interrupt status will be re-asserted before this method returns. If already terminated, invoking this method has no effect. <br /> | | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Future](../java/util/concurrent/Future.md)<T>!>! | [invokeAll](../java/util/concurrent/ExecutorService.md))`(`tasks:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` ` [Callable](../java/util/concurrent/Callable.md)<T>!>!`)` <br /> Executes the given tasks, returning a list of Futures holding their status and results when all complete. [Future.isDone](../java/util/concurrent/Future.md))is`true`for each element of the returned list. Note that a*completed*task could have terminated either normally or by throwing an exception. The results of this method are undefined if the given collection is modified while this operation is in progress. <br /> | | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Future](../java/util/concurrent/Future.md)<T>!>! | [invokeAll](../java/util/concurrent/ExecutorService.md))`(`tasks:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` ` [Callable](../java/util/concurrent/Callable.md)<T>!>!`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](../java/util/concurrent/TimeUnit.md)!`)` <br /> Executes the given tasks, returning a list of Futures holding their status and results when all complete or the timeout expires, whichever happens first. [Future.isDone](../java/util/concurrent/Future.md))is`true`for each element of the returned list. Upon return, tasks that have not completed are cancelled. Note that a*completed*task could have terminated either normally or by throwing an exception. The results of this method are undefined if the given collection is modified while this operation is in progress. <br /> | | T | [invokeAny](../java/util/concurrent/ExecutorService.md))`(`tasks:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` ` [Callable](../java/util/concurrent/Callable.md)<T>!>!`)` <br /> Executes the given tasks, returning the result of one that has completed successfully (i.e., without throwing an exception), if any do. Upon normal or exceptional return, tasks that have not completed are cancelled. The results of this method are undefined if the given collection is modified while this operation is in progress. <br /> | | T | [invokeAny](../java/util/concurrent/ExecutorService.md))`(`tasks:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` ` [Callable](../java/util/concurrent/Callable.md)<T>!>!`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](../java/util/concurrent/TimeUnit.md)!`)` <br /> Executes the given tasks, returning the result of one that has completed successfully (i.e., without throwing an exception), if any do before the given timeout elapses. Upon normal or exceptional return, tasks that have not completed are cancelled. The results of this method are undefined if the given collection is modified while this operation is in progress. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isShutdown](../java/util/concurrent/ExecutorService.md))`()` <br /> Returns`true`if this executor has been shut down. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTerminated](../java/util/concurrent/ExecutorService.md))`()` <br /> Returns`true`if all tasks have completed following shut down. Note that`isTerminated`is never`true`unless either`shutdown`or`shutdownNow`was called first. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [shutdown](../java/util/concurrent/ExecutorService.md))`()` <br /> Initiates an orderly shutdown in which previously submitted tasks are executed, but no new tasks will be accepted. Invocation has no additional effect if already shut down. This method does not wait for previously submitted tasks to complete execution. Use [awaitTermination](../java/util/concurrent/ExecutorService.md))to do that. <br /> | | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Runnable](../java/lang/Runnable.md)!>! | [shutdownNow](../java/util/concurrent/ExecutorService.md))`()` <br /> Attempts to stop all actively executing tasks, halts the processing of waiting tasks, and returns a list of the tasks that were awaiting execution. This method does not wait for actively executing tasks to terminate. Use [awaitTermination](../java/util/concurrent/ExecutorService.md))to do that. There are no guarantees beyond best-effort attempts to stop processing actively executing tasks. For example, typical implementations will cancel via [Thread.interrupt](../java/lang/Thread.md)), so any task that fails to respond to interrupts may never terminate. <br /> | | [Future](../java/util/concurrent/Future.md)<*>! | [submit](../java/util/concurrent/ExecutorService.md))`(`task:` ` [Runnable](../java/lang/Runnable.md)!`)` <br /> Submits a Runnable task for execution and returns a Future representing that task. The Future's`get`method will return`null`upon*successful*completion. <br /> | | [Future](../java/util/concurrent/Future.md)<T>! | [submit](../java/util/concurrent/ExecutorService.md))`(`task:` ` [Runnable](../java/lang/Runnable.md)!`, `result:` `T`)` <br /> Submits a Runnable task for execution and returns a Future representing that task. The Future's`get`method will return the given result upon successful completion. <br /> | | [Future](../java/util/concurrent/Future.md)<T>! | [submit](../java/util/concurrent/ExecutorService.md))`(`task:` ` [Callable](../java/util/concurrent/Callable.md)<T>!`)` <br /> Submits a value-returning task for execution and returns a Future representing the pending results of the task. The Future's`get`method will return the task's result upon successful completion. If you would like to immediately block waiting for a task, you can use constructions of the form`result = exec.submit(aCallable).get();` Note: The [Executors](../java/util/concurrent/Executors.md) class includes a set of methods that can convert some other common closure-like objects, for example, [java.security.PrivilegedAction](../java/security/PrivilegedAction.md) to [Callable](../java/util/concurrent/Callable.md) form so they can be submitted. <br /> | ||
| From class [Executor](../java/util/concurrent/Executor.md) |------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [execute](../java/util/concurrent/Executor.md))`(`command:` ` [Runnable](../java/lang/Runnable.md)!`)` <br /> Executes the given command at some time in the future. The command may execute in a new thread, in a pooled thread, or in the calling thread, at the discretion of the`Executor`implementation. <br /> | ||

## Public methods

### schedule

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun schedule(
    command: Runnable!, 
    delay: Long, 
    unit: TimeUnit!
): ScheduledFuture<*>!
```

Submits a one-shot task that becomes enabled after the given delay.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------|
| `command` | [Runnable](../java/lang/Runnable.md)!:the task to execute |
| `delay` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the time from now to delay execution |
| `unit` | [TimeUnit](../java/util/concurrent/TimeUnit.md)!:the time unit of the delay parameter |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [ScheduledFuture](../java/util/concurrent/ScheduledFuture.md)<*>! | a ScheduledFuture representing pending completion of the task and whose`get()`method will return`null`upon completion |

| Exceptions ||
|---------------------------------------------------|-----------------------------------------------|
| `java.util.concurrent.RejectedExecutionException` | if the task cannot be scheduled for execution |
| `java.lang.NullPointerException` | if command or unit is null |

### schedule

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <V : Any!> schedule(
    callable: Callable<V>!, 
    delay: Long, 
    unit: TimeUnit!
): ScheduledFuture<V>!
```

Submits a value-returning one-shot task that becomes enabled after the given delay.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------|
| `callable` | [Callable](../java/util/concurrent/Callable.md)\<V\>!:the function to execute |
| `delay` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the time from now to delay execution |
| `unit` | [TimeUnit](../java/util/concurrent/TimeUnit.md)!:the time unit of the delay parameter |
| --- | --- |
| `<V>` | the type of the callable's result |

| Return ||
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [ScheduledFuture](../java/util/concurrent/ScheduledFuture.md)<V>! | a ScheduledFuture that can be used to extract result or cancel |

| Exceptions ||
|---------------------------------------------------|-----------------------------------------------|
| `java.util.concurrent.RejectedExecutionException` | if the task cannot be scheduled for execution |
| `java.lang.NullPointerException` | if callable or unit is null |

### scheduleAtFixedRate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun scheduleAtFixedRate(
    command: Runnable!, 
    initialDelay: Long, 
    period: Long, 
    unit: TimeUnit!
): ScheduledFuture<*>!
```

Submits a periodic action that becomes enabled first after the given initial delay, and subsequently with the given period; that is, executions will commence after`initialDelay`, then`initialDelay + period`, then`initialDelay + 2 * period`, and so on.

The sequence of task executions continues indefinitely until one of the following exceptional completions occur:

- The task is [explicitly cancelled](../java/util/concurrent/Future.md))via the returned future.
- The executor terminates, also resulting in task cancellation.
- An execution of the task throws an exception. In this case calling [get](../java/util/concurrent/Future.md))on the returned future will throw [ExecutionException](../java/util/concurrent/ExecutionException.md), holding the exception as its cause.

Subsequent executions are suppressed. Subsequent calls to [isDone()](../java/util/concurrent/Future.md))on the returned future will return`true`.

If any execution of this task takes longer than its period, then subsequent executions may start late, but will not concurrently execute.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `command` | [Runnable](../java/lang/Runnable.md)!:the task to execute |
| `initialDelay` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the time to delay first execution |
| `period` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the period between successive executions |
| --- | --- |
| `unit` | [TimeUnit](../java/util/concurrent/TimeUnit.md)!:the time unit of the initialDelay and period parameters |

| Return ||
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ScheduledFuture](../java/util/concurrent/ScheduledFuture.md)<*>! | a ScheduledFuture representing pending completion of the series of repeated tasks. The future's [get()](../java/util/concurrent/Future.md))method will never return normally, and will throw an exception upon task cancellation or abnormal termination of a task execution. |

| Exceptions ||
|---------------------------------------------------|-----------------------------------------------|
| `java.util.concurrent.RejectedExecutionException` | if the task cannot be scheduled for execution |
| `java.lang.NullPointerException` | if command or unit is null |
| `java.lang.IllegalArgumentException` | if period less than or equal to zero |
| --- | --- |

### scheduleWithFixedDelay

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun scheduleWithFixedDelay(
    command: Runnable!, 
    initialDelay: Long, 
    delay: Long, 
    unit: TimeUnit!
): ScheduledFuture<*>!
```

Submits a periodic action that becomes enabled first after the given initial delay, and subsequently with the given delay between the termination of one execution and the commencement of the next.

The sequence of task executions continues indefinitely until one of the following exceptional completions occur:

- The task is [explicitly cancelled](../java/util/concurrent/Future.md))via the returned future.
- The executor terminates, also resulting in task cancellation.
- An execution of the task throws an exception. In this case calling [get](../java/util/concurrent/Future.md))on the returned future will throw [ExecutionException](../java/util/concurrent/ExecutionException.md), holding the exception as its cause.

Subsequent executions are suppressed. Subsequent calls to [isDone()](../java/util/concurrent/Future.md))on the returned future will return`true`.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `command` | [Runnable](../java/lang/Runnable.md)!:the task to execute |
| `initialDelay` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the time to delay first execution |
| `delay` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the delay between the termination of one execution and the commencement of the next |
| --- | --- |
| `unit` | [TimeUnit](../java/util/concurrent/TimeUnit.md)!:the time unit of the initialDelay and delay parameters |

| Return ||
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ScheduledFuture](../java/util/concurrent/ScheduledFuture.md)<*>! | a ScheduledFuture representing pending completion of the series of repeated tasks. The future's [get()](../java/util/concurrent/Future.md))method will never return normally, and will throw an exception upon task cancellation or abnormal termination of a task execution. |

| Exceptions ||
|---------------------------------------------------|-----------------------------------------------|
| `java.util.concurrent.RejectedExecutionException` | if the task cannot be scheduled for execution |
| `java.lang.NullPointerException` | if command or unit is null |
| `java.lang.IllegalArgumentException` | if delay less than or equal to zero |
| --- | --- |
