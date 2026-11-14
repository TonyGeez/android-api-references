Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ThreadPoolExecutor

```
open class ThreadPoolExecutor : AbstractExecutorService
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.concurrent.AbstractExecutorService](https://developer.android.com/reference/kotlin/java/util/concurrent/AbstractExecutorService) ||
| | ↳ | [java.util.concurrent.ThreadPoolExecutor](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#) |

| Known Direct Subclasses [ScheduledThreadPoolExecutor](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor) |---|---| | [ScheduledThreadPoolExecutor](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledThreadPoolExecutor) | A `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#` that can additionally schedule commands to run after a given delay, or to execute periodically. | |
| --- | --- | --- | --- | --- | --- | --- |

An `https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService` that executes each submitted task using one of possibly several pooled threads, normally configured using `https://developer.android.com/reference/kotlin/java/util/concurrent/Executors` factory methods.

Thread pools address two different problems: they usually provide improved performance when executing large numbers of asynchronous tasks, due to reduced per-task invocation overhead, and they provide a means of bounding and managing the resources, including threads, consumed when executing a collection of tasks. Each `ThreadPoolExecutor` also maintains some basic statistics, such as the number of completed tasks.

To be useful across a wide range of contexts, this class provides many adjustable parameters and extensibility hooks. However, programmers are urged to use the more convenient `https://developer.android.com/reference/kotlin/java/util/concurrent/Executors` factory methods java.util.concurrent.Executors#newCachedThreadPool (unbounded thread pool, with automatic thread reclamation), java.util.concurrent.Executors#newFixedThreadPool (fixed size thread pool) and java.util.concurrent.Executors#newSingleThreadExecutor (single background thread), that preconfigure settings for the most common usage scenarios. Otherwise, use the following guide when manually configuring and tuning this class:

Core and maximum pool sizes
: A `ThreadPoolExecutor` will automatically adjust the pool size (see `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#getPoolSize()`) according to the bounds set by corePoolSize (see `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#getCorePoolSize()`) and maximumPoolSize (see `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#getMaximumPoolSize()`). When a new task is submitted in method `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#execute(java.lang.Runnable)`, if fewer than corePoolSize threads are running, a new thread is created to handle the request, even if other worker threads are idle. Else if fewer than maximumPoolSize threads are running, a new thread will be created to handle the request only if the queue is full. By setting corePoolSize and maximumPoolSize the same, you create a fixed-size thread pool. By setting maximumPoolSize to an essentially unbounded value such as `Integer.MAX_VALUE`, you allow the pool to accommodate an arbitrary number of concurrent tasks. Most typically, core and maximum pool sizes are set only upon construction, but they may also be changed dynamically using `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#setCorePoolSize(kotlin.Int)` and `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#setMaximumPoolSize(kotlin.Int)`.

On-demand construction
: By default, even core threads are initially created and started only when new tasks arrive, but this can be overridden dynamically using method `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#prestartCoreThread()` or `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#prestartAllCoreThreads()`. You probably want to prestart threads if you construct the pool with a non-empty queue.

Creating new threads
: New threads are created using a `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadFactory`. If not otherwise specified, a `https://developer.android.com/reference/kotlin/java/util/concurrent/Executors#defaultThreadFactory()` is used, that creates threads to all be in the same `https://developer.android.com/reference/kotlin/java/lang/ThreadGroup.html#` and with the same `NORM_PRIORITY` priority and non-daemon status. By supplying a different ThreadFactory, you can alter the thread's name, thread group, priority, daemon status, etc. If a `ThreadFactory` fails to create a thread when asked by returning null from `newThread`, the executor will continue, but might not be able to execute any tasks.

Keep-alive times
: If the pool currently has more than corePoolSize threads, excess threads will be terminated if they have been idle for more than the keepAliveTime (see `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#getKeepAliveTime(java.util.concurrent.TimeUnit)`). This provides a means of reducing resource consumption when the pool is not being actively used. If the pool becomes more active later, new threads will be constructed. This parameter can also be changed dynamically using method `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#setKeepAliveTime(kotlin.Long,%20java.util.concurrent.TimeUnit)`. Using a value of `Long.MAX_VALUE` `https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit` effectively disables idle threads from ever terminating prior to shut down. By default, the keep-alive policy applies only when there are more than corePoolSize threads, but method `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#allowCoreThreadTimeOut(kotlin.Boolean)` can be used to apply this time-out policy to core threads as well, so long as the keepAliveTime value is non-zero.

Queuing
: Any `https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue` may be used to transfer and hold submitted tasks. The use of this queue interacts with pool sizing:

 - If fewer than corePoolSize threads are running, the Executor always prefers adding a new thread rather than queuing.
 - If corePoolSize or more threads are running, the Executor always prefers queuing a request rather than adding a new thread.
 - If a request cannot be queued, a new thread is created unless this would exceed maximumPoolSize, in which case, the task will be rejected.

 There are three general strategies for queuing:

 1. *Direct handoffs.* A good default choice for a work queue is a `https://developer.android.com/reference/kotlin/java/util/concurrent/SynchronousQueue` that hands off tasks to threads without otherwise holding them. Here, an attempt to queue a task will fail if no threads are immediately available to run it, so a new thread will be constructed. This policy avoids lockups when handling sets of requests that might have internal dependencies. Direct handoffs generally require unbounded maximumPoolSizes to avoid rejection of new submitted tasks. This in turn admits the possibility of unbounded thread growth when commands continue to arrive on average faster than they can be processed.
 2. *Unbounded queues.* Using an unbounded queue (for example a `https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingQueue` without a predefined capacity) will cause new tasks to wait in the queue when all corePoolSize threads are busy. Thus, no more than corePoolSize threads will ever be created. (And the value of the maximumPoolSize therefore doesn't have any effect.) This may be appropriate when each task is completely independent of others, so tasks cannot affect each others execution; for example, in a web page server. While this style of queuing can be useful in smoothing out transient bursts of requests, it admits the possibility of unbounded work queue growth when commands continue to arrive on average faster than they can be processed.
 3. *Bounded queues.* A bounded queue (for example, an `https://developer.android.com/reference/kotlin/java/util/concurrent/ArrayBlockingQueue`) helps prevent resource exhaustion when used with finite maximumPoolSizes, but can be more difficult to tune and control. Queue sizes and maximum pool sizes may be traded off for each other: Using large queues and small pools minimizes CPU usage, OS resources, and context-switching overhead, but can lead to artificially low throughput. If tasks frequently block (for example if they are I/O bound), a system may be able to schedule time for more threads than you otherwise allow. Use of small queues generally requires larger pool sizes, which keeps CPUs busier but may encounter unacceptable scheduling overhead, which also decreases throughput.

Rejected tasks
: New tasks submitted in method `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#execute(java.lang.Runnable)` will be *rejected* when the Executor has been shut down, and also when the Executor uses finite bounds for both maximum threads and work queue capacity, and is saturated. In either case, the `execute` method invokes the `https://developer.android.com/reference/kotlin/java/util/concurrent/RejectedExecutionHandler#rejectedExecution(java.lang.Runnable,%20java.util.concurrent.ThreadPoolExecutor)` method of its `https://developer.android.com/reference/kotlin/java/util/concurrent/RejectedExecutionHandler`. Four predefined handler policies are provided:

 1. In the default `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor.AbortPolicy`, the handler throws a runtime `https://developer.android.com/reference/kotlin/java/util/concurrent/RejectedExecutionException` upon rejection.
 2. In `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor.CallerRunsPolicy`, the thread that invokes `execute` itself runs the task. This provides a simple feedback control mechanism that will slow down the rate that new tasks are submitted.
 3. In `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor.DiscardPolicy`, a task that cannot be executed is simply dropped. This policy is designed only for those rare cases in which task completion is never relied upon.
 4. In `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor.DiscardOldestPolicy`, if the executor is not shut down, the task at the head of the work queue is dropped, and then execution is retried (which can fail again, causing this to be repeated.) This policy is rarely acceptable. In nearly all cases, you should also cancel the task to cause an exception in any component waiting for its completion, and/or log the failure, as illustrated in `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor.DiscardOldestPolicy` documentation.

 It is possible to define and use other kinds of `https://developer.android.com/reference/kotlin/java/util/concurrent/RejectedExecutionHandler` classes. Doing so requires some care especially when policies are designed to work only under particular capacity or queuing policies.

Hook methods
: This class provides `protected` overridable `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#beforeExecute(java.lang.Thread,%20java.lang.Runnable)` and `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#afterExecute(java.lang.Runnable,%20kotlin.Throwable)` methods that are called before and after execution of each task. These can be used to manipulate the execution environment; for example, reinitializing ThreadLocals, gathering statistics, or adding log entries. Additionally, method `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#terminated()` can be overridden to perform any special processing that needs to be done once the Executor has fully terminated.

 If hook, callback, or BlockingQueue methods throw exceptions, internal worker threads may in turn fail, abruptly terminate, and possibly be replaced.

Queue maintenance
: Method `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#getQueue()` allows access to the work queue for purposes of monitoring and debugging. Use of this method for any other purpose is strongly discouraged. Two supplied methods, `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#remove(java.lang.Runnable)` and `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#purge()` are available to assist in storage reclamation when large numbers of queued tasks become cancelled.

Reclamation
: A pool that is no longer referenced in a program *AND* has no remaining threads may be reclaimed (garbage collected) without being explicitly shutdown. You can configure a pool to allow all unused threads to eventually die by setting appropriate keep-alive times, using a lower bound of zero core threads and/or setting `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#allowCoreThreadTimeOut(kotlin.Boolean)`.

**Extension example.** Most extensions of this class override one or more of the protected hook methods. For example, here is a subclass that adds a simple pause/resume feature:

```kotlin
<code>class PausableThreadPoolExecutor extends ThreadPoolExecutor {
    private boolean isPaused;
    private ReentrantLock pauseLock = new ReentrantLock();
    private Condition unpaused = pauseLock.newCondition();
 
    public PausableThreadPoolExecutor(...) { super(...); }
 
    protected void beforeExecute(Thread t, Runnable r) {
      super.beforeExecute(t, r);
      pauseLock.lock();
      try {
        while (isPaused) unpaused.await();
      } catch (InterruptedException ie) {
        t.interrupt();
      } finally {
        pauseLock.unlock();
      }
    }
 
    public void pause() {
      pauseLock.lock();
      try {
        isPaused = true;
      } finally {
        pauseLock.unlock();
      }
    }
 
    public void resume() {
      pauseLock.lock();
      try {
        isPaused = false;
        unpaused.signalAll();
      } finally {
        pauseLock.unlock();
      }
    }
  }</code>
```

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor.AbortPolicy` A handler for rejected tasks that throws a `https://developer.android.com/reference/kotlin/java/util/concurrent/RejectedExecutionException`. |
| open | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor.CallerRunsPolicy` A handler for rejected tasks that runs the rejected task directly in the calling thread of the `execute` method, unless the executor has been shut down, in which case the task is discarded. |
| open | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor.DiscardOldestPolicy` A handler for rejected tasks that discards the oldest unhandled request and then retries `execute`, unless the executor is shut down, in which case the task is discarded. |
| --- | --- |
| open | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor.DiscardPolicy` A handler for rejected tasks that silently discards the rejected task. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#ThreadPoolExecutor(kotlin.Int,%20kotlin.Int,%20kotlin.Long,%20java.util.concurrent.TimeUnit,%20java.util.concurrent.BlockingQueue)(corePoolSize: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, maximumPoolSize: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, keepAliveTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, unit: https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit!, workQueue: https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue<https://developer.android.com/reference/kotlin/java/lang/Runnable.html#!>!)` Creates a new `ThreadPoolExecutor` with the given initial parameters, the [default thread factory](https://developer.android.com/reference/kotlin/java/util/concurrent/Executors#defaultThreadFactory()) and the [default rejected execution handler](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor.AbortPolicy). |
| `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#ThreadPoolExecutor(kotlin.Int,%20kotlin.Int,%20kotlin.Long,%20java.util.concurrent.TimeUnit,%20java.util.concurrent.BlockingQueue,%20java.util.concurrent.RejectedExecutionHandler)(corePoolSize: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, maximumPoolSize: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, keepAliveTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, unit: https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit!, workQueue: https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue<https://developer.android.com/reference/kotlin/java/lang/Runnable.html#!>!, handler: https://developer.android.com/reference/kotlin/java/util/concurrent/RejectedExecutionHandler!)` Creates a new `ThreadPoolExecutor` with the given initial parameters and the [default thread factory](https://developer.android.com/reference/kotlin/java/util/concurrent/Executors#defaultThreadFactory()). |
| `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#ThreadPoolExecutor(kotlin.Int,%20kotlin.Int,%20kotlin.Long,%20java.util.concurrent.TimeUnit,%20java.util.concurrent.BlockingQueue,%20java.util.concurrent.ThreadFactory)(corePoolSize: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, maximumPoolSize: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, keepAliveTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, unit: https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit!, workQueue: https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue<https://developer.android.com/reference/kotlin/java/lang/Runnable.html#!>!, threadFactory: https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadFactory!)` Creates a new `ThreadPoolExecutor` with the given initial parameters and the [default rejected execution handler](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor.AbortPolicy). |
| `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#ThreadPoolExecutor(kotlin.Int,%20kotlin.Int,%20kotlin.Long,%20java.util.concurrent.TimeUnit,%20java.util.concurrent.BlockingQueue,%20java.util.concurrent.ThreadFactory,%20java.util.concurrent.RejectedExecutionHandler)(corePoolSize: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, maximumPoolSize: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, keepAliveTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, unit: https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit!, workQueue: https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue<https://developer.android.com/reference/kotlin/java/lang/Runnable.html#!>!, threadFactory: https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadFactory!, handler: https://developer.android.com/reference/kotlin/java/util/concurrent/RejectedExecutionHandler!)` Creates a new `ThreadPoolExecutor` with the given initial parameters. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#allowCoreThreadTimeOut(kotlin.Boolean)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets the policy governing whether core threads may time out and terminate if no tasks arrive within the keep-alive time, being replaced if needed when new tasks arrive. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#allowsCoreThreadTimeOut()()` Returns true if this pool allows core threads to time out and terminate if no tasks arrive within the keepAlive time, being replaced if needed when new tasks arrive. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#awaitTermination(kotlin.Long,%20java.util.concurrent.TimeUnit)(timeout: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, unit: https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit!)` Blocks until all tasks have completed execution after a shutdown request, or the timeout occurs, or the current thread is interrupted, whichever happens first. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#execute(java.lang.Runnable)(command: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#!)` Executes the given task sometime in the future. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#getActiveCount()()` Returns the approximate number of threads that are actively executing tasks. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#getCompletedTaskCount()()` Returns the approximate total number of tasks that have completed execution. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#getCorePoolSize()()` Returns the core number of threads. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#getKeepAliveTime(java.util.concurrent.TimeUnit)(unit: https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit!)` Returns the thread keep-alive time, which is the amount of time that threads may remain idle before being terminated. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#getLargestPoolSize()()` Returns the largest number of threads that have ever simultaneously been in the pool. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#getMaximumPoolSize()()` Returns the maximum allowed number of threads. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#getPoolSize()()` Returns the current number of threads in the pool. |
| open [BlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue)\< [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!\>! | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#getQueue()()` Returns the task queue used by this executor. |
| --- | --- |
| open [RejectedExecutionHandler](https://developer.android.com/reference/kotlin/java/util/concurrent/RejectedExecutionHandler)! | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#getRejectedExecutionHandler()()` Returns the current handler for unexecutable tasks. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#getTaskCount()()` Returns the approximate total number of tasks that have ever been scheduled for execution. |
| open [ThreadFactory](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadFactory)! | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#getThreadFactory()()` Returns the thread factory used to create new threads. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#isShutdown()()` Returns `true` if this executor has been shut down. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#isTerminated()()` Returns `true` if all tasks have completed following shut down. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#isTerminating()()` Returns true if this executor is in the process of terminating after `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#shutdown()` or `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#shutdownNow()` but has not completely terminated. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#prestartAllCoreThreads()()` Starts all core threads, causing them to idly wait for work. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#prestartCoreThread()()` Starts a core thread, causing it to idly wait for work. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#purge()()` Tries to remove from the work queue all `https://developer.android.com/reference/kotlin/java/util/concurrent/Future` tasks that have been cancelled. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#remove(java.lang.Runnable)(task: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#!)` Removes this task from the executor's internal queue if it is present, thus causing it not to be run if it has not already started. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#setCorePoolSize(kotlin.Int)(corePoolSize: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the core number of threads. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#setKeepAliveTime(kotlin.Long,%20java.util.concurrent.TimeUnit)(time: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, unit: https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit!)` Sets the thread keep-alive time, which is the amount of time that threads may remain idle before being terminated. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#setMaximumPoolSize(kotlin.Int)(maximumPoolSize: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the maximum allowed number of threads. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#setRejectedExecutionHandler(java.util.concurrent.RejectedExecutionHandler)(handler: https://developer.android.com/reference/kotlin/java/util/concurrent/RejectedExecutionHandler!)` Sets a new handler for unexecutable tasks. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#setThreadFactory(java.util.concurrent.ThreadFactory)(threadFactory: https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadFactory!)` Sets the thread factory used to create new threads. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#shutdown()()` Initiates an orderly shutdown in which previously submitted tasks are executed, but no new tasks will be accepted. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!\>! | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#shutdownNow()()` Attempts to stop all actively executing tasks, halts the processing of waiting tasks, and returns a list of the tasks that were awaiting execution. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#toString()()` Returns a string identifying this pool, as well as its state, including indications of run state and estimated worker and task counts. |
| --- | --- |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#afterExecute(java.lang.Runnable,%20kotlin.Throwable)(r: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#!, t: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html!)` Method invoked upon completion of execution of the given Runnable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#beforeExecute(java.lang.Thread,%20java.lang.Runnable)(t: https://developer.android.com/reference/kotlin/java/lang/Thread.html#!, r: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#!)` Method invoked prior to executing the given Runnable in the given thread. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#finalize()()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#terminated()()` Method invoked when the Executor has terminated. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService#awaitTermination(kotlin.Long,%20java.util.concurrent.TimeUnit)(timeout: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, unit: https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit!)` Blocks until all tasks have completed execution after a shutdown request, or the timeout occurs, or the current thread is interrupted, whichever happens first. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService#close()()` Initiates an orderly shutdown in which previously submitted tasks are executed, but no new tasks will be accepted. This method waits until all tasks have completed execution and the executor has terminated. If interrupted while waiting, this method stops all executing tasks as if by invoking `https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService#shutdownNow()`. It then continues to wait until all actively executing tasks have completed. Tasks that were awaiting execution are not executed. The interrupt status will be re-asserted before this method returns. If already terminated, invoking this method has no effect. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService#isShutdown()()` Returns `true` if this executor has been shut down. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService#isTerminated()()` Returns `true` if all tasks have completed following shut down. Note that `isTerminated` is never `true` unless either `shutdown` or `shutdownNow` was called first. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService#shutdown()()` Initiates an orderly shutdown in which previously submitted tasks are executed, but no new tasks will be accepted. Invocation has no additional effect if already shut down. This method does not wait for previously submitted tasks to complete execution. Use `https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService#awaitTermination(kotlin.Long,%20java.util.concurrent.TimeUnit)` to do that. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/lang/Runnable.html#!>!` | `https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService#shutdownNow()()` Attempts to stop all actively executing tasks, halts the processing of waiting tasks, and returns a list of the tasks that were awaiting execution. This method does not wait for actively executing tasks to terminate. Use `https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService#awaitTermination(kotlin.Long,%20java.util.concurrent.TimeUnit)` to do that. There are no guarantees beyond best-effort attempts to stop processing actively executing tasks. For example, typical implementations will cancel via `https://developer.android.com/reference/kotlin/java/lang/Thread.html#interrupt()`, so any task that fails to respond to interrupts may never terminate. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor#execute(java.lang.Runnable)(command: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#!)` Executes the given command at some time in the future. The command may execute in a new thread, in a pooled thread, or in the calling thread, at the discretion of the `Executor` implementation. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/java/util/concurrent/AbstractExecutorService` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/util/concurrent/Future<T>!>!` | `https://developer.android.com/reference/kotlin/java/util/concurrent/AbstractExecutorService#invokeAll(kotlin.collections.MutableCollection)(tasks: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<out https://developer.android.com/reference/kotlin/java/util/concurrent/Callable<T>!>!)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/util/concurrent/Future<T>!>!` | `https://developer.android.com/reference/kotlin/java/util/concurrent/AbstractExecutorService#invokeAll(kotlin.collections.MutableCollection,%20kotlin.Long,%20java.util.concurrent.TimeUnit)(tasks: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<out https://developer.android.com/reference/kotlin/java/util/concurrent/Callable<T>!>!, timeout: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, unit: https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit!)` <br /> | | `T` | `https://developer.android.com/reference/kotlin/java/util/concurrent/AbstractExecutorService#invokeAny(kotlin.collections.MutableCollection)(tasks: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<out https://developer.android.com/reference/kotlin/java/util/concurrent/Callable<T>!>!)` <br /> | | `T` | `https://developer.android.com/reference/kotlin/java/util/concurrent/AbstractExecutorService#invokeAny(kotlin.collections.MutableCollection,%20kotlin.Long,%20java.util.concurrent.TimeUnit)(tasks: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<out https://developer.android.com/reference/kotlin/java/util/concurrent/Callable<T>!>!, timeout: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, unit: https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit!)` <br /> | | `https://developer.android.com/reference/kotlin/java/util/concurrent/RunnableFuture<T>!` | `https://developer.android.com/reference/kotlin/java/util/concurrent/AbstractExecutorService#newTaskFor(java.lang.Runnable,%20java.util.concurrent.AbstractExecutorService.newTaskFor.T)(runnable: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#!, value: T)` Returns a `RunnableFuture` for the given runnable and default value. <br /> | | `https://developer.android.com/reference/kotlin/java/util/concurrent/RunnableFuture<T>!` | `https://developer.android.com/reference/kotlin/java/util/concurrent/AbstractExecutorService#newTaskFor(java.util.concurrent.Callable)(callable: https://developer.android.com/reference/kotlin/java/util/concurrent/Callable<T>!)` Returns a `RunnableFuture` for the given callable task. <br /> | | `https://developer.android.com/reference/kotlin/java/util/concurrent/Future<*>!` | `https://developer.android.com/reference/kotlin/java/util/concurrent/AbstractExecutorService#submit(java.lang.Runnable)(task: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#!)` <br /> | | `https://developer.android.com/reference/kotlin/java/util/concurrent/Future<T>!` | `https://developer.android.com/reference/kotlin/java/util/concurrent/AbstractExecutorService#submit(java.lang.Runnable,%20java.util.concurrent.AbstractExecutorService.submit.T)(task: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#!, result: T)` <br /> | | `https://developer.android.com/reference/kotlin/java/util/concurrent/Future<T>!` | `https://developer.android.com/reference/kotlin/java/util/concurrent/AbstractExecutorService#submit(java.util.concurrent.Callable)(task: https://developer.android.com/reference/kotlin/java/util/concurrent/Callable<T>!)` <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

## Public constructors

### ThreadPoolExecutor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ThreadPoolExecutor(
    corePoolSize: Int, 
    maximumPoolSize: Int, 
    keepAliveTime: Long, 
    unit: TimeUnit!, 
    workQueue: BlockingQueue<Runnable!>!)
```

Creates a new `ThreadPoolExecutor` with the given initial parameters, the [default thread factory](https://developer.android.com/reference/kotlin/java/util/concurrent/Executors#defaultThreadFactory()) and the [default rejected execution handler](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor.AbortPolicy).

It may be more convenient to use one of the `https://developer.android.com/reference/kotlin/java/util/concurrent/Executors` factory methods instead of this general purpose constructor.

| Parameters ||
|---|---|
| `corePoolSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of threads to keep in the pool, even if they are idle, unless `allowCoreThreadTimeOut` is set |
| `maximumPoolSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the maximum number of threads to allow in the pool |
| `keepAliveTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): when the number of threads is greater than the core, this is the maximum time that excess idle threads will wait for new tasks before terminating. |
| --- | --- |
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!: the time unit for the `keepAliveTime` argument |
| `workQueue` | [BlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue)\< [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!\>!: the queue to use for holding tasks before they are executed. This queue will hold only the `Runnable` tasks submitted by the `execute` method. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if one of the following holds: `corePoolSize < 0` `keepAliveTime < 0` `maximumPoolSize <= 0` `maximumPoolSize < corePoolSize` |
| `java.lang.NullPointerException` | if `workQueue` is null |

### ThreadPoolExecutor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ThreadPoolExecutor(
    corePoolSize: Int, 
    maximumPoolSize: Int, 
    keepAliveTime: Long, 
    unit: TimeUnit!, 
    workQueue: BlockingQueue<Runnable!>!, 
    handler: RejectedExecutionHandler!)
```

Creates a new `ThreadPoolExecutor` with the given initial parameters and the [default thread factory](https://developer.android.com/reference/kotlin/java/util/concurrent/Executors#defaultThreadFactory()).

| Parameters ||
|---|---|
| `corePoolSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of threads to keep in the pool, even if they are idle, unless `allowCoreThreadTimeOut` is set |
| `maximumPoolSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the maximum number of threads to allow in the pool |
| `keepAliveTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): when the number of threads is greater than the core, this is the maximum time that excess idle threads will wait for new tasks before terminating. |
| --- | --- |
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!: the time unit for the `keepAliveTime` argument |
| `workQueue` | [BlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue)\< [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!\>!: the queue to use for holding tasks before they are executed. This queue will hold only the `Runnable` tasks submitted by the `execute` method. |
| `handler` | [RejectedExecutionHandler](https://developer.android.com/reference/kotlin/java/util/concurrent/RejectedExecutionHandler)!: the handler to use when execution is blocked because the thread bounds and queue capacities are reached |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if one of the following holds: `corePoolSize < 0` `keepAliveTime < 0` `maximumPoolSize <= 0` `maximumPoolSize < corePoolSize` |
| `java.lang.NullPointerException` | if `workQueue` or `handler` is null |

### ThreadPoolExecutor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ThreadPoolExecutor(
    corePoolSize: Int, 
    maximumPoolSize: Int, 
    keepAliveTime: Long, 
    unit: TimeUnit!, 
    workQueue: BlockingQueue<Runnable!>!, 
    threadFactory: ThreadFactory!)
```

Creates a new `ThreadPoolExecutor` with the given initial parameters and the [default rejected execution handler](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor.AbortPolicy).

| Parameters ||
|---|---|
| `corePoolSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of threads to keep in the pool, even if they are idle, unless `allowCoreThreadTimeOut` is set |
| `maximumPoolSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the maximum number of threads to allow in the pool |
| `keepAliveTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): when the number of threads is greater than the core, this is the maximum time that excess idle threads will wait for new tasks before terminating. |
| --- | --- |
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!: the time unit for the `keepAliveTime` argument |
| `workQueue` | [BlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue)\< [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!\>!: the queue to use for holding tasks before they are executed. This queue will hold only the `Runnable` tasks submitted by the `execute` method. |
| `threadFactory` | [ThreadFactory](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadFactory)!: the factory to use when the executor creates a new thread |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if one of the following holds: `corePoolSize < 0` `keepAliveTime < 0` `maximumPoolSize <= 0` `maximumPoolSize < corePoolSize` |
| `java.lang.NullPointerException` | if `workQueue` or `threadFactory` is null |

### ThreadPoolExecutor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ThreadPoolExecutor(
    corePoolSize: Int, 
    maximumPoolSize: Int, 
    keepAliveTime: Long, 
    unit: TimeUnit!, 
    workQueue: BlockingQueue<Runnable!>!, 
    threadFactory: ThreadFactory!, 
    handler: RejectedExecutionHandler!)
```

Creates a new `ThreadPoolExecutor` with the given initial parameters.

| Parameters ||
|---|---|
| `corePoolSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of threads to keep in the pool, even if they are idle, unless `allowCoreThreadTimeOut` is set |
| `maximumPoolSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the maximum number of threads to allow in the pool |
| `keepAliveTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): when the number of threads is greater than the core, this is the maximum time that excess idle threads will wait for new tasks before terminating. |
| --- | --- |
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!: the time unit for the `keepAliveTime` argument |
| `workQueue` | [BlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue)\< [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!\>!: the queue to use for holding tasks before they are executed. This queue will hold only the `Runnable` tasks submitted by the `execute` method. |
| `threadFactory` | [ThreadFactory](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadFactory)!: the factory to use when the executor creates a new thread |
| --- | --- |
| `handler` | [RejectedExecutionHandler](https://developer.android.com/reference/kotlin/java/util/concurrent/RejectedExecutionHandler)!: the handler to use when execution is blocked because the thread bounds and queue capacities are reached |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if one of the following holds: `corePoolSize < 0` `keepAliveTime < 0` `maximumPoolSize <= 0` `maximumPoolSize < corePoolSize` |
| `java.lang.NullPointerException` | if `workQueue` or `threadFactory` or `handler` is null |

## Public methods

### allowCoreThreadTimeOut

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun allowCoreThreadTimeOut(value: Boolean): Unit
```

Sets the policy governing whether core threads may time out and terminate if no tasks arrive within the keep-alive time, being replaced if needed when new tasks arrive. When false, core threads are never terminated due to lack of incoming tasks. When true, the same keep-alive policy applying to non-core threads applies also to core threads. To avoid continual thread replacement, the keep-alive time must be greater than zero when setting `true`. This method should in general be called before the pool is actively used.

| Parameters ||
|---|---|
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if should time out, else `false` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if value is `true` and the current keep-alive time is not greater than zero |

### allowsCoreThreadTimeOut

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun allowsCoreThreadTimeOut(): Boolean
```

Returns true if this pool allows core threads to time out and terminate if no tasks arrive within the keepAlive time, being replaced if needed when new tasks arrive. When true, the same keep-alive policy applying to non-core threads applies also to core threads. When false (the default), core threads are never terminated due to lack of incoming tasks.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if core threads are allowed to time out, else `false` |

### awaitTermination

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun awaitTermination(
    timeout: Long, 
    unit: TimeUnit!
): Boolean
```

Blocks until all tasks have completed execution after a shutdown request, or the timeout occurs, or the current thread is interrupted, whichever happens first.

| Parameters ||
|---|---|
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the maximum time to wait |
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!: the time unit of the timeout argument |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this executor terminated and `false` if the timeout elapsed before termination |

| Exceptions ||
|---|---|
| `java.lang.InterruptedException` | if interrupted while waiting |

### execute

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun execute(command: Runnable!): Unit
```

Executes the given task sometime in the future. The task may execute in a new thread or in an existing pooled thread. If the task cannot be submitted for execution, either because this executor has been shutdown or because its capacity has been reached, the task is handled by the current `https://developer.android.com/reference/kotlin/java/util/concurrent/RejectedExecutionHandler`.

| Parameters ||
|---|---|
| `command` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!: the task to execute |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `command` is null |
| `java.util.concurrent.RejectedExecutionException` | at discretion of `RejectedExecutionHandler`, if the task cannot be accepted for execution |

### getActiveCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getActiveCount(): Int
```

Returns the approximate number of threads that are actively executing tasks.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of threads |

### getCompletedTaskCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCompletedTaskCount(): Long
```

Returns the approximate total number of tasks that have completed execution. Because the states of tasks and threads may change dynamically during computation, the returned value is only an approximation, but one that does not ever decrease across successive calls.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the number of tasks |

### getCorePoolSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCorePoolSize(): Int
```

Returns the core number of threads.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the core number of threads |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#setCorePoolSize(kotlin.Int)`

### getKeepAliveTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getKeepAliveTime(unit: TimeUnit!): Long
```

Returns the thread keep-alive time, which is the amount of time that threads may remain idle before being terminated. Threads that wait this amount of time without processing a task will be terminated if there are more than the core number of threads currently in the pool, or if this pool [allows core thread timeout](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#allowsCoreThreadTimeOut()).

| Parameters ||
|---|---|
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!: the desired time unit of the result |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the time limit |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#setKeepAliveTime(kotlin.Long,%20java.util.concurrent.TimeUnit)`

### getLargestPoolSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLargestPoolSize(): Int
```

Returns the largest number of threads that have ever simultaneously been in the pool.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of threads |

### getMaximumPoolSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMaximumPoolSize(): Int
```

Returns the maximum allowed number of threads.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the maximum allowed number of threads |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#setMaximumPoolSize(kotlin.Int)`

### getPoolSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPoolSize(): Int
```

Returns the current number of threads in the pool.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of threads |

### getQueue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getQueue(): BlockingQueue<Runnable!>!
```

Returns the task queue used by this executor. Access to the task queue is intended primarily for debugging and monitoring. This queue may be in active use. Retrieving the task queue does not prevent queued tasks from executing.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue<https://developer.android.com/reference/kotlin/java/lang/Runnable.html#!>!` | the task queue |

### getRejectedExecutionHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRejectedExecutionHandler(): RejectedExecutionHandler!
```

Returns the current handler for unexecutable tasks.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/RejectedExecutionHandler!` | the current handler |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#setRejectedExecutionHandler(java.util.concurrent.RejectedExecutionHandler)`

### getTaskCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTaskCount(): Long
```

Returns the approximate total number of tasks that have ever been scheduled for execution. Because the states of tasks and threads may change dynamically during computation, the returned value is only an approximation.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the number of tasks |

### getThreadFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getThreadFactory(): ThreadFactory!
```

Returns the thread factory used to create new threads.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadFactory!` | the current thread factory |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#setThreadFactory(java.util.concurrent.ThreadFactory)`

### isShutdown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isShutdown(): Boolean
```

Returns `true` if this executor has been shut down.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this executor has been shut down |

### isTerminated

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isTerminated(): Boolean
```

Returns `true` if all tasks have completed following shut down. Note that `isTerminated` is never `true` unless either `shutdown` or `shutdownNow` was called first.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if all tasks have completed following shut down |

### isTerminating

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isTerminating(): Boolean
```

Returns true if this executor is in the process of terminating after `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#shutdown()` or `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#shutdownNow()` but has not completely terminated. This method may be useful for debugging. A return of `true` reported a sufficient period after shutdown may indicate that submitted tasks have ignored or suppressed interruption, causing this executor not to properly terminate.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if terminating but not yet terminated |

### prestartAllCoreThreads

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun prestartAllCoreThreads(): Int
```

Starts all core threads, causing them to idly wait for work. This overrides the default policy of starting core threads only when new tasks are executed.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of threads started |

### prestartCoreThread

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun prestartCoreThread(): Boolean
```

Starts a core thread, causing it to idly wait for work. This overrides the default policy of starting core threads only when new tasks are executed. This method will return `false` if all core threads have already been started.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if a thread was started |

### purge

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun purge(): Unit
```

Tries to remove from the work queue all `https://developer.android.com/reference/kotlin/java/util/concurrent/Future` tasks that have been cancelled. This method can be useful as a storage reclamation operation, that has no other impact on functionality. Cancelled tasks are never executed, but may accumulate in work queues until worker threads can actively remove them. Invoking this method instead tries to remove them now. However, this method may fail to remove tasks in the presence of interference by other threads.

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun remove(task: Runnable!): Boolean
```

Removes this task from the executor's internal queue if it is present, thus causing it not to be run if it has not already started.

This method may be useful as one part of a cancellation scheme. It may fail to remove tasks that have been converted into other forms before being placed on the internal queue. For example, a task entered using `submit` might be converted into a form that maintains `Future` status. However, in such cases, method `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#purge()` may be used to remove those Futures that have been cancelled.

| Parameters ||
|---|---|
| `task` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!: the task to remove |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the task was removed |

### setCorePoolSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setCorePoolSize(corePoolSize: Int): Unit
```

Sets the core number of threads. This overrides any value set in the constructor. If the new value is smaller than the current value, excess existing threads will be terminated when they next become idle. If larger, new threads will, if needed, be started to execute any queued tasks.

| Parameters ||
|---|---|
| `corePoolSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the new core size |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `corePoolSize < 0` |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#getCorePoolSize()`

### setKeepAliveTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setKeepAliveTime(
    time: Long, 
    unit: TimeUnit!
): Unit
```

Sets the thread keep-alive time, which is the amount of time that threads may remain idle before being terminated. Threads that wait this amount of time without processing a task will be terminated if there are more than the core number of threads currently in the pool, or if this pool [allows core thread timeout](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#allowsCoreThreadTimeOut()). This overrides any value set in the constructor.

| Parameters ||
|---|---|
| `time` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the time to wait. A time value of zero will cause excess threads to terminate immediately after executing tasks. |
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!: the time unit of the `time` argument |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `time` less than zero or if `time` is zero and `allowsCoreThreadTimeOut` |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#getKeepAliveTime(java.util.concurrent.TimeUnit)`

### setMaximumPoolSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMaximumPoolSize(maximumPoolSize: Int): Unit
```

Sets the maximum allowed number of threads. This overrides any value set in the constructor. If the new value is smaller than the current value, excess existing threads will be terminated when they next become idle.

| Parameters ||
|---|---|
| `maximumPoolSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the new maximum |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the new maximum is less than or equal to zero, or less than the [core pool size](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#getCorePoolSize()) |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#getMaximumPoolSize()`

### setRejectedExecutionHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setRejectedExecutionHandler(handler: RejectedExecutionHandler!): Unit
```

Sets a new handler for unexecutable tasks.

| Parameters ||
|---|---|
| `handler` | [RejectedExecutionHandler](https://developer.android.com/reference/kotlin/java/util/concurrent/RejectedExecutionHandler)!: the new handler |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if handler is null |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#getRejectedExecutionHandler()`

### setThreadFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setThreadFactory(threadFactory: ThreadFactory!): Unit
```

Sets the thread factory used to create new threads.

| Parameters ||
|---|---|
| `threadFactory` | [ThreadFactory](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadFactory)!: the new thread factory |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if threadFactory is null |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#getThreadFactory()`

### shutdown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun shutdown(): Unit
```

Initiates an orderly shutdown in which previously submitted tasks are executed, but no new tasks will be accepted. Invocation has no additional effect if already shut down.

This method does not wait for previously submitted tasks to complete execution. Use `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#awaitTermination(kotlin.Long,%20java.util.concurrent.TimeUnit)` to do that.

### shutdownNow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun shutdownNow(): MutableList<Runnable!>!
```

Attempts to stop all actively executing tasks, halts the processing of waiting tasks, and returns a list of the tasks that were awaiting execution. These tasks are drained (removed) from the task queue upon return from this method.

This method does not wait for actively executing tasks to terminate. Use `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#awaitTermination(kotlin.Long,%20java.util.concurrent.TimeUnit)` to do that.

There are no guarantees beyond best-effort attempts to stop processing actively executing tasks. This implementation interrupts tasks via `https://developer.android.com/reference/kotlin/java/lang/Thread.html#interrupt()`; any task that fails to respond to interrupts may never terminate.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/lang/Runnable.html#!>!` | list of tasks that never commenced execution |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string identifying this pool, as well as its state, including indications of run state and estimated worker and task counts.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string identifying this pool, as well as its state |

## Protected methods

### afterExecute

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun afterExecute(
    r: Runnable!, 
    t: Throwable!
): Unit
```

Method invoked upon completion of execution of the given Runnable. This method is invoked by the thread that executed the task. If non-null, the Throwable is the uncaught `RuntimeException` or `Error` that caused execution to terminate abruptly.

This implementation does nothing, but may be customized in subclasses. Note: To properly nest multiple overridings, subclasses should generally invoke `super.afterExecute` at the beginning of this method.

**Note:** When actions are enclosed in tasks (such as `https://developer.android.com/reference/kotlin/java/util/concurrent/FutureTask`) either explicitly or via methods such as `submit`, these task objects catch and maintain computational exceptions, and so they do not cause abrupt termination, and the internal exceptions are *not* passed to this method. If you would like to trap both kinds of failures in this method, you can further probe for such cases, as in this sample subclass that prints either the direct cause or the underlying exception if a task has been aborted:

```kotlin
<code>class ExtendedExecutor extends ThreadPoolExecutor {
    // ...
    protected void afterExecute(Runnable r, Throwable t) {
      super.afterExecute(r, t);
      if (t == null
          &amp;&amp; r instanceof Future&lt;?&gt;
          &amp;&amp; ((Future&lt;?&gt;)r).isDone()) {
        try {
          Object result = ((Future&lt;?&gt;) r).get();
        } catch (CancellationException ce) {
          t = ce;
        } catch (ExecutionException ee) {
          t = ee.getCause();
        } catch (InterruptedException ie) {
          // ignore/reset
          Thread.currentThread().interrupt();
        }
      }
      if (t != null)
        System.out.println(t);
    }
  }</code>
```

| Parameters ||
|---|---|
| `r` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!: the runnable that has completed |
| `t` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: the exception that caused termination, or null if execution completed normally |

### beforeExecute

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun beforeExecute(
    t: Thread!, 
    r: Runnable!
): Unit
```

Method invoked prior to executing the given Runnable in the given thread. This method is invoked by thread `t` that will execute task `r`, and may be used to re-initialize ThreadLocals, or to perform logging.

This implementation does nothing, but may be customized in subclasses. Note: To properly nest multiple overridings, subclasses should generally invoke `super.beforeExecute` at the end of this method.

| Parameters ||
|---|---|
| `t` | [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread.html#)!: the thread that will run task `r` |
| `r` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!: the task that will be executed |

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun finalize(): Unit
```

**Deprecated:** *Subclass is not recommended to override finalize(). If it must, please always invoke super.finalize().*

| Exceptions ||
|---|---|
| `java.lang.Throwable` | the `Exception` raised by this method |

### terminated

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun terminated(): Unit
```

Method invoked when the Executor has terminated. Default implementation does nothing. Note: To properly nest multiple overridings, subclasses should generally invoke `super.terminated` within this method.
