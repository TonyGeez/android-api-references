# ScheduledExecutorService

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScheduledExecutorService

```
interface ScheduledExecutorService : ExecutorService
```

| [java.util.concurrent.ScheduledExecutorService](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledExecutorService#) |

| Known Direct Subclasses [ScheduledThreadPoolExecutor](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor) |--------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ScheduledThreadPoolExecutor](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor) | A [ThreadPoolExecutor](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor) that can additionally schedule commands to run after a given delay, or to execute periodically. | |

An [ExecutorService](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService) that can schedule commands to run after a given delay, or to execute periodically.

The`schedule`methods create tasks with various delays and return a task object that can be used to cancel or check execution. The`scheduleAtFixedRate`and`scheduleWithFixedDelay`methods create and execute tasks that run periodically until cancelled.

Commands submitted using the [Executor.execute(Runnable)](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor#execute(java.lang.Runnable))and [ExecutorService](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService)`submit`methods are scheduled with a requested delay of zero. Zero and negative delays (but not periods) are also allowed in`schedule`methods, and are treated as requests for immediate execution.

All`schedule`methods accept*relative* delays and periods as arguments, not absolute times or dates. It is a simple matter to transform an absolute time represented as a to the required form. For example, to schedule at a certain future`date`, you can use:`schedule(task, date.getTime() - System.currentTimeMillis(), TimeUnit.MILLISECONDS)`. Beware however that expiration of a relative delay need not coincide with the current`Date`at which the task is enabled due to network time synchronization protocols, clock drift, or other factors.

The [Executors](https://developer.android.com/reference/kotlin/java/util/concurrent/Executors) class provides convenient factory methods for the ScheduledExecutorService implementations provided in this package.

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
| abstract [ScheduledFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledFuture)\<\*\>! | [schedule](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledExecutorService#schedule(java.lang.Runnable,%20kotlin.Long,%20java.util.concurrent.TimeUnit))`(`command:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`, `delay:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` Submits a one-shot task that becomes enabled after the given delay. |
| abstract [ScheduledFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledFuture)\<V\>! | [schedule](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledExecutorService#schedule(java.util.concurrent.Callable,%20kotlin.Long,%20java.util.concurrent.TimeUnit))`(`callable:` ` [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable)<V>!`, `delay:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` Submits a value-returning one-shot task that becomes enabled after the given delay. |
| abstract [ScheduledFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledFuture)\<\*\>! | [scheduleAtFixedRate](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledExecutorService#scheduleAtFixedRate(java.lang.Runnable,%20kotlin.Long,%20kotlin.Long,%20java.util.concurrent.TimeUnit))`(`command:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`, `initialDelay:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `period:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` Submits a periodic action that becomes enabled first after the given initial delay, and subsequently with the given period; that is, executions will commence after`initialDelay`, then`initialDelay + period`, then`initialDelay + 2 * period`, and so on. |
| abstract [ScheduledFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledFuture)\<\*\>! | [scheduleWithFixedDelay](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledExecutorService#scheduleWithFixedDelay(java.lang.Runnable,%20kotlin.Long,%20kotlin.Long,%20java.util.concurrent.TimeUnit))`(`command:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`, `initialDelay:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `delay:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` Submits a periodic action that becomes enabled first after the given initial delay, and subsequently with the given delay between the termination of one execution and the commencement of the next. |

| Inherited functions ||
|---|---|
| From class [ExecutorService](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService) |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [awaitTermination](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService#awaitTermination(kotlin.Long,%20java.util.concurrent.TimeUnit))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` <br /> Blocks until all tasks have completed execution after a shutdown request, or the timeout occurs, or the current thread is interrupted, whichever happens first. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService#close())`()` <br /> Initiates an orderly shutdown in which previously submitted tasks are executed, but no new tasks will be accepted. This method waits until all tasks have completed execution and the executor has terminated. If interrupted while waiting, this method stops all executing tasks as if by invoking [shutdownNow()](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService#shutdownNow()). It then continues to wait until all actively executing tasks have completed. Tasks that were awaiting execution are not executed. The interrupt status will be re-asserted before this method returns. If already terminated, invoking this method has no effect. <br /> | | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)<T>!>! | [invokeAll](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService#invokeAll(kotlin.collections.MutableCollection))`(`tasks:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` ` [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable)<T>!>!`)` <br /> Executes the given tasks, returning a list of Futures holding their status and results when all complete. [Future.isDone](https://developer.android.com/reference/kotlin/java/util/concurrent/Future#isDone())is`true`for each element of the returned list. Note that a*completed*task could have terminated either normally or by throwing an exception. The results of this method are undefined if the given collection is modified while this operation is in progress. <br /> | | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)<T>!>! | [invokeAll](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService#invokeAll(kotlin.collections.MutableCollection,%20kotlin.Long,%20java.util.concurrent.TimeUnit))`(`tasks:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` ` [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable)<T>!>!`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` <br /> Executes the given tasks, returning a list of Futures holding their status and results when all complete or the timeout expires, whichever happens first. [Future.isDone](https://developer.android.com/reference/kotlin/java/util/concurrent/Future#isDone())is`true`for each element of the returned list. Upon return, tasks that have not completed are cancelled. Note that a*completed*task could have terminated either normally or by throwing an exception. The results of this method are undefined if the given collection is modified while this operation is in progress. <br /> | | T | [invokeAny](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService#invokeAny(kotlin.collections.MutableCollection))`(`tasks:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` ` [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable)<T>!>!`)` <br /> Executes the given tasks, returning the result of one that has completed successfully (i.e., without throwing an exception), if any do. Upon normal or exceptional return, tasks that have not completed are cancelled. The results of this method are undefined if the given collection is modified while this operation is in progress. <br /> | | T | [invokeAny](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService#invokeAny(kotlin.collections.MutableCollection,%20kotlin.Long,%20java.util.concurrent.TimeUnit))`(`tasks:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` ` [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable)<T>!>!`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` <br /> Executes the given tasks, returning the result of one that has completed successfully (i.e., without throwing an exception), if any do before the given timeout elapses. Upon normal or exceptional return, tasks that have not completed are cancelled. The results of this method are undefined if the given collection is modified while this operation is in progress. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isShutdown](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService#isShutdown())`()` <br /> Returns`true`if this executor has been shut down. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTerminated](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService#isTerminated())`()` <br /> Returns`true`if all tasks have completed following shut down. Note that`isTerminated`is never`true`unless either`shutdown`or`shutdownNow`was called first. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [shutdown](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService#shutdown())`()` <br /> Initiates an orderly shutdown in which previously submitted tasks are executed, but no new tasks will be accepted. Invocation has no additional effect if already shut down. This method does not wait for previously submitted tasks to complete execution. Use [awaitTermination](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService#awaitTermination(kotlin.Long,%20java.util.concurrent.TimeUnit))to do that. <br /> | | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!>! | [shutdownNow](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService#shutdownNow())`()` <br /> Attempts to stop all actively executing tasks, halts the processing of waiting tasks, and returns a list of the tasks that were awaiting execution. This method does not wait for actively executing tasks to terminate. Use [awaitTermination](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService#awaitTermination(kotlin.Long,%20java.util.concurrent.TimeUnit))to do that. There are no guarantees beyond best-effort attempts to stop processing actively executing tasks. For example, typical implementations will cancel via [Thread.interrupt](https://developer.android.com/reference/kotlin/java/lang/Thread.html#interrupt()), so any task that fails to respond to interrupts may never terminate. <br /> | | [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)<*>! | [submit](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService#submit(java.lang.Runnable))`(`task:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`)` <br /> Submits a Runnable task for execution and returns a Future representing that task. The Future's`get`method will return`null`upon*successful*completion. <br /> | | [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)<T>! | [submit](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService#submit(java.lang.Runnable,%20java.util.concurrent.ExecutorService.submit.T))`(`task:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`, `result:` `T`)` <br /> Submits a Runnable task for execution and returns a Future representing that task. The Future's`get`method will return the given result upon successful completion. <br /> | | [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)<T>! | [submit](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService#submit(java.util.concurrent.Callable))`(`task:` ` [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable)<T>!`)` <br /> Submits a value-returning task for execution and returns a Future representing the pending results of the task. The Future's`get`method will return the task's result upon successful completion. If you would like to immediately block waiting for a task, you can use constructions of the form`result = exec.submit(aCallable).get();` Note: The [Executors](https://developer.android.com/reference/kotlin/java/util/concurrent/Executors) class includes a set of methods that can convert some other common closure-like objects, for example, [java.security.PrivilegedAction](https://developer.android.com/reference/kotlin/java/security/PrivilegedAction.html#) to [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable) form so they can be submitted. <br /> | ||
| From class [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor) |------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [execute](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor#execute(java.lang.Runnable))`(`command:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`)` <br /> Executes the given command at some time in the future. The command may execute in a new thread, in a pooled thread, or in the calling thread, at the discretion of the`Executor`implementation. <br /> | ||

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
| `command` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!:the task to execute |
| `delay` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the time from now to delay execution |
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!:the time unit of the delay parameter |

| Return ||
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [ScheduledFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledFuture)<*>! | a ScheduledFuture representing pending completion of the task and whose`get()`method will return`null`upon completion |

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
| `callable` | [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable)\<V\>!:the function to execute |
| `delay` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the time from now to delay execution |
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!:the time unit of the delay parameter |
| `<V>` | the type of the callable's result |

| Return ||
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [ScheduledFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledFuture)<V>! | a ScheduledFuture that can be used to extract result or cancel |

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

- The task is [explicitly cancelled](https://developer.android.com/reference/kotlin/java/util/concurrent/Future#cancel(kotlin.Boolean))via the returned future.
- The executor terminates, also resulting in task cancellation.
- An execution of the task throws an exception. In this case calling [get](https://developer.android.com/reference/kotlin/java/util/concurrent/Future#get())on the returned future will throw [ExecutionException](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutionException), holding the exception as its cause.

Subsequent executions are suppressed. Subsequent calls to [isDone()](https://developer.android.com/reference/kotlin/java/util/concurrent/Future#isDone())on the returned future will return`true`.

If any execution of this task takes longer than its period, then subsequent executions may start late, but will not concurrently execute.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `command` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!:the task to execute |
| `initialDelay` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the time to delay first execution |
| `period` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the period between successive executions |
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!:the time unit of the initialDelay and period parameters |

| Return ||
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ScheduledFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledFuture)<*>! | a ScheduledFuture representing pending completion of the series of repeated tasks. The future's [get()](https://developer.android.com/reference/kotlin/java/util/concurrent/Future#get())method will never return normally, and will throw an exception upon task cancellation or abnormal termination of a task execution. |

| Exceptions ||
|---------------------------------------------------|-----------------------------------------------|
| `java.util.concurrent.RejectedExecutionException` | if the task cannot be scheduled for execution |
| `java.lang.NullPointerException` | if command or unit is null |
| `java.lang.IllegalArgumentException` | if period less than or equal to zero |

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

- The task is [explicitly cancelled](https://developer.android.com/reference/kotlin/java/util/concurrent/Future#cancel(kotlin.Boolean))via the returned future.
- The executor terminates, also resulting in task cancellation.
- An execution of the task throws an exception. In this case calling [get](https://developer.android.com/reference/kotlin/java/util/concurrent/Future#get())on the returned future will throw [ExecutionException](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutionException), holding the exception as its cause.

Subsequent executions are suppressed. Subsequent calls to [isDone()](https://developer.android.com/reference/kotlin/java/util/concurrent/Future#isDone())on the returned future will return`true`.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `command` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!:the task to execute |
| `initialDelay` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the time to delay first execution |
| `delay` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the delay between the termination of one execution and the commencement of the next |
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!:the time unit of the initialDelay and delay parameters |

| Return ||
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ScheduledFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledFuture)<*>! | a ScheduledFuture representing pending completion of the series of repeated tasks. The future's [get()](https://developer.android.com/reference/kotlin/java/util/concurrent/Future#get())method will never return normally, and will throw an exception upon task cancellation or abnormal termination of a task execution. |

| Exceptions ||
|---------------------------------------------------|-----------------------------------------------|
| `java.util.concurrent.RejectedExecutionException` | if the task cannot be scheduled for execution |
| `java.lang.NullPointerException` | if command or unit is null |
| `java.lang.IllegalArgumentException` | if delay less than or equal to zero |
