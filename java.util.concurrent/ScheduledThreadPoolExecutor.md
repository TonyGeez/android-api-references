# ScheduledThreadPoolExecutor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScheduledThreadPoolExecutor

```
open class ScheduledThreadPoolExecutor : ThreadPoolExecutor, ScheduledExecutorService
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.util.concurrent.AbstractExecutorService](AbstractExecutorService.md) |||
| | ↳ | [java.util.concurrent.ThreadPoolExecutor](ThreadPoolExecutor.md) ||
| | | ↳ | [java.util.concurrent.ScheduledThreadPoolExecutor](ScheduledThreadPoolExecutor.md) |
| --- | --- | --- | --- |

A [ThreadPoolExecutor](ThreadPoolExecutor.md) that can additionally schedule commands to run after a given delay, or to execute periodically. This class is preferable to [java.util.Timer](../java.util/Timer.md) when multiple worker threads are needed, or when the additional flexibility or capabilities of [ThreadPoolExecutor](ThreadPoolExecutor.md)(which this class extends) are required.

Delayed tasks execute no sooner than they are enabled, but without any real-time guarantees about when, after they are enabled, they will commence. Tasks scheduled for exactly the same execution time are enabled in first-in-first-out (FIFO) order of submission.

When a submitted task is cancelled before it is run, execution is suppressed. By default, such a cancelled task is not automatically removed from the work queue until its delay elapses. While this enables further inspection and monitoring, it may also cause unbounded retention of cancelled tasks.

Successive executions of a periodic task scheduled via [scheduleAtFixedRate](ScheduledThreadPoolExecutor.md))or [scheduleWithFixedDelay](ScheduledThreadPoolExecutor.md))do not overlap. While different executions may be performed by different threads, the effects of prior executions [*happen-before*](_package.md) those of subsequent ones.

While this class inherits from [ThreadPoolExecutor](ThreadPoolExecutor.md), a few of the inherited tuning methods are not useful for it. In particular, because it acts as a fixed-sized pool using`corePoolSize`threads and an unbounded queue, adjustments to`maximumPoolSize`have no useful effect. Additionally, it is almost never a good idea to set`corePoolSize`to zero or use`allowCoreThreadTimeOut`because this may leave the pool without threads to handle tasks once they become eligible to run.

As with`ThreadPoolExecutor`, if not otherwise specified, this class uses [Executors.defaultThreadFactory](Executors.md))as the default thread factory, and [ThreadPoolExecutor.AbortPolicy](../java/util/concurrent/ThreadPoolExecutor.AbortPolicy.md) as the default rejected execution handler.

**Extension notes:** This class overrides the [execute](ThreadPoolExecutor.md))and [submit](AbstractExecutorService.md))methods to generate internal [ScheduledFuture](ScheduledFuture.md) objects to control per-task delays and scheduling. To preserve functionality, any further overrides of these methods in subclasses must invoke superclass versions, which effectively disables additional task customization. However, this class provides alternative protected extension method`decorateTask`(one version each for`Runnable`and`Callable`) that can be used to customize the concrete task types used to execute commands entered via`execute`,`submit`,`schedule`,`scheduleAtFixedRate`, and`scheduleWithFixedDelay`. By default, a`ScheduledThreadPoolExecutor`uses a task type extending [FutureTask](FutureTask.md). However, this may be modified or replaced using subclasses of the form: 

```kotlin
<code>public class CustomScheduledExecutor extends ScheduledThreadPoolExecutor {
 
    static class CustomTask&lt;V&gt; implements RunnableScheduledFuture&lt;V&gt; { ... }
 
    protected &lt;V&gt; RunnableScheduledFuture&lt;V&gt; decorateTask(
                 Runnable r, RunnableScheduledFuture&lt;V&gt; task) {
        return new CustomTask&lt;V&gt;(r, task);
    }
 
    protected &lt;V&gt; RunnableScheduledFuture&lt;V&gt; decorateTask(
                 Callable&lt;V&gt; c, RunnableScheduledFuture&lt;V&gt; task) {
        return new CustomTask&lt;V&gt;(c, task);
    }
    // ... add constructors, etc.
  }</code>
```

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ScheduledThreadPoolExecutor](ScheduledThreadPoolExecutor.md))`(`corePoolSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new`ScheduledThreadPoolExecutor`with the given core pool size. |
| [ScheduledThreadPoolExecutor](ScheduledThreadPoolExecutor.md))`(`corePoolSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `handler:` ` [RejectedExecutionHandler](RejectedExecutionHandler.md)!`)` Creates a new`ScheduledThreadPoolExecutor`with the given initial parameters. |
| [ScheduledThreadPoolExecutor](ScheduledThreadPoolExecutor.md))`(`corePoolSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `threadFactory:` ` [ThreadFactory](ThreadFactory.md)!`)` Creates a new`ScheduledThreadPoolExecutor`with the given initial parameters. |
| [ScheduledThreadPoolExecutor](ScheduledThreadPoolExecutor.md))`(`corePoolSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `threadFactory:` ` [ThreadFactory](ThreadFactory.md)!`, `handler:` ` [RejectedExecutionHandler](RejectedExecutionHandler.md)!`)` Creates a new`ScheduledThreadPoolExecutor`with the given initial parameters. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [execute](ScheduledThreadPoolExecutor.md))`(`command:` ` [Runnable](../java.lang/Runnable.md)!`)` Executes`command`with zero required delay. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getContinueExistingPeriodicTasksAfterShutdownPolicy](ScheduledThreadPoolExecutor.md))`()` Gets the policy on whether to continue executing existing periodic tasks even when this executor has been`shutdown`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getExecuteExistingDelayedTasksAfterShutdownPolicy](ScheduledThreadPoolExecutor.md))`()` Gets the policy on whether to execute existing delayed tasks even when this executor has been`shutdown`. |
| --- | --- |
| open [BlockingQueue](BlockingQueue.md)\< [Runnable](../java.lang/Runnable.md)!\>! | [getQueue](ScheduledThreadPoolExecutor.md))`()` Returns the task queue used by this executor. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getRemoveOnCancelPolicy](ScheduledThreadPoolExecutor.md))`()` Gets the policy on whether cancelled tasks should be immediately removed from the work queue at time of cancellation. |
| open [ScheduledFuture](ScheduledFuture.md)\<\*\>! | [schedule](ScheduledThreadPoolExecutor.md))`(`command:` ` [Runnable](../java.lang/Runnable.md)!`, `delay:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` <br /> |
| --- | --- |
| open [ScheduledFuture](ScheduledFuture.md)\<V\>! | [schedule](ScheduledThreadPoolExecutor.md))`(`callable:` ` [Callable](Callable.md)<V>!`, `delay:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` <br /> |
| open [ScheduledFuture](ScheduledFuture.md)\<\*\>! | [scheduleAtFixedRate](ScheduledThreadPoolExecutor.md))`(`command:` ` [Runnable](../java.lang/Runnable.md)!`, `initialDelay:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `period:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` Submits a periodic action that becomes enabled first after the given initial delay, and subsequently with the given period; that is, executions will commence after`initialDelay`, then`initialDelay + period`, then`initialDelay + 2 * period`, and so on. |
| open [ScheduledFuture](ScheduledFuture.md)\<\*\>! | [scheduleWithFixedDelay](ScheduledThreadPoolExecutor.md))`(`command:` ` [Runnable](../java.lang/Runnable.md)!`, `initialDelay:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `delay:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` Submits a periodic action that becomes enabled first after the given initial delay, and subsequently with the given delay between the termination of one execution and the commencement of the next. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContinueExistingPeriodicTasksAfterShutdownPolicy](ScheduledThreadPoolExecutor.md))`(`value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the policy on whether to continue executing existing periodic tasks even when this executor has been`shutdown`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setExecuteExistingDelayedTasksAfterShutdownPolicy](ScheduledThreadPoolExecutor.md))`(`value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the policy on whether to execute existing delayed tasks even when this executor has been`shutdown`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRemoveOnCancelPolicy](ScheduledThreadPoolExecutor.md))`(`value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the policy on whether cancelled tasks should be immediately removed from the work queue at time of cancellation. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [shutdown](ScheduledThreadPoolExecutor.md))`()` Initiates an orderly shutdown in which previously submitted tasks are executed, but no new tasks will be accepted. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Runnable](../java.lang/Runnable.md)!\>! | [shutdownNow](ScheduledThreadPoolExecutor.md))`()` Attempts to stop all actively executing tasks, halts the processing of waiting tasks, and returns a list of the tasks that were awaiting execution. |
| open [Future](Future.md)\<\*\>! | [submit](ScheduledThreadPoolExecutor.md))`(`task:` ` [Runnable](../java.lang/Runnable.md)!`)` <br /> |
| --- | --- |
| open [Future](Future.md)\<T\>! | [submit](ScheduledThreadPoolExecutor.md))`(`task:` ` [Runnable](../java.lang/Runnable.md)!`, `result:` `T`)` <br /> |
| open [Future](Future.md)\<T\>! | [submit](ScheduledThreadPoolExecutor.md))`(`task:` ` [Callable](Callable.md)<T>!`)` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [RunnableScheduledFuture](RunnableScheduledFuture.md)\<V\>! | [decorateTask](ScheduledThreadPoolExecutor.md))`(`runnable:` ` [Runnable](../java.lang/Runnable.md)!`, `task:` ` [RunnableScheduledFuture](RunnableScheduledFuture.md)<V>!`)` Modifies or replaces the task used to execute a runnable. |
| open [RunnableScheduledFuture](RunnableScheduledFuture.md)\<V\>! | [decorateTask](ScheduledThreadPoolExecutor.md))`(`callable:` ` [Callable](Callable.md)<V>!`, `task:` ` [RunnableScheduledFuture](RunnableScheduledFuture.md)<V>!`)` Modifies or replaces the task used to execute a callable. |

| Inherited functions ||
|---|---|
| From class [ThreadPoolExecutor](ThreadPoolExecutor.md) |---------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [afterExecute](ThreadPoolExecutor.md))`(`r:` ` [Runnable](../java.lang/Runnable.md)!`, `t:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> Method invoked upon completion of execution of the given Runnable. This method is invoked by the thread that executed the task. If non-null, the Throwable is the uncaught`RuntimeException`or`Error`that caused execution to terminate abruptly. This implementation does nothing, but may be customized in subclasses. Note: To properly nest multiple overridings, subclasses should generally invoke`super.afterExecute`at the beginning of this method. **Note:** When actions are enclosed in tasks (such as [FutureTask](FutureTask.md)) either explicitly or via methods such as`submit`, these task objects catch and maintain computational exceptions, and so they do not cause abrupt termination, and the internal exceptions are*not*passed to this method. If you would like to trap both kinds of failures in this method, you can further probe for such cases, as in this sample subclass that prints either the direct cause or the underlying exception if a task has been aborted: ```kotlin <code>class ExtendedExecutor extends ThreadPoolExecutor { // ... protected void afterExecute(Runnable r, Throwable t) { super.afterExecute(r, t); if (t == null &amp;&amp; r instanceof Future&lt;?&gt; &amp;&amp; ((Future&lt;?&gt;)r).isDone()) { try { Object result = ((Future&lt;?&gt;) r).get(); } catch (CancellationException ce) { t = ce; } catch (ExecutionException ee) { t = ee.getCause(); } catch (InterruptedException ie) { // ignore/reset Thread.currentThread().interrupt(); } } if (t != null) System.out.println(t); } }</code> ``` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [allowCoreThreadTimeOut](ThreadPoolExecutor.md))`(`value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets the policy governing whether core threads may time out and terminate if no tasks arrive within the keep-alive time, being replaced if needed when new tasks arrive. When false, core threads are never terminated due to lack of incoming tasks. When true, the same keep-alive policy applying to non-core threads applies also to core threads. To avoid continual thread replacement, the keep-alive time must be greater than zero when setting`true`. This method should in general be called before the pool is actively used. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [allowsCoreThreadTimeOut](ThreadPoolExecutor.md))`()` <br /> Returns true if this pool allows core threads to time out and terminate if no tasks arrive within the keepAlive time, being replaced if needed when new tasks arrive. When true, the same keep-alive policy applying to non-core threads applies also to core threads. When false (the default), core threads are never terminated due to lack of incoming tasks. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [awaitTermination](ThreadPoolExecutor.md))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [beforeExecute](ThreadPoolExecutor.md))`(`t:` ` [Thread](../java.lang/Thread.md)!`, `r:` ` [Runnable](../java.lang/Runnable.md)!`)` <br /> Method invoked prior to executing the given Runnable in the given thread. This method is invoked by thread`t`that will execute task`r`, and may be used to re-initialize ThreadLocals, or to perform logging. This implementation does nothing, but may be customized in subclasses. Note: To properly nest multiple overridings, subclasses should generally invoke`super.beforeExecute`at the end of this method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](ThreadPoolExecutor.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getActiveCount](ThreadPoolExecutor.md))`()` <br /> Returns the approximate number of threads that are actively executing tasks. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCompletedTaskCount](ThreadPoolExecutor.md))`()` <br /> Returns the approximate total number of tasks that have completed execution. Because the states of tasks and threads may change dynamically during computation, the returned value is only an approximation, but one that does not ever decrease across successive calls. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCorePoolSize](ThreadPoolExecutor.md))`()` <br /> Returns the core number of threads. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getKeepAliveTime](ThreadPoolExecutor.md))`(`unit:` ` [TimeUnit](TimeUnit.md)!`)` <br /> Returns the thread keep-alive time, which is the amount of time that threads may remain idle before being terminated. Threads that wait this amount of time without processing a task will be terminated if there are more than the core number of threads currently in the pool, or if this pool [allows core thread timeout](ThreadPoolExecutor.md)). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLargestPoolSize](ThreadPoolExecutor.md))`()` <br /> Returns the largest number of threads that have ever simultaneously been in the pool. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaximumPoolSize](ThreadPoolExecutor.md))`()` <br /> Returns the maximum allowed number of threads. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPoolSize](ThreadPoolExecutor.md))`()` <br /> Returns the current number of threads in the pool. <br /> | | [RejectedExecutionHandler](RejectedExecutionHandler.md)! | [getRejectedExecutionHandler](ThreadPoolExecutor.md))`()` <br /> Returns the current handler for unexecutable tasks. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTaskCount](ThreadPoolExecutor.md))`()` <br /> Returns the approximate total number of tasks that have ever been scheduled for execution. Because the states of tasks and threads may change dynamically during computation, the returned value is only an approximation. <br /> | | [ThreadFactory](ThreadFactory.md)! | [getThreadFactory](ThreadPoolExecutor.md))`()` <br /> Returns the thread factory used to create new threads. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isShutdown](ThreadPoolExecutor.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTerminated](ThreadPoolExecutor.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTerminating](ThreadPoolExecutor.md))`()` <br /> Returns true if this executor is in the process of terminating after [shutdown](ThreadPoolExecutor.md))or [shutdownNow](ThreadPoolExecutor.md))but has not completely terminated. This method may be useful for debugging. A return of`true`reported a sufficient period after shutdown may indicate that submitted tasks have ignored or suppressed interruption, causing this executor not to properly terminate. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [prestartAllCoreThreads](ThreadPoolExecutor.md))`()` <br /> Starts all core threads, causing them to idly wait for work. This overrides the default policy of starting core threads only when new tasks are executed. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [prestartCoreThread](ThreadPoolExecutor.md))`()` <br /> Starts a core thread, causing it to idly wait for work. This overrides the default policy of starting core threads only when new tasks are executed. This method will return`false`if all core threads have already been started. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [purge](ThreadPoolExecutor.md))`()` <br /> Tries to remove from the work queue all [Future](Future.md) tasks that have been cancelled. This method can be useful as a storage reclamation operation, that has no other impact on functionality. Cancelled tasks are never executed, but may accumulate in work queues until worker threads can actively remove them. Invoking this method instead tries to remove them now. However, this method may fail to remove tasks in the presence of interference by other threads. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](ThreadPoolExecutor.md))`(`task:` ` [Runnable](../java.lang/Runnable.md)!`)` <br /> Removes this task from the executor's internal queue if it is present, thus causing it not to be run if it has not already started. This method may be useful as one part of a cancellation scheme. It may fail to remove tasks that have been converted into other forms before being placed on the internal queue. For example, a task entered using`submit`might be converted into a form that maintains`Future`status. However, in such cases, method [purge](ThreadPoolExecutor.md))may be used to remove those Futures that have been cancelled. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCorePoolSize](ThreadPoolExecutor.md))`(`corePoolSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the core number of threads. This overrides any value set in the constructor. If the new value is smaller than the current value, excess existing threads will be terminated when they next become idle. If larger, new threads will, if needed, be started to execute any queued tasks. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setKeepAliveTime](ThreadPoolExecutor.md))`(`time:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` <br /> Sets the thread keep-alive time, which is the amount of time that threads may remain idle before being terminated. Threads that wait this amount of time without processing a task will be terminated if there are more than the core number of threads currently in the pool, or if this pool [allows core thread timeout](ThreadPoolExecutor.md)). This overrides any value set in the constructor. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMaximumPoolSize](ThreadPoolExecutor.md))`(`maximumPoolSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the maximum allowed number of threads. This overrides any value set in the constructor. If the new value is smaller than the current value, excess existing threads will be terminated when they next become idle. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRejectedExecutionHandler](ThreadPoolExecutor.md))`(`handler:` ` [RejectedExecutionHandler](RejectedExecutionHandler.md)!`)` <br /> Sets a new handler for unexecutable tasks. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setThreadFactory](ThreadPoolExecutor.md))`(`threadFactory:` ` [ThreadFactory](ThreadFactory.md)!`)` <br /> Sets the thread factory used to create new threads. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [terminated](ThreadPoolExecutor.md))`()` <br /> Method invoked when the Executor has terminated. Default implementation does nothing. Note: To properly nest multiple overridings, subclasses should generally invoke`super.terminated`within this method. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](ThreadPoolExecutor.md))`()` <br /> Returns a string identifying this pool, as well as its state, including indications of run state and estimated worker and task counts. <br /> | ||
| From class [ExecutorService](ExecutorService.md) |------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [awaitTermination](ExecutorService.md))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` <br /> Blocks until all tasks have completed execution after a shutdown request, or the timeout occurs, or the current thread is interrupted, whichever happens first. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](ExecutorService.md))`()` <br /> Initiates an orderly shutdown in which previously submitted tasks are executed, but no new tasks will be accepted. This method waits until all tasks have completed execution and the executor has terminated. If interrupted while waiting, this method stops all executing tasks as if by invoking [shutdownNow()](ExecutorService.md)). It then continues to wait until all actively executing tasks have completed. Tasks that were awaiting execution are not executed. The interrupt status will be re-asserted before this method returns. If already terminated, invoking this method has no effect. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isShutdown](ExecutorService.md))`()` <br /> Returns`true`if this executor has been shut down. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTerminated](ExecutorService.md))`()` <br /> Returns`true`if all tasks have completed following shut down. Note that`isTerminated`is never`true`unless either`shutdown`or`shutdownNow`was called first. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [shutdown](ExecutorService.md))`()` <br /> Initiates an orderly shutdown in which previously submitted tasks are executed, but no new tasks will be accepted. Invocation has no additional effect if already shut down. This method does not wait for previously submitted tasks to complete execution. Use [awaitTermination](ExecutorService.md))to do that. <br /> | | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Runnable](../java.lang/Runnable.md)!>! | [shutdownNow](ExecutorService.md))`()` <br /> Attempts to stop all actively executing tasks, halts the processing of waiting tasks, and returns a list of the tasks that were awaiting execution. This method does not wait for actively executing tasks to terminate. Use [awaitTermination](ExecutorService.md))to do that. There are no guarantees beyond best-effort attempts to stop processing actively executing tasks. For example, typical implementations will cancel via [Thread.interrupt](../java.lang/Thread.md)), so any task that fails to respond to interrupts may never terminate. <br /> | ||
| From class [Executor](Executor.md) |------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [execute](Executor.md))`(`command:` ` [Runnable](../java.lang/Runnable.md)!`)` <br /> Executes the given command at some time in the future. The command may execute in a new thread, in a pooled thread, or in the calling thread, at the discretion of the`Executor`implementation. <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- |
| From class [AbstractExecutorService](AbstractExecutorService.md) |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Future](Future.md)<T>!>! | [invokeAll](AbstractExecutorService.md))`(`tasks:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` ` [Callable](Callable.md)<T>!>!`)` <br /> | | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Future](Future.md)<T>!>! | [invokeAll](AbstractExecutorService.md))`(`tasks:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` ` [Callable](Callable.md)<T>!>!`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` <br /> | | T | [invokeAny](AbstractExecutorService.md))`(`tasks:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` ` [Callable](Callable.md)<T>!>!`)` <br /> | | T | [invokeAny](AbstractExecutorService.md))`(`tasks:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` ` [Callable](Callable.md)<T>!>!`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` <br /> | | [RunnableFuture](RunnableFuture.md)<T>! | [newTaskFor](AbstractExecutorService.md))`(`runnable:` ` [Runnable](../java.lang/Runnable.md)!`, `value:` `T`)` <br /> Returns a`RunnableFuture`for the given runnable and default value. <br /> | | [RunnableFuture](RunnableFuture.md)<T>! | [newTaskFor](AbstractExecutorService.md))`(`callable:` ` [Callable](Callable.md)<T>!`)` <br /> Returns a`RunnableFuture`for the given callable task. <br /> | | [Future](Future.md)<*>! | [submit](AbstractExecutorService.md))`(`task:` ` [Runnable](../java.lang/Runnable.md)!`)` <br /> | | [Future](Future.md)<T>! | [submit](AbstractExecutorService.md))`(`task:` ` [Runnable](../java.lang/Runnable.md)!`, `result:` `T`)` <br /> | | [Future](Future.md)<T>! | [submit](AbstractExecutorService.md))`(`task:` ` [Callable](Callable.md)<T>!`)` <br /> | ||

## Public constructors

### ScheduledThreadPoolExecutor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ScheduledThreadPoolExecutor(corePoolSize: Int)
```

Creates a new`ScheduledThreadPoolExecutor`with the given core pool size.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `corePoolSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of threads to keep in the pool, even if they are idle, unless`allowCoreThreadTimeOut`is set |

| Exceptions ||
|--------------------------------------|----------------------|
| `java.lang.IllegalArgumentException` | if`corePoolSize < 0` |

### ScheduledThreadPoolExecutor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ScheduledThreadPoolExecutor(
    corePoolSize: Int, 
    handler: RejectedExecutionHandler!)
```

Creates a new`ScheduledThreadPoolExecutor`with the given initial parameters.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `corePoolSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of threads to keep in the pool, even if they are idle, unless`allowCoreThreadTimeOut`is set |
| `handler` | [RejectedExecutionHandler](RejectedExecutionHandler.md)!:the handler to use when execution is blocked because the thread bounds and queue capacities are reached |

| Exceptions ||
|--------------------------------------|----------------------|
| `java.lang.IllegalArgumentException` | if`corePoolSize < 0` |
| `java.lang.NullPointerException` | if`handler`is null |

### ScheduledThreadPoolExecutor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ScheduledThreadPoolExecutor(
    corePoolSize: Int, 
    threadFactory: ThreadFactory!)
```

Creates a new`ScheduledThreadPoolExecutor`with the given initial parameters.

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `corePoolSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of threads to keep in the pool, even if they are idle, unless`allowCoreThreadTimeOut`is set |
| `threadFactory` | [ThreadFactory](ThreadFactory.md)!:the factory to use when the executor creates a new thread |

| Exceptions ||
|--------------------------------------|--------------------------|
| `java.lang.IllegalArgumentException` | if`corePoolSize < 0` |
| `java.lang.NullPointerException` | if`threadFactory`is null |

### ScheduledThreadPoolExecutor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ScheduledThreadPoolExecutor(
    corePoolSize: Int, 
    threadFactory: ThreadFactory!, 
    handler: RejectedExecutionHandler!)
```

Creates a new`ScheduledThreadPoolExecutor`with the given initial parameters.

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `corePoolSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of threads to keep in the pool, even if they are idle, unless`allowCoreThreadTimeOut`is set |
| `threadFactory` | [ThreadFactory](ThreadFactory.md)!:the factory to use when the executor creates a new thread |
| `handler` | [RejectedExecutionHandler](RejectedExecutionHandler.md)!:the handler to use when execution is blocked because the thread bounds and queue capacities are reached |
| --- | --- |

| Exceptions ||
|--------------------------------------|-------------------------------------|
| `java.lang.IllegalArgumentException` | if`corePoolSize < 0` |
| `java.lang.NullPointerException` | if`threadFactory`or`handler`is null |

## Public methods

### execute

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun execute(command: Runnable!): Unit
```

Executes`command`with zero required delay. This has effect equivalent to [schedule(command, 0, anyUnit)](ScheduledThreadPoolExecutor.md)). Note that inspections of the queue and of the list returned by`shutdownNow`will access the zero-delayed [ScheduledFuture](ScheduledFuture.md), not the`command`itself.

A consequence of the use of`ScheduledFuture`objects is that [afterExecute](ThreadPoolExecutor.md))is always called with a null second`Throwable`argument, even if the`command`terminated abruptly. Instead, the`Throwable`thrown by such a task can be obtained via java.util.concurrent.Future#get.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------|
| `command` | [Runnable](../java.lang/Runnable.md)!:the runnable task |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| `java.util.concurrent.RejectedExecutionException` | at discretion of`RejectedExecutionHandler`, if the task cannot be accepted for execution because the executor has been shut down |
| `java.lang.NullPointerException` | if`command`is null |

### getContinueExistingPeriodicTasksAfterShutdownPolicy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getContinueExistingPeriodicTasksAfterShutdownPolicy(): Boolean
```

Gets the policy on whether to continue executing existing periodic tasks even when this executor has been`shutdown`. In this case, executions will continue until`shutdownNow`or the policy is set to`false`when already shutdown. This value is by default`false`.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if will continue after shutdown |

**See Also**

- [#setContinueExistingPeriodicTasksAfterShutdownPolicy](ScheduledThreadPoolExecutor.md)) 

### getExecuteExistingDelayedTasksAfterShutdownPolicy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getExecuteExistingDelayedTasksAfterShutdownPolicy(): Boolean
```

Gets the policy on whether to execute existing delayed tasks even when this executor has been`shutdown`. In this case, these tasks will only terminate upon`shutdownNow`, or after setting the policy to`false`when already shutdown. This value is by default`true`.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if will execute after shutdown |

**See Also**

- [#setExecuteExistingDelayedTasksAfterShutdownPolicy](ScheduledThreadPoolExecutor.md)) 

### getQueue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getQueue(): BlockingQueue<Runnable!>!
```

Returns the task queue used by this executor. Access to the task queue is intended primarily for debugging and monitoring. This queue may be in active use. Retrieving the task queue does not prevent queued tasks from executing.

Each element of this queue is a [ScheduledFuture](ScheduledFuture.md). For tasks submitted via one of the`schedule`methods, the element will be identical to the returned`ScheduledFuture`. For tasks submitted using [execute](ScheduledThreadPoolExecutor.md)), the element will be a zero-delay`ScheduledFuture`.

Iteration over this queue is*not*guaranteed to traverse tasks in the order in which they will execute.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------|
| [BlockingQueue](BlockingQueue.md)< [Runnable](../java.lang/Runnable.md)!>! | the task queue |

### getRemoveOnCancelPolicy

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRemoveOnCancelPolicy(): Boolean
```

Gets the policy on whether cancelled tasks should be immediately removed from the work queue at time of cancellation. This value is by default`false`.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if cancelled tasks are immediately removed from the queue |

**See Also**

- [#setRemoveOnCancelPolicy](ScheduledThreadPoolExecutor.md)) 

### schedule

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun schedule(
    command: Runnable!, 
    delay: Long, 
    unit: TimeUnit!
): ScheduledFuture<*>!
```

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------|
| `command` | [Runnable](../java.lang/Runnable.md)!:the task to execute |
| `delay` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the time from now to delay execution |
| `unit` | [TimeUnit](TimeUnit.md)!:the time unit of the delay parameter |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [ScheduledFuture](ScheduledFuture.md)<*>! | a ScheduledFuture representing pending completion of the task and whose`get()`method will return`null`upon completion |

| Exceptions ||
|---------------------------------------------------|-----------------------------------------------|
| `java.util.concurrent.RejectedExecutionException` | if the task cannot be scheduled for execution |
| `java.lang.NullPointerException` | if command or unit is null |

### schedule

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <V : Any!> schedule(
    callable: Callable<V>!, 
    delay: Long, 
    unit: TimeUnit!
): ScheduledFuture<V>!
```

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------|
| `callable` | [Callable](Callable.md)\<V\>!:the function to execute |
| `delay` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the time from now to delay execution |
| `unit` | [TimeUnit](TimeUnit.md)!:the time unit of the delay parameter |
| --- | --- |
| `<V>` | the type of the callable's result |

| Return ||
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [ScheduledFuture](ScheduledFuture.md)<V>! | a ScheduledFuture that can be used to extract result or cancel |

| Exceptions ||
|---------------------------------------------------|-----------------------------------------------|
| `java.util.concurrent.RejectedExecutionException` | if the task cannot be scheduled for execution |
| `java.lang.NullPointerException` | if callable or unit is null |

### scheduleAtFixedRate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun scheduleAtFixedRate(
    command: Runnable!, 
    initialDelay: Long, 
    period: Long, 
    unit: TimeUnit!
): ScheduledFuture<*>!
```

Submits a periodic action that becomes enabled first after the given initial delay, and subsequently with the given period; that is, executions will commence after`initialDelay`, then`initialDelay + period`, then`initialDelay + 2 * period`, and so on.

The sequence of task executions continues indefinitely until one of the following exceptional completions occur:

- The task is [explicitly cancelled](Future.md))via the returned future.
- Method [shutdown](ScheduledThreadPoolExecutor.md))is called and the [policy on](ScheduledThreadPoolExecutor.md))is not set true, or method [shutdownNow](ScheduledThreadPoolExecutor.md))is called; also resulting in task cancellation.
- An execution of the task throws an exception. In this case calling [get](Future.md))on the returned future will throw [ExecutionException](ExecutionException.md), holding the exception as its cause.

Subsequent executions are suppressed. Subsequent calls to [isDone()](Future.md))on the returned future will return`true`.

Since API level 31: If the app is frozen by the Android cached apps freezer before the fixed rate task is done or canceled, the task may run many times immediately when the app unfreezes, just as if a single execution of the command had taken the duration of the frozen period to execute.

Since API level 36: If any execution of this task takes longer than its period, then the subsequent execution will be scheduled for the most recent missed period.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `command` | [Runnable](../java.lang/Runnable.md)!:the task to execute |
| `initialDelay` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the time to delay first execution |
| `period` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the period between successive executions |
| --- | --- |
| `unit` | [TimeUnit](TimeUnit.md)!:the time unit of the initialDelay and period parameters |

| Return ||
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ScheduledFuture](ScheduledFuture.md)<*>! | a ScheduledFuture representing pending completion of the series of repeated tasks. The future's [get()](Future.md))method will never return normally, and will throw an exception upon task cancellation or abnormal termination of a task execution. |

| Exceptions ||
|---------------------------------------------------|-----------------------------------------------|
| `java.util.concurrent.RejectedExecutionException` | if the task cannot be scheduled for execution |
| `java.lang.NullPointerException` | if command or unit is null |
| `java.lang.IllegalArgumentException` | if period less than or equal to zero |
| --- | --- |

### scheduleWithFixedDelay

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun scheduleWithFixedDelay(
    command: Runnable!, 
    initialDelay: Long, 
    delay: Long, 
    unit: TimeUnit!
): ScheduledFuture<*>!
```

Submits a periodic action that becomes enabled first after the given initial delay, and subsequently with the given delay between the termination of one execution and the commencement of the next.

The sequence of task executions continues indefinitely until one of the following exceptional completions occur:

- The task is [explicitly cancelled](Future.md))via the returned future.
- Method [shutdown](ScheduledThreadPoolExecutor.md))is called and the [policy on](ScheduledThreadPoolExecutor.md))is not set true, or method [shutdownNow](ScheduledThreadPoolExecutor.md))is called; also resulting in task cancellation.
- An execution of the task throws an exception. In this case calling [get](Future.md))on the returned future will throw [ExecutionException](ExecutionException.md), holding the exception as its cause.

Subsequent executions are suppressed. Subsequent calls to [isDone()](Future.md))on the returned future will return`true`.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `command` | [Runnable](../java.lang/Runnable.md)!:the task to execute |
| `initialDelay` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the time to delay first execution |
| `delay` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the delay between the termination of one execution and the commencement of the next |
| --- | --- |
| `unit` | [TimeUnit](TimeUnit.md)!:the time unit of the initialDelay and delay parameters |

| Return ||
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ScheduledFuture](ScheduledFuture.md)<*>! | a ScheduledFuture representing pending completion of the series of repeated tasks. The future's [get()](Future.md))method will never return normally, and will throw an exception upon task cancellation or abnormal termination of a task execution. |

| Exceptions ||
|---------------------------------------------------|-----------------------------------------------|
| `java.util.concurrent.RejectedExecutionException` | if the task cannot be scheduled for execution |
| `java.lang.NullPointerException` | if command or unit is null |
| `java.lang.IllegalArgumentException` | if delay less than or equal to zero |
| --- | --- |

### setContinueExistingPeriodicTasksAfterShutdownPolicy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setContinueExistingPeriodicTasksAfterShutdownPolicy(value: Boolean): Unit
```

Sets the policy on whether to continue executing existing periodic tasks even when this executor has been`shutdown`. In this case, executions will continue until`shutdownNow`or the policy is set to`false`when already shutdown. This value is by default`false`.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if`true`, continue after shutdown, else don't |

**See Also**

- [#getContinueExistingPeriodicTasksAfterShutdownPolicy](ScheduledThreadPoolExecutor.md)) 

### setExecuteExistingDelayedTasksAfterShutdownPolicy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setExecuteExistingDelayedTasksAfterShutdownPolicy(value: Boolean): Unit
```

Sets the policy on whether to execute existing delayed tasks even when this executor has been`shutdown`. In this case, these tasks will only terminate upon`shutdownNow`, or after setting the policy to`false`when already shutdown. This value is by default`true`.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if`true`, execute after shutdown, else don't |

**See Also**

- [#getExecuteExistingDelayedTasksAfterShutdownPolicy](ScheduledThreadPoolExecutor.md)) 

### setRemoveOnCancelPolicy

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setRemoveOnCancelPolicy(value: Boolean): Unit
```

Sets the policy on whether cancelled tasks should be immediately removed from the work queue at time of cancellation. This value is by default`false`.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if`true`, remove on cancellation, else don't |

**See Also**

- [#getRemoveOnCancelPolicy](ScheduledThreadPoolExecutor.md)) 

### shutdown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun shutdown(): Unit
```

Initiates an orderly shutdown in which previously submitted tasks are executed, but no new tasks will be accepted. Invocation has no additional effect if already shut down.

This method does not wait for previously submitted tasks to complete execution. Use [awaitTermination](ThreadPoolExecutor.md))to do that.

If the`ExecuteExistingDelayedTasksAfterShutdownPolicy`has been set`false`, existing delayed tasks whose delays have not yet elapsed are cancelled. And unless the`ContinueExistingPeriodicTasksAfterShutdownPolicy`has been set`true`, future executions of existing periodic tasks will be cancelled. 

### shutdownNow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun shutdownNow(): MutableList<Runnable!>!
```

Attempts to stop all actively executing tasks, halts the processing of waiting tasks, and returns a list of the tasks that were awaiting execution. These tasks are drained (removed) from the task queue upon return from this method.

This method does not wait for actively executing tasks to terminate. Use [awaitTermination](ThreadPoolExecutor.md))to do that.

There are no guarantees beyond best-effort attempts to stop processing actively executing tasks. This implementation interrupts tasks via [Thread.interrupt](../java.lang/Thread.md)); any task that fails to respond to interrupts may never terminate.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Runnable](../java.lang/Runnable.md)!>! | list of tasks that never commenced execution. Each element of this list is a [ScheduledFuture](ScheduledFuture.md). For tasks submitted via one of the`schedule`methods, the element will be identical to the returned`ScheduledFuture`. For tasks submitted using [execute](ScheduledThreadPoolExecutor.md)), the element will be a zero-delay`ScheduledFuture`. |

### submit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun submit(task: Runnable!): Future<*>!
```

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------|
| `task` | [Runnable](../java.lang/Runnable.md)!:the task to submit |

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------------|
| [Future](Future.md)<*>! | a Future representing pending completion of the task |

| Exceptions ||
|---------------------------------------------------|-----------------------------------------------|
| `java.util.concurrent.RejectedExecutionException` | if the task cannot be scheduled for execution |
| `java.lang.NullPointerException` | if the task is null |

### submit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Any!> submit(
    task: Runnable!, 
    result: T
): Future<T>!
```

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------|
| `task` | [Runnable](../java.lang/Runnable.md)!:the task to submit |
| `result` | T:the result to return |
| `<T>` | the type of the result |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------------|
| [Future](Future.md)<T>! | a Future representing pending completion of the task |

| Exceptions ||
|---------------------------------------------------|-----------------------------------------------|
| `java.util.concurrent.RejectedExecutionException` | if the task cannot be scheduled for execution |
| `java.lang.NullPointerException` | if the task is null |

### submit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Any!> submit(task: Callable<T>!): Future<T>!
```

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------|
| `task` | [Callable](Callable.md)\<T\>!:the task to submit |
| `<T>` | the type of the task's result |

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------------|
| [Future](Future.md)<T>! | a Future representing pending completion of the task |

| Exceptions ||
|---------------------------------------------------|-----------------------------------------------|
| `java.util.concurrent.RejectedExecutionException` | if the task cannot be scheduled for execution |
| `java.lang.NullPointerException` | if the task is null |

## Protected methods

### decorateTask

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun <V : Any!> decorateTask(
    runnable: Runnable!, 
    task: RunnableScheduledFuture<V>!
): RunnableScheduledFuture<V>!
```

Modifies or replaces the task used to execute a runnable. This method can be used to override the concrete class used for managing internal tasks. The default implementation simply returns the given task.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `runnable` | [Runnable](../java.lang/Runnable.md)!:the submitted Runnable |
| `task` | [RunnableScheduledFuture](RunnableScheduledFuture.md)\<V\>!:the task created to execute the runnable |
| `<V>` | the type of the task's result |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| [RunnableScheduledFuture](RunnableScheduledFuture.md)<V>! | a task that can execute the runnable |

### decorateTask

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun <V : Any!> decorateTask(
    callable: Callable<V>!, 
    task: RunnableScheduledFuture<V>!
): RunnableScheduledFuture<V>!
```

Modifies or replaces the task used to execute a callable. This method can be used to override the concrete class used for managing internal tasks. The default implementation simply returns the given task.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callable` | [Callable](Callable.md)\<V\>!:the submitted Callable |
| `task` | [RunnableScheduledFuture](RunnableScheduledFuture.md)\<V\>!:the task created to execute the callable |
| `<V>` | the type of the task's result |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| [RunnableScheduledFuture](RunnableScheduledFuture.md)<V>! | a task that can execute the callable |
