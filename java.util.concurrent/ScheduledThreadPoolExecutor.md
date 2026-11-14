# ScheduledThreadPoolExecutor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScheduledThreadPoolExecutor

```
open class ScheduledThreadPoolExecutor : ThreadPoolExecutor, ScheduledExecutorService
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [java.util.concurrent.AbstractExecutorService](https://developer.android.com/reference/kotlin/java/util/concurrent/AbstractExecutorService) |||
| | ↳ | [java.util.concurrent.ThreadPoolExecutor](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor) ||
| | | ↳ | [java.util.concurrent.ScheduledThreadPoolExecutor](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#) |

A [ThreadPoolExecutor](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor) that can additionally schedule commands to run after a given delay, or to execute periodically. This class is preferable to [java.util.Timer](https://developer.android.com/reference/kotlin/java/util/Timer.html#) when multiple worker threads are needed, or when the additional flexibility or capabilities of [ThreadPoolExecutor](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor)(which this class extends) are required.

Delayed tasks execute no sooner than they are enabled, but without any real-time guarantees about when, after they are enabled, they will commence. Tasks scheduled for exactly the same execution time are enabled in first-in-first-out (FIFO) order of submission.

When a submitted task is cancelled before it is run, execution is suppressed. By default, such a cancelled task is not automatically removed from the work queue until its delay elapses. While this enables further inspection and monitoring, it may also cause unbounded retention of cancelled tasks.

Successive executions of a periodic task scheduled via [scheduleAtFixedRate](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#scheduleAtFixedRate(java.lang.Runnable,%20kotlin.Long,%20kotlin.Long,%20java.util.concurrent.TimeUnit))or [scheduleWithFixedDelay](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#scheduleWithFixedDelay(java.lang.Runnable,%20kotlin.Long,%20kotlin.Long,%20java.util.concurrent.TimeUnit))do not overlap. While different executions may be performed by different threads, the effects of prior executions [*happen-before*](https://developer.android.com/reference/kotlin/java/util/concurrent/package-summary#MemoryVisibility) those of subsequent ones.

While this class inherits from [ThreadPoolExecutor](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor), a few of the inherited tuning methods are not useful for it. In particular, because it acts as a fixed-sized pool using`corePoolSize`threads and an unbounded queue, adjustments to`maximumPoolSize`have no useful effect. Additionally, it is almost never a good idea to set`corePoolSize`to zero or use`allowCoreThreadTimeOut`because this may leave the pool without threads to handle tasks once they become eligible to run.

As with`ThreadPoolExecutor`, if not otherwise specified, this class uses [Executors.defaultThreadFactory](https://developer.android.com/reference/kotlin/java/util/concurrent/Executors#defaultThreadFactory())as the default thread factory, and [ThreadPoolExecutor.AbortPolicy](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor.AbortPolicy) as the default rejected execution handler.

**Extension notes:** This class overrides the [execute](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#execute(java.lang.Runnable))and [submit](https://developer.android.com/reference/kotlin/java/util/concurrent/AbstractExecutorService#submit(java.lang.Runnable))methods to generate internal [ScheduledFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledFuture) objects to control per-task delays and scheduling. To preserve functionality, any further overrides of these methods in subclasses must invoke superclass versions, which effectively disables additional task customization. However, this class provides alternative protected extension method`decorateTask`(one version each for`Runnable`and`Callable`) that can be used to customize the concrete task types used to execute commands entered via`execute`,`submit`,`schedule`,`scheduleAtFixedRate`, and`scheduleWithFixedDelay`. By default, a`ScheduledThreadPoolExecutor`uses a task type extending [FutureTask](https://developer.android.com/reference/kotlin/java/util/concurrent/FutureTask). However, this may be modified or replaced using subclasses of the form: 

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
| [ScheduledThreadPoolExecutor](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#ScheduledThreadPoolExecutor(kotlin.Int))`(`corePoolSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new`ScheduledThreadPoolExecutor`with the given core pool size. |
| [ScheduledThreadPoolExecutor](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#ScheduledThreadPoolExecutor(kotlin.Int,%20java.util.concurrent.RejectedExecutionHandler))`(`corePoolSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `handler:` ` [RejectedExecutionHandler](https://developer.android.com/reference/kotlin/java/util/concurrent/RejectedExecutionHandler)!`)` Creates a new`ScheduledThreadPoolExecutor`with the given initial parameters. |
| [ScheduledThreadPoolExecutor](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#ScheduledThreadPoolExecutor(kotlin.Int,%20java.util.concurrent.ThreadFactory))`(`corePoolSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `threadFactory:` ` [ThreadFactory](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadFactory)!`)` Creates a new`ScheduledThreadPoolExecutor`with the given initial parameters. |
| [ScheduledThreadPoolExecutor](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#ScheduledThreadPoolExecutor(kotlin.Int,%20java.util.concurrent.ThreadFactory,%20java.util.concurrent.RejectedExecutionHandler))`(`corePoolSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `threadFactory:` ` [ThreadFactory](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadFactory)!`, `handler:` ` [RejectedExecutionHandler](https://developer.android.com/reference/kotlin/java/util/concurrent/RejectedExecutionHandler)!`)` Creates a new`ScheduledThreadPoolExecutor`with the given initial parameters. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [execute](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#execute(java.lang.Runnable))`(`command:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`)` Executes`command`with zero required delay. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getContinueExistingPeriodicTasksAfterShutdownPolicy](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#getContinueExistingPeriodicTasksAfterShutdownPolicy())`()` Gets the policy on whether to continue executing existing periodic tasks even when this executor has been`shutdown`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getExecuteExistingDelayedTasksAfterShutdownPolicy](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#getExecuteExistingDelayedTasksAfterShutdownPolicy())`()` Gets the policy on whether to execute existing delayed tasks even when this executor has been`shutdown`. |
| open [BlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue)\< [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!\>! | [getQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#getQueue())`()` Returns the task queue used by this executor. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getRemoveOnCancelPolicy](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#getRemoveOnCancelPolicy())`()` Gets the policy on whether cancelled tasks should be immediately removed from the work queue at time of cancellation. |
| open [ScheduledFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledFuture)\<\*\>! | [schedule](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#schedule(java.lang.Runnable,%20kotlin.Long,%20java.util.concurrent.TimeUnit))`(`command:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`, `delay:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` <br /> |
| open [ScheduledFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledFuture)\<V\>! | [schedule](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#schedule(java.util.concurrent.Callable,%20kotlin.Long,%20java.util.concurrent.TimeUnit))`(`callable:` ` [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable)<V>!`, `delay:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` <br /> |
| open [ScheduledFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledFuture)\<\*\>! | [scheduleAtFixedRate](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#scheduleAtFixedRate(java.lang.Runnable,%20kotlin.Long,%20kotlin.Long,%20java.util.concurrent.TimeUnit))`(`command:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`, `initialDelay:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `period:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` Submits a periodic action that becomes enabled first after the given initial delay, and subsequently with the given period; that is, executions will commence after`initialDelay`, then`initialDelay + period`, then`initialDelay + 2 * period`, and so on. |
| open [ScheduledFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledFuture)\<\*\>! | [scheduleWithFixedDelay](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#scheduleWithFixedDelay(java.lang.Runnable,%20kotlin.Long,%20kotlin.Long,%20java.util.concurrent.TimeUnit))`(`command:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`, `initialDelay:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `delay:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` Submits a periodic action that becomes enabled first after the given initial delay, and subsequently with the given delay between the termination of one execution and the commencement of the next. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContinueExistingPeriodicTasksAfterShutdownPolicy](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#setContinueExistingPeriodicTasksAfterShutdownPolicy(kotlin.Boolean))`(`value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the policy on whether to continue executing existing periodic tasks even when this executor has been`shutdown`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setExecuteExistingDelayedTasksAfterShutdownPolicy](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#setExecuteExistingDelayedTasksAfterShutdownPolicy(kotlin.Boolean))`(`value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the policy on whether to execute existing delayed tasks even when this executor has been`shutdown`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRemoveOnCancelPolicy](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#setRemoveOnCancelPolicy(kotlin.Boolean))`(`value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the policy on whether cancelled tasks should be immediately removed from the work queue at time of cancellation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [shutdown](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#shutdown())`()` Initiates an orderly shutdown in which previously submitted tasks are executed, but no new tasks will be accepted. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!\>! | [shutdownNow](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#shutdownNow())`()` Attempts to stop all actively executing tasks, halts the processing of waiting tasks, and returns a list of the tasks that were awaiting execution. |
| open [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)\<\*\>! | [submit](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#submit(java.lang.Runnable))`(`task:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`)` <br /> |
| open [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)\<T\>! | [submit](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#submit(java.lang.Runnable,%20java.util.concurrent.ScheduledThreadPoolExecutor.submit.T))`(`task:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`, `result:` `T`)` <br /> |
| open [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)\<T\>! | [submit](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#submit(java.util.concurrent.Callable))`(`task:` ` [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable)<T>!`)` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [RunnableScheduledFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/RunnableScheduledFuture)\<V\>! | [decorateTask](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#decorateTask(java.lang.Runnable,%20java.util.concurrent.RunnableScheduledFuture))`(`runnable:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`, `task:` ` [RunnableScheduledFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/RunnableScheduledFuture)<V>!`)` Modifies or replaces the task used to execute a runnable. |
| open [RunnableScheduledFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/RunnableScheduledFuture)\<V\>! | [decorateTask](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#decorateTask(java.util.concurrent.Callable,%20java.util.concurrent.RunnableScheduledFuture))`(`callable:` ` [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable)<V>!`, `task:` ` [RunnableScheduledFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/RunnableScheduledFuture)<V>!`)` Modifies or replaces the task used to execute a callable. |

| Inherited functions ||
|---|---|
| From class [ThreadPoolExecutor](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor) |---------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [afterExecute](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#afterExecute(java.lang.Runnable,%20kotlin.Throwable))`(`r:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`, `t:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> Method invoked upon completion of execution of the given Runnable. This method is invoked by the thread that executed the task. If non-null, the Throwable is the uncaught`RuntimeException`or`Error`that caused execution to terminate abruptly. This implementation does nothing, but may be customized in subclasses. Note: To properly nest multiple overridings, subclasses should generally invoke`super.afterExecute`at the beginning of this method. **Note:** When actions are enclosed in tasks (such as [FutureTask](https://developer.android.com/reference/kotlin/java/util/concurrent/FutureTask)) either explicitly or via methods such as`submit`, these task objects catch and maintain computational exceptions, and so they do not cause abrupt termination, and the internal exceptions are*not*passed to this method. If you would like to trap both kinds of failures in this method, you can further probe for such cases, as in this sample subclass that prints either the direct cause or the underlying exception if a task has been aborted: ```kotlin <code>class ExtendedExecutor extends ThreadPoolExecutor { // ... protected void afterExecute(Runnable r, Throwable t) { super.afterExecute(r, t); if (t == null &amp;&amp; r instanceof Future&lt;?&gt; &amp;&amp; ((Future&lt;?&gt;)r).isDone()) { try { Object result = ((Future&lt;?&gt;) r).get(); } catch (CancellationException ce) { t = ce; } catch (ExecutionException ee) { t = ee.getCause(); } catch (InterruptedException ie) { // ignore/reset Thread.currentThread().interrupt(); } } if (t != null) System.out.println(t); } }</code> ``` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [allowCoreThreadTimeOut](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#allowCoreThreadTimeOut(kotlin.Boolean))`(`value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets the policy governing whether core threads may time out and terminate if no tasks arrive within the keep-alive time, being replaced if needed when new tasks arrive. When false, core threads are never terminated due to lack of incoming tasks. When true, the same keep-alive policy applying to non-core threads applies also to core threads. To avoid continual thread replacement, the keep-alive time must be greater than zero when setting`true`. This method should in general be called before the pool is actively used. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [allowsCoreThreadTimeOut](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#allowsCoreThreadTimeOut())`()` <br /> Returns true if this pool allows core threads to time out and terminate if no tasks arrive within the keepAlive time, being replaced if needed when new tasks arrive. When true, the same keep-alive policy applying to non-core threads applies also to core threads. When false (the default), core threads are never terminated due to lack of incoming tasks. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [awaitTermination](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#awaitTermination(kotlin.Long,%20java.util.concurrent.TimeUnit))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [beforeExecute](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#beforeExecute(java.lang.Thread,%20java.lang.Runnable))`(`t:` ` [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread.html#)!`, `r:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`)` <br /> Method invoked prior to executing the given Runnable in the given thread. This method is invoked by thread`t`that will execute task`r`, and may be used to re-initialize ThreadLocals, or to perform logging. This implementation does nothing, but may be customized in subclasses. Note: To properly nest multiple overridings, subclasses should generally invoke`super.beforeExecute`at the end of this method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#finalize())`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getActiveCount](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#getActiveCount())`()` <br /> Returns the approximate number of threads that are actively executing tasks. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCompletedTaskCount](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#getCompletedTaskCount())`()` <br /> Returns the approximate total number of tasks that have completed execution. Because the states of tasks and threads may change dynamically during computation, the returned value is only an approximation, but one that does not ever decrease across successive calls. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCorePoolSize](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#getCorePoolSize())`()` <br /> Returns the core number of threads. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getKeepAliveTime](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#getKeepAliveTime(java.util.concurrent.TimeUnit))`(`unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` <br /> Returns the thread keep-alive time, which is the amount of time that threads may remain idle before being terminated. Threads that wait this amount of time without processing a task will be terminated if there are more than the core number of threads currently in the pool, or if this pool [allows core thread timeout](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#allowsCoreThreadTimeOut()). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLargestPoolSize](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#getLargestPoolSize())`()` <br /> Returns the largest number of threads that have ever simultaneously been in the pool. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaximumPoolSize](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#getMaximumPoolSize())`()` <br /> Returns the maximum allowed number of threads. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPoolSize](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#getPoolSize())`()` <br /> Returns the current number of threads in the pool. <br /> | | [RejectedExecutionHandler](https://developer.android.com/reference/kotlin/java/util/concurrent/RejectedExecutionHandler)! | [getRejectedExecutionHandler](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#getRejectedExecutionHandler())`()` <br /> Returns the current handler for unexecutable tasks. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTaskCount](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#getTaskCount())`()` <br /> Returns the approximate total number of tasks that have ever been scheduled for execution. Because the states of tasks and threads may change dynamically during computation, the returned value is only an approximation. <br /> | | [ThreadFactory](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadFactory)! | [getThreadFactory](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#getThreadFactory())`()` <br /> Returns the thread factory used to create new threads. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isShutdown](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#isShutdown())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTerminated](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#isTerminated())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTerminating](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#isTerminating())`()` <br /> Returns true if this executor is in the process of terminating after [shutdown](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#shutdown())or [shutdownNow](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#shutdownNow())but has not completely terminated. This method may be useful for debugging. A return of`true`reported a sufficient period after shutdown may indicate that submitted tasks have ignored or suppressed interruption, causing this executor not to properly terminate. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [prestartAllCoreThreads](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#prestartAllCoreThreads())`()` <br /> Starts all core threads, causing them to idly wait for work. This overrides the default policy of starting core threads only when new tasks are executed. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [prestartCoreThread](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#prestartCoreThread())`()` <br /> Starts a core thread, causing it to idly wait for work. This overrides the default policy of starting core threads only when new tasks are executed. This method will return`false`if all core threads have already been started. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [purge](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#purge())`()` <br /> Tries to remove from the work queue all [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future) tasks that have been cancelled. This method can be useful as a storage reclamation operation, that has no other impact on functionality. Cancelled tasks are never executed, but may accumulate in work queues until worker threads can actively remove them. Invoking this method instead tries to remove them now. However, this method may fail to remove tasks in the presence of interference by other threads. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#remove(java.lang.Runnable))`(`task:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`)` <br /> Removes this task from the executor's internal queue if it is present, thus causing it not to be run if it has not already started. This method may be useful as one part of a cancellation scheme. It may fail to remove tasks that have been converted into other forms before being placed on the internal queue. For example, a task entered using`submit`might be converted into a form that maintains`Future`status. However, in such cases, method [purge](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#purge())may be used to remove those Futures that have been cancelled. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCorePoolSize](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#setCorePoolSize(kotlin.Int))`(`corePoolSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the core number of threads. This overrides any value set in the constructor. If the new value is smaller than the current value, excess existing threads will be terminated when they next become idle. If larger, new threads will, if needed, be started to execute any queued tasks. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setKeepAliveTime](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#setKeepAliveTime(kotlin.Long,%20java.util.concurrent.TimeUnit))`(`time:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` <br /> Sets the thread keep-alive time, which is the amount of time that threads may remain idle before being terminated. Threads that wait this amount of time without processing a task will be terminated if there are more than the core number of threads currently in the pool, or if this pool [allows core thread timeout](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#allowsCoreThreadTimeOut()). This overrides any value set in the constructor. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMaximumPoolSize](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#setMaximumPoolSize(kotlin.Int))`(`maximumPoolSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the maximum allowed number of threads. This overrides any value set in the constructor. If the new value is smaller than the current value, excess existing threads will be terminated when they next become idle. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRejectedExecutionHandler](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#setRejectedExecutionHandler(java.util.concurrent.RejectedExecutionHandler))`(`handler:` ` [RejectedExecutionHandler](https://developer.android.com/reference/kotlin/java/util/concurrent/RejectedExecutionHandler)!`)` <br /> Sets a new handler for unexecutable tasks. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setThreadFactory](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#setThreadFactory(java.util.concurrent.ThreadFactory))`(`threadFactory:` ` [ThreadFactory](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadFactory)!`)` <br /> Sets the thread factory used to create new threads. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [terminated](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#terminated())`()` <br /> Method invoked when the Executor has terminated. Default implementation does nothing. Note: To properly nest multiple overridings, subclasses should generally invoke`super.terminated`within this method. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#toString())`()` <br /> Returns a string identifying this pool, as well as its state, including indications of run state and estimated worker and task counts. <br /> | ||
| From class [ExecutorService](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService) |------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [awaitTermination](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService#awaitTermination(kotlin.Long,%20java.util.concurrent.TimeUnit))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` <br /> Blocks until all tasks have completed execution after a shutdown request, or the timeout occurs, or the current thread is interrupted, whichever happens first. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService#close())`()` <br /> Initiates an orderly shutdown in which previously submitted tasks are executed, but no new tasks will be accepted. This method waits until all tasks have completed execution and the executor has terminated. If interrupted while waiting, this method stops all executing tasks as if by invoking [shutdownNow()](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService#shutdownNow()). It then continues to wait until all actively executing tasks have completed. Tasks that were awaiting execution are not executed. The interrupt status will be re-asserted before this method returns. If already terminated, invoking this method has no effect. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isShutdown](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService#isShutdown())`()` <br /> Returns`true`if this executor has been shut down. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTerminated](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService#isTerminated())`()` <br /> Returns`true`if all tasks have completed following shut down. Note that`isTerminated`is never`true`unless either`shutdown`or`shutdownNow`was called first. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [shutdown](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService#shutdown())`()` <br /> Initiates an orderly shutdown in which previously submitted tasks are executed, but no new tasks will be accepted. Invocation has no additional effect if already shut down. This method does not wait for previously submitted tasks to complete execution. Use [awaitTermination](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService#awaitTermination(kotlin.Long,%20java.util.concurrent.TimeUnit))to do that. <br /> | | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!>! | [shutdownNow](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService#shutdownNow())`()` <br /> Attempts to stop all actively executing tasks, halts the processing of waiting tasks, and returns a list of the tasks that were awaiting execution. This method does not wait for actively executing tasks to terminate. Use [awaitTermination](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService#awaitTermination(kotlin.Long,%20java.util.concurrent.TimeUnit))to do that. There are no guarantees beyond best-effort attempts to stop processing actively executing tasks. For example, typical implementations will cancel via [Thread.interrupt](https://developer.android.com/reference/kotlin/java/lang/Thread.html#interrupt()), so any task that fails to respond to interrupts may never terminate. <br /> | ||
| From class [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor) |------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [execute](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor#execute(java.lang.Runnable))`(`command:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`)` <br /> Executes the given command at some time in the future. The command may execute in a new thread, in a pooled thread, or in the calling thread, at the discretion of the`Executor`implementation. <br /> | ||
| From class [AbstractExecutorService](https://developer.android.com/reference/kotlin/java/util/concurrent/AbstractExecutorService) |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)<T>!>! | [invokeAll](https://developer.android.com/reference/kotlin/java/util/concurrent/AbstractExecutorService#invokeAll(kotlin.collections.MutableCollection))`(`tasks:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` ` [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable)<T>!>!`)` <br /> | | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)<T>!>! | [invokeAll](https://developer.android.com/reference/kotlin/java/util/concurrent/AbstractExecutorService#invokeAll(kotlin.collections.MutableCollection,%20kotlin.Long,%20java.util.concurrent.TimeUnit))`(`tasks:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` ` [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable)<T>!>!`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` <br /> | | T | [invokeAny](https://developer.android.com/reference/kotlin/java/util/concurrent/AbstractExecutorService#invokeAny(kotlin.collections.MutableCollection))`(`tasks:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` ` [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable)<T>!>!`)` <br /> | | T | [invokeAny](https://developer.android.com/reference/kotlin/java/util/concurrent/AbstractExecutorService#invokeAny(kotlin.collections.MutableCollection,%20kotlin.Long,%20java.util.concurrent.TimeUnit))`(`tasks:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` ` [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable)<T>!>!`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` <br /> | | [RunnableFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/RunnableFuture)<T>! | [newTaskFor](https://developer.android.com/reference/kotlin/java/util/concurrent/AbstractExecutorService#newTaskFor(java.lang.Runnable,%20java.util.concurrent.AbstractExecutorService.newTaskFor.T))`(`runnable:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`, `value:` `T`)` <br /> Returns a`RunnableFuture`for the given runnable and default value. <br /> | | [RunnableFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/RunnableFuture)<T>! | [newTaskFor](https://developer.android.com/reference/kotlin/java/util/concurrent/AbstractExecutorService#newTaskFor(java.util.concurrent.Callable))`(`callable:` ` [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable)<T>!`)` <br /> Returns a`RunnableFuture`for the given callable task. <br /> | | [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)<*>! | [submit](https://developer.android.com/reference/kotlin/java/util/concurrent/AbstractExecutorService#submit(java.lang.Runnable))`(`task:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`)` <br /> | | [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)<T>! | [submit](https://developer.android.com/reference/kotlin/java/util/concurrent/AbstractExecutorService#submit(java.lang.Runnable,%20java.util.concurrent.AbstractExecutorService.submit.T))`(`task:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`, `result:` `T`)` <br /> | | [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)<T>! | [submit](https://developer.android.com/reference/kotlin/java/util/concurrent/AbstractExecutorService#submit(java.util.concurrent.Callable))`(`task:` ` [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable)<T>!`)` <br /> | ||

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
| `handler` | [RejectedExecutionHandler](https://developer.android.com/reference/kotlin/java/util/concurrent/RejectedExecutionHandler)!:the handler to use when execution is blocked because the thread bounds and queue capacities are reached |

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
| `threadFactory` | [ThreadFactory](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadFactory)!:the factory to use when the executor creates a new thread |

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
| `threadFactory` | [ThreadFactory](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadFactory)!:the factory to use when the executor creates a new thread |
| `handler` | [RejectedExecutionHandler](https://developer.android.com/reference/kotlin/java/util/concurrent/RejectedExecutionHandler)!:the handler to use when execution is blocked because the thread bounds and queue capacities are reached |

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

Executes`command`with zero required delay. This has effect equivalent to [schedule(command, 0, anyUnit)](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#schedule(java.lang.Runnable,%20kotlin.Long,%20java.util.concurrent.TimeUnit)). Note that inspections of the queue and of the list returned by`shutdownNow`will access the zero-delayed [ScheduledFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledFuture), not the`command`itself.

A consequence of the use of`ScheduledFuture`objects is that [afterExecute](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#afterExecute(java.lang.Runnable,%20kotlin.Throwable))is always called with a null second`Throwable`argument, even if the`command`terminated abruptly. Instead, the`Throwable`thrown by such a task can be obtained via java.util.concurrent.Future#get.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------|
| `command` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!:the runnable task |

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

- [#setContinueExistingPeriodicTasksAfterShutdownPolicy](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#setContinueExistingPeriodicTasksAfterShutdownPolicy(kotlin.Boolean)) 

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

- [#setExecuteExistingDelayedTasksAfterShutdownPolicy](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#setExecuteExistingDelayedTasksAfterShutdownPolicy(kotlin.Boolean)) 

### getQueue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getQueue(): BlockingQueue<Runnable!>!
```

Returns the task queue used by this executor. Access to the task queue is intended primarily for debugging and monitoring. This queue may be in active use. Retrieving the task queue does not prevent queued tasks from executing.

Each element of this queue is a [ScheduledFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledFuture). For tasks submitted via one of the`schedule`methods, the element will be identical to the returned`ScheduledFuture`. For tasks submitted using [execute](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#execute(java.lang.Runnable)), the element will be a zero-delay`ScheduledFuture`.

Iteration over this queue is*not*guaranteed to traverse tasks in the order in which they will execute.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------|
| [BlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue)< [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!>! | the task queue |

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

- [#setRemoveOnCancelPolicy](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#setRemoveOnCancelPolicy(kotlin.Boolean)) 

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
open fun <V : Any!> schedule(
    callable: Callable<V>!, 
    delay: Long, 
    unit: TimeUnit!
): ScheduledFuture<V>!
```

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
open fun scheduleAtFixedRate(
    command: Runnable!, 
    initialDelay: Long, 
    period: Long, 
    unit: TimeUnit!
): ScheduledFuture<*>!
```

Submits a periodic action that becomes enabled first after the given initial delay, and subsequently with the given period; that is, executions will commence after`initialDelay`, then`initialDelay + period`, then`initialDelay + 2 * period`, and so on.

The sequence of task executions continues indefinitely until one of the following exceptional completions occur:

- The task is [explicitly cancelled](https://developer.android.com/reference/kotlin/java/util/concurrent/Future#cancel(kotlin.Boolean))via the returned future.
- Method [shutdown](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#shutdown())is called and the [policy on](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#getContinueExistingPeriodicTasksAfterShutdownPolicy())is not set true, or method [shutdownNow](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#shutdownNow())is called; also resulting in task cancellation.
- An execution of the task throws an exception. In this case calling [get](https://developer.android.com/reference/kotlin/java/util/concurrent/Future#get())on the returned future will throw [ExecutionException](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutionException), holding the exception as its cause.

Subsequent executions are suppressed. Subsequent calls to [isDone()](https://developer.android.com/reference/kotlin/java/util/concurrent/Future#isDone())on the returned future will return`true`.

Since API level 31: If the app is frozen by the Android cached apps freezer before the fixed rate task is done or canceled, the task may run many times immediately when the app unfreezes, just as if a single execution of the command had taken the duration of the frozen period to execute.

Since API level 36: If any execution of this task takes longer than its period, then the subsequent execution will be scheduled for the most recent missed period.

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
open fun scheduleWithFixedDelay(
    command: Runnable!, 
    initialDelay: Long, 
    delay: Long, 
    unit: TimeUnit!
): ScheduledFuture<*>!
```

Submits a periodic action that becomes enabled first after the given initial delay, and subsequently with the given delay between the termination of one execution and the commencement of the next.

The sequence of task executions continues indefinitely until one of the following exceptional completions occur:

- The task is [explicitly cancelled](https://developer.android.com/reference/kotlin/java/util/concurrent/Future#cancel(kotlin.Boolean))via the returned future.
- Method [shutdown](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#shutdown())is called and the [policy on](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#getContinueExistingPeriodicTasksAfterShutdownPolicy())is not set true, or method [shutdownNow](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#shutdownNow())is called; also resulting in task cancellation.
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

- [#getContinueExistingPeriodicTasksAfterShutdownPolicy](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#getContinueExistingPeriodicTasksAfterShutdownPolicy()) 

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

- [#getExecuteExistingDelayedTasksAfterShutdownPolicy](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#getExecuteExistingDelayedTasksAfterShutdownPolicy()) 

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

- [#getRemoveOnCancelPolicy](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#getRemoveOnCancelPolicy()) 

### shutdown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun shutdown(): Unit
```

Initiates an orderly shutdown in which previously submitted tasks are executed, but no new tasks will be accepted. Invocation has no additional effect if already shut down.

This method does not wait for previously submitted tasks to complete execution. Use [awaitTermination](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#awaitTermination(kotlin.Long,%20java.util.concurrent.TimeUnit))to do that.

If the`ExecuteExistingDelayedTasksAfterShutdownPolicy`has been set`false`, existing delayed tasks whose delays have not yet elapsed are cancelled. And unless the`ContinueExistingPeriodicTasksAfterShutdownPolicy`has been set`true`, future executions of existing periodic tasks will be cancelled. 

### shutdownNow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun shutdownNow(): MutableList<Runnable!>!
```

Attempts to stop all actively executing tasks, halts the processing of waiting tasks, and returns a list of the tasks that were awaiting execution. These tasks are drained (removed) from the task queue upon return from this method.

This method does not wait for actively executing tasks to terminate. Use [awaitTermination](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#awaitTermination(kotlin.Long,%20java.util.concurrent.TimeUnit))to do that.

There are no guarantees beyond best-effort attempts to stop processing actively executing tasks. This implementation interrupts tasks via [Thread.interrupt](https://developer.android.com/reference/kotlin/java/lang/Thread.html#interrupt()); any task that fails to respond to interrupts may never terminate.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!>! | list of tasks that never commenced execution. Each element of this list is a [ScheduledFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledFuture). For tasks submitted via one of the`schedule`methods, the element will be identical to the returned`ScheduledFuture`. For tasks submitted using [execute](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor#execute(java.lang.Runnable)), the element will be a zero-delay`ScheduledFuture`. |

### submit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun submit(task: Runnable!): Future<*>!
```

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------|
| `task` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!:the task to submit |

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------------|
| [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)<*>! | a Future representing pending completion of the task |

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
| `task` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!:the task to submit |
| `result` | T:the result to return |
| `<T>` | the type of the result |

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------------|
| [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)<T>! | a Future representing pending completion of the task |

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
| `task` | [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable)\<T\>!:the task to submit |
| `<T>` | the type of the task's result |

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------------|
| [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)<T>! | a Future representing pending completion of the task |

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
| `runnable` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!:the submitted Runnable |
| `task` | [RunnableScheduledFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/RunnableScheduledFuture)\<V\>!:the task created to execute the runnable |
| `<V>` | the type of the task's result |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| [RunnableScheduledFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/RunnableScheduledFuture)<V>! | a task that can execute the runnable |

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
| `callable` | [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable)\<V\>!:the submitted Callable |
| `task` | [RunnableScheduledFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/RunnableScheduledFuture)\<V\>!:the task created to execute the callable |
| `<V>` | the type of the task's result |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| [RunnableScheduledFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/RunnableScheduledFuture)<V>! | a task that can execute the callable |
