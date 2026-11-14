# ForkJoinPool

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ForkJoinPool

```
open class ForkJoinPool : AbstractExecutorService
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.concurrent.AbstractExecutorService](https://developer.android.com/reference/kotlin/java/util/concurrent/AbstractExecutorService) ||
| | ↳ | [java.util.concurrent.ForkJoinPool](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#) |

An [ExecutorService](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService) for running [ForkJoinTask](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask) s. A`ForkJoinPool`provides the entry point for submissions from non-`ForkJoinTask`clients, as well as management and monitoring operations.

A`ForkJoinPool`differs from other kinds of [ExecutorService](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService) mainly by virtue of employing*work-stealing* : all threads in the pool attempt to find and execute tasks submitted to the pool and/or created by other active tasks (eventually blocking waiting for work if none exist). This enables efficient processing when most tasks spawn other subtasks (as do most`ForkJoinTask`s), as well as when many small tasks are submitted to the pool from external clients. Especially when setting*asyncMode* to true in constructors,`ForkJoinPool`s may also be appropriate for use with event-style tasks that are never joined. All worker threads are initialized with [Thread.isDaemon](https://developer.android.com/reference/kotlin/java/lang/Thread.html#isDaemon())set`true`.

A static [commonPool()](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#commonPool())is available and appropriate for most applications. The common pool is used by any ForkJoinTask that is not explicitly submitted to a specified pool. Using the common pool normally reduces resource usage (its threads are slowly reclaimed during periods of non-use, and reinstated upon subsequent use).

For applications that require separate or custom pools, a`ForkJoinPool`may be constructed with a given target parallelism level; by default, equal to the number of available processors. The pool attempts to maintain enough active (or available) threads by dynamically adding, suspending, or resuming internal worker threads, even if some tasks are stalled waiting to join others. However, no such adjustments are guaranteed in the face of blocked I/O or other unmanaged synchronization. The nested [ManagedBlocker](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool.ManagedBlocker) interface enables extension of the kinds of synchronization accommodated. The default policies may be overridden using a constructor with parameters corresponding to those documented in class [ThreadPoolExecutor](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor).

In addition to execution and lifecycle control methods, this class provides status check methods (for example [getStealCount](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#getStealCount())) that are intended to aid in developing, tuning, and monitoring fork/join applications. Also, method [toString](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#toString())returns indications of pool state in a convenient form for informal monitoring.

As is the case with other ExecutorServices, there are three main task execution methods summarized in the following table. These are designed to be used primarily by clients not already engaged in fork/join computations in the current pool. The main forms of these methods accept instances of`ForkJoinTask`, but overloaded forms also allow mixed execution of plain`Runnable`- or`Callable`- based activities as well. However, tasks that are already executing in a pool should normally instead use the within-computation forms listed in the table unless using async event-style tasks that are not usually joined, in which case there is little difference among choice of methods.

| | Call from non-fork/join clients | Call from within fork/join computations |
| --- | --- | --- |

The parameters used to construct the common pool may be controlled by setting the following java.lang.System#getProperty:

- `java.util.concurrent.ForkJoinPool.common.parallelism`- the parallelism level, a non-negative integer
- `java.util.concurrent.ForkJoinPool.common.threadFactory`- the class name of a [ForkJoinWorkerThreadFactory](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool.ForkJoinWorkerThreadFactory). The [system class loader](https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#getSystemClassLoader())is used to load this class.
- `java.util.concurrent.ForkJoinPool.common.exceptionHandler`- the class name of a [UncaughtExceptionHandler](https://developer.android.com/reference/kotlin/java/lang/Thread.UncaughtExceptionHandler.html#). The [system class loader](https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#getSystemClassLoader())is used to load this class.
- `java.util.concurrent.ForkJoinPool.common.maximumSpares`- the maximum number of allowed extra threads to maintain target parallelism (default 256).

If no thread factory is supplied via a system property, then the common pool uses a factory that uses the system class loader as the [thread context class loader](https://developer.android.com/reference/kotlin/java/lang/Thread.html#getContextClassLoader()). In addition, if a [SecurityManager](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#) is present, then the common pool uses a factory supplying threads that have no [Permissions](https://developer.android.com/reference/kotlin/java/security/Permissions.html#) enabled, and are not guaranteed to preserve the values of [java.lang.ThreadLocal](https://developer.android.com/reference/kotlin/java/lang/ThreadLocal.html#) variables across tasks. Upon any error in establishing these settings, default parameters are used. It is possible to disable or limit the use of threads in the common pool by setting the parallelism property to zero, and/or using a factory that may return`null`. However doing so may cause unjoined tasks to never be executed.

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [ForkJoinWorkerThreadFactory](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool.ForkJoinWorkerThreadFactory) Factory for creating new [ForkJoinWorkerThread](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinWorkerThread) s. |
| abstract | [ManagedBlocker](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool.ManagedBlocker) Interface for extending managed parallelism for tasks running in [ForkJoinPool](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#) s. |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ForkJoinPool](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#ForkJoinPool())`()` Creates a`ForkJoinPool`with parallelism equal to [java.lang.Runtime#availableProcessors](https://developer.android.com/reference/kotlin/java/lang/Runtime.html#availableProcessors()), using defaults for all other parameters (see [ForkJoinPool(int,java.util.concurrent.ForkJoinPool.ForkJoinWorkerThreadFactory,java.lang.Thread.UncaughtExceptionHandler,boolean,int,int,int,java.util.function.Predicate,long,java.util.concurrent.TimeUnit)](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#ForkJoinPool(kotlin.Int,%20java.util.concurrent.ForkJoinPool.ForkJoinWorkerThreadFactory,%20java.lang.Thread.UncaughtExceptionHandler,%20kotlin.Boolean,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20java.util.function.Predicate,%20kotlin.Long,%20java.util.concurrent.TimeUnit))). |
| [ForkJoinPool](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#ForkJoinPool(kotlin.Int))`(`parallelism:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a`ForkJoinPool`with the indicated parallelism level, using defaults for all other parameters (see [ForkJoinPool(int,java.util.concurrent.ForkJoinPool.ForkJoinWorkerThreadFactory,java.lang.Thread.UncaughtExceptionHandler,boolean,int,int,int,java.util.function.Predicate,long,java.util.concurrent.TimeUnit)](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#ForkJoinPool(kotlin.Int,%20java.util.concurrent.ForkJoinPool.ForkJoinWorkerThreadFactory,%20java.lang.Thread.UncaughtExceptionHandler,%20kotlin.Boolean,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20java.util.function.Predicate,%20kotlin.Long,%20java.util.concurrent.TimeUnit))). |
| [ForkJoinPool](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#ForkJoinPool(kotlin.Int,%20java.util.concurrent.ForkJoinPool.ForkJoinWorkerThreadFactory,%20java.lang.Thread.UncaughtExceptionHandler,%20kotlin.Boolean))`(`parallelism:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `factory:` ` [ForkJoinPool.ForkJoinWorkerThreadFactory](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool.ForkJoinWorkerThreadFactory)!`, `handler:` ` [Thread.UncaughtExceptionHandler](https://developer.android.com/reference/kotlin/java/lang/Thread.UncaughtExceptionHandler.html#)!`, `asyncMode:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a`ForkJoinPool`with the given parameters (using defaults for others -- see [ForkJoinPool(int,java.util.concurrent.ForkJoinPool.ForkJoinWorkerThreadFactory,java.lang.Thread.UncaughtExceptionHandler,boolean,int,int,int,java.util.function.Predicate,long,java.util.concurrent.TimeUnit)](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#ForkJoinPool(kotlin.Int,%20java.util.concurrent.ForkJoinPool.ForkJoinWorkerThreadFactory,%20java.lang.Thread.UncaughtExceptionHandler,%20kotlin.Boolean,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20java.util.function.Predicate,%20kotlin.Long,%20java.util.concurrent.TimeUnit))). |
| [ForkJoinPool](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#ForkJoinPool(kotlin.Int,%20java.util.concurrent.ForkJoinPool.ForkJoinWorkerThreadFactory,%20java.lang.Thread.UncaughtExceptionHandler,%20kotlin.Boolean,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20java.util.function.Predicate,%20kotlin.Long,%20java.util.concurrent.TimeUnit))`(`parallelism:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `factory:` ` [ForkJoinPool.ForkJoinWorkerThreadFactory](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool.ForkJoinWorkerThreadFactory)!`, `handler:` ` [Thread.UncaughtExceptionHandler](https://developer.android.com/reference/kotlin/java/lang/Thread.UncaughtExceptionHandler.html#)!`, `asyncMode:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `corePoolSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `maximumPoolSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `minimumRunnable:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `saturate:` ` [Predicate](https://developer.android.com/reference/kotlin/java/util/function/Predicate.html#)<in` ` [ForkJoinPool](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#)!>!`, `keepAliveTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` Creates a`ForkJoinPool`with the given parameters. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [awaitQuiescence](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#awaitQuiescence(kotlin.Long,%20java.util.concurrent.TimeUnit))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` If called by a ForkJoinTask operating in this pool, equivalent in effect to [ForkJoinTask.helpQuiesce](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#helpQuiesce()). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [awaitTermination](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#awaitTermination(kotlin.Long,%20java.util.concurrent.TimeUnit))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` Blocks until all tasks have completed execution after a shutdown request, or the timeout occurs, or the current thread is interrupted, whichever happens first. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#close())`()` Unless this is the [commonPool()](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#commonPool()), initiates an orderly shutdown in which previously submitted tasks are executed, but no new tasks will be accepted, and waits until all tasks have completed execution and the executor has terminated. |
| --- | --- |
| openstatic [ForkJoinPool](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#)! | [commonPool](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#commonPool())`()` Returns the common pool instance. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [execute](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#execute(java.lang.Runnable))`(`task:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [execute](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#execute(java.util.concurrent.ForkJoinTask))`(`task:` ` [ForkJoinTask](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask)<*>!`)` Arranges for (asynchronous) execution of the given task. |
| --- | --- |
| open [ForkJoinTask](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask)\<T\>! | [externalSubmit](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#externalSubmit(java.util.concurrent.ForkJoinTask))`(`task:` ` [ForkJoinTask](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask)<T>!`)` Submits the given task as if submitted from a non-`ForkJoinTask`client. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getActiveThreadCount](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#getActiveThreadCount())`()` Returns an estimate of the number of threads that are currently stealing or executing tasks. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getAsyncMode](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#getAsyncMode())`()` Returns`true`if this pool uses local first-in-first-out scheduling mode for forked tasks that are never joined. |
| --- | --- |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCommonPoolParallelism](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#getCommonPoolParallelism())`()` Returns the targeted parallelism level of the common pool. |
| open [ForkJoinPool.ForkJoinWorkerThreadFactory](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool.ForkJoinWorkerThreadFactory)! | [getFactory](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#getFactory())`()` Returns the factory used for constructing new workers. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getParallelism](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#getParallelism())`()` Returns the targeted parallelism level of this pool. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPoolSize](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#getPoolSize())`()` Returns the number of worker threads that have started but not yet terminated. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getQueuedSubmissionCount](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#getQueuedSubmissionCount())`()` Returns an estimate of the number of tasks submitted to this pool that have not yet begun executing. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getQueuedTaskCount](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#getQueuedTaskCount())`()` Returns an estimate of the total number of tasks currently held in queues by worker threads (but not including tasks submitted to the pool that have not begun executing). |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRunningThreadCount](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#getRunningThreadCount())`()` Returns an estimate of the number of worker threads that are not blocked waiting to join tasks or for other managed synchronization. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getStealCount](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#getStealCount())`()` Returns an estimate of the total number of completed tasks that were executed by a thread other than their submitter. |
| open [Thread.UncaughtExceptionHandler](https://developer.android.com/reference/kotlin/java/lang/Thread.UncaughtExceptionHandler.html#)! | [getUncaughtExceptionHandler](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#getUncaughtExceptionHandler())`()` Returns the handler for internal worker threads that terminate due to unrecoverable errors encountered while executing tasks. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasQueuedSubmissions](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#hasQueuedSubmissions())`()` Returns`true`if there are any tasks submitted to this pool that have not yet begun executing. |
| openT | [invoke](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#invoke(java.util.concurrent.ForkJoinTask))`(`task:` ` [ForkJoinTask](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask)<T>!`)` Performs the given task, returning its result upon completion. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)\<T\>!\>! | [invokeAll](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#invokeAll(kotlin.collections.MutableCollection))`(`tasks:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` ` [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable)<T>!>!`)` <br /> |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)\<T\>!\>! | [invokeAll](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#invokeAll(kotlin.collections.MutableCollection,%20kotlin.Long,%20java.util.concurrent.TimeUnit))`(`tasks:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` ` [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable)<T>!>!`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` <br /> |
| openT | [invokeAny](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#invokeAny(kotlin.collections.MutableCollection))`(`tasks:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` ` [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable)<T>!>!`)` <br /> |
| openT | [invokeAny](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#invokeAny(kotlin.collections.MutableCollection,%20kotlin.Long,%20java.util.concurrent.TimeUnit))`(`tasks:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` ` [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable)<T>!>!`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isQuiescent](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#isQuiescent())`()` Returns`true`if all worker threads are currently idle. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isShutdown](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#isShutdown())`()` Returns`true`if this pool has been shut down. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTerminated](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#isTerminated())`()` Returns`true`if all tasks have completed following shut down. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTerminating](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#isTerminating())`()` Returns`true`if the process of termination has commenced but not yet completed. |
| open [ForkJoinTask](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask)\<T\>! | [lazySubmit](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#lazySubmit(java.util.concurrent.ForkJoinTask))`(`task:` ` [ForkJoinTask](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask)<T>!`)` Submits the given task without guaranteeing that it will eventually execute in the absence of available active threads. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [managedBlock](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#managedBlock(java.util.concurrent.ForkJoinPool.ManagedBlocker))`(`blocker:` ` [ForkJoinPool.ManagedBlocker](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool.ManagedBlocker)!`)` Runs the given possibly blocking task. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [setParallelism](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#setParallelism(kotlin.Int))`(`size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Changes the target parallelism of this pool, controlling the future creation, use, and termination of worker threads. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [shutdown](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#shutdown())`()` Possibly initiates an orderly shutdown in which previously submitted tasks are executed, but no new tasks will be accepted. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!\>! | [shutdownNow](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#shutdownNow())`()` Possibly attempts to cancel and/or stop all tasks, and reject all subsequently submitted tasks. |
| --- | --- |
| open [ForkJoinTask](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask)\<\*\>! | [submit](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#submit(java.lang.Runnable))`(`task:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`)` <br /> |
| open [ForkJoinTask](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask)\<T\>! | [submit](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#submit(java.lang.Runnable,%20java.util.concurrent.ForkJoinPool.submit.T))`(`task:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`, `result:` `T`)` <br /> |
| open [ForkJoinTask](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask)\<T\>! | [submit](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#submit(java.util.concurrent.Callable))`(`task:` ` [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable)<T>!`)` <br /> |
| --- | --- |
| open [ForkJoinTask](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask)\<T\>! | [submit](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#submit(java.util.concurrent.ForkJoinTask))`(`task:` ` [ForkJoinTask](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask)<T>!`)` Submits a ForkJoinTask for execution. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#toString())`()` Returns a string identifying this pool, as well as its state, including indications of run state, parallelism level, and worker and task counts. |

| Protected methods ||
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [drainTasksTo](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#drainTasksTo(kotlin.collections.MutableCollection))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<in` ` [ForkJoinTask](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask)<*>!>!`)` Removes all available unexecuted submitted and forked tasks from scheduling queues and adds them to the given collection, without altering their execution status. |
| open [RunnableFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/RunnableFuture)\<T\>! | [newTaskFor](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#newTaskFor(java.lang.Runnable,%20java.util.concurrent.ForkJoinPool.newTaskFor.T))`(`runnable:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`, `value:` `T`)` <br /> |
| open [RunnableFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/RunnableFuture)\<T\>! | [newTaskFor](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#newTaskFor(java.util.concurrent.Callable))`(`callable:` ` [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable)<T>!`)` <br /> |
| --- | --- |
| open [ForkJoinTask](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask)\<\*\>! | [pollSubmission](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#pollSubmission())`()` Removes and returns the next unexecuted submission if one is available. |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [ForkJoinPool.ForkJoinWorkerThreadFactory](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool.ForkJoinWorkerThreadFactory)! | [defaultForkJoinWorkerThreadFactory](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#defaultForkJoinWorkerThreadFactory:java.util.concurrent.ForkJoinPool.ForkJoinWorkerThreadFactory) Creates a new ForkJoinWorkerThread. |

## Public constructors

### ForkJoinPool

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ForkJoinPool()
```

Creates a`ForkJoinPool`with parallelism equal to [java.lang.Runtime#availableProcessors](https://developer.android.com/reference/kotlin/java/lang/Runtime.html#availableProcessors()), using defaults for all other parameters (see [ForkJoinPool(int,java.util.concurrent.ForkJoinPool.ForkJoinWorkerThreadFactory,java.lang.Thread.UncaughtExceptionHandler,boolean,int,int,int,java.util.function.Predicate,long,java.util.concurrent.TimeUnit)](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#ForkJoinPool(kotlin.Int,%20java.util.concurrent.ForkJoinPool.ForkJoinWorkerThreadFactory,%20java.lang.Thread.UncaughtExceptionHandler,%20kotlin.Boolean,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20java.util.function.Predicate,%20kotlin.Long,%20java.util.concurrent.TimeUnit))).

| Exceptions ||
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and the caller is not permitted to modify threads because it does not hold`("modifyThread")` |

### ForkJoinPool

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ForkJoinPool(parallelism: Int)
```

Creates a`ForkJoinPool`with the indicated parallelism level, using defaults for all other parameters (see [ForkJoinPool(int,java.util.concurrent.ForkJoinPool.ForkJoinWorkerThreadFactory,java.lang.Thread.UncaughtExceptionHandler,boolean,int,int,int,java.util.function.Predicate,long,java.util.concurrent.TimeUnit)](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#ForkJoinPool(kotlin.Int,%20java.util.concurrent.ForkJoinPool.ForkJoinWorkerThreadFactory,%20java.lang.Thread.UncaughtExceptionHandler,%20kotlin.Boolean,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20java.util.function.Predicate,%20kotlin.Long,%20java.util.concurrent.TimeUnit))).

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------|
| `parallelism` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the parallelism level |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if parallelism less than or equal to zero, or greater than implementation limit |
| `java.lang.SecurityException` | if a security manager exists and the caller is not permitted to modify threads because it does not hold`("modifyThread")` |

### ForkJoinPool

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ForkJoinPool(
    parallelism: Int, 
    factory: ForkJoinPool.ForkJoinWorkerThreadFactory!, 
    handler: Thread.UncaughtExceptionHandler!, 
    asyncMode: Boolean)
```

Creates a`ForkJoinPool`with the given parameters (using defaults for others -- see [ForkJoinPool(int,java.util.concurrent.ForkJoinPool.ForkJoinWorkerThreadFactory,java.lang.Thread.UncaughtExceptionHandler,boolean,int,int,int,java.util.function.Predicate,long,java.util.concurrent.TimeUnit)](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#ForkJoinPool(kotlin.Int,%20java.util.concurrent.ForkJoinPool.ForkJoinWorkerThreadFactory,%20java.lang.Thread.UncaughtExceptionHandler,%20kotlin.Boolean,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20java.util.function.Predicate,%20kotlin.Long,%20java.util.concurrent.TimeUnit))).

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parallelism` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the parallelism level. For default value, use [java.lang.Runtime#availableProcessors](https://developer.android.com/reference/kotlin/java/lang/Runtime.html#availableProcessors()). |
| `factory` | [ForkJoinPool.ForkJoinWorkerThreadFactory](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool.ForkJoinWorkerThreadFactory)!:the factory for creating new threads. For default value, use [defaultForkJoinWorkerThreadFactory](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#defaultForkJoinWorkerThreadFactory:java.util.concurrent.ForkJoinPool.ForkJoinWorkerThreadFactory). |
| `handler` | [Thread.UncaughtExceptionHandler](https://developer.android.com/reference/kotlin/java/lang/Thread.UncaughtExceptionHandler.html#)!:the handler for internal worker threads that terminate due to unrecoverable errors encountered while executing tasks. For default value, use`null`. |
| --- | --- |
| `asyncMode` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if true, establishes local first-in-first-out scheduling mode for forked tasks that are never joined. This mode may be more appropriate than default locally stack-based mode in applications in which worker threads only process event-style asynchronous tasks. For default value, use`false`. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if parallelism less than or equal to zero, or greater than implementation limit |
| `java.lang.NullPointerException` | if the factory is null |
| `java.lang.SecurityException` | if a security manager exists and the caller is not permitted to modify threads because it does not hold`("modifyThread")` |
| --- | --- |

### ForkJoinPool

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ForkJoinPool(
    parallelism: Int, 
    factory: ForkJoinPool.ForkJoinWorkerThreadFactory!, 
    handler: Thread.UncaughtExceptionHandler!, 
    asyncMode: Boolean, 
    corePoolSize: Int, 
    maximumPoolSize: Int, 
    minimumRunnable: Int, 
    saturate: Predicate<in ForkJoinPool!>!, 
    keepAliveTime: Long, 
    unit: TimeUnit!)
```

Creates a`ForkJoinPool`with the given parameters.

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parallelism` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the parallelism level. For default value, use [java.lang.Runtime#availableProcessors](https://developer.android.com/reference/kotlin/java/lang/Runtime.html#availableProcessors()). |
| `factory` | [ForkJoinPool.ForkJoinWorkerThreadFactory](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool.ForkJoinWorkerThreadFactory)!:the factory for creating new threads. For default value, use [defaultForkJoinWorkerThreadFactory](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#defaultForkJoinWorkerThreadFactory:java.util.concurrent.ForkJoinPool.ForkJoinWorkerThreadFactory). |
| `handler` | [Thread.UncaughtExceptionHandler](https://developer.android.com/reference/kotlin/java/lang/Thread.UncaughtExceptionHandler.html#)!:the handler for internal worker threads that terminate due to unrecoverable errors encountered while executing tasks. For default value, use`null`. |
| --- | --- |
| `asyncMode` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if true, establishes local first-in-first-out scheduling mode for forked tasks that are never joined. This mode may be more appropriate than default locally stack-based mode in applications in which worker threads only process event-style asynchronous tasks. For default value, use`false`. |
| `corePoolSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of threads to keep in the pool (unless timed out after an elapsed keep-alive). Normally (and by default) this is the same value as the parallelism level, but may be set to a larger value to reduce dynamic overhead if tasks regularly block. Using a smaller value (for example`0`) has the same effect as the default. |
| `maximumPoolSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum number of threads allowed. When the maximum is reached, attempts to replace blocked threads fail. (However, because creation and termination of different threads may overlap, and may be managed by the given thread factory, this value may be transiently exceeded.) To arrange the same value as is used by default for the common pool, use`256`plus the`parallelism`level. (By default, the common pool allows a maximum of 256 spare threads.) Using a value (for example`Integer.MAX_VALUE`) larger than the implementation's total thread limit has the same effect as using this limit (which is the default). |
| --- | --- |
| `minimumRunnable` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the minimum allowed number of core threads not blocked by a join or [ManagedBlocker](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool.ManagedBlocker). To ensure progress, when too few unblocked threads exist and unexecuted tasks may exist, new threads are constructed, up to the given maximumPoolSize. For the default value, use`1`, that ensures liveness. A larger value might improve throughput in the presence of blocked activities, but might not, due to increased overhead. A value of zero may be acceptable when submitted tasks cannot have dependencies requiring additional threads. |
| `saturate` | [Predicate](https://developer.android.com/reference/kotlin/java/util/function/Predicate.html#)\<in [ForkJoinPool](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#)!\>!:if non-null, a predicate invoked upon attempts to create more than the maximum total allowed threads. By default, when a thread is about to block on a join or [ManagedBlocker](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool.ManagedBlocker), but cannot be replaced because the maximumPoolSize would be exceeded, a [RejectedExecutionException](https://developer.android.com/reference/kotlin/java/util/concurrent/RejectedExecutionException) is thrown. But if this predicate returns`true`, then no exception is thrown, so the pool continues to operate with fewer than the target number of runnable threads, which might not ensure progress. |
| `keepAliveTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the elapsed time since last use before a thread is terminated (and then later replaced if needed). For the default value, use`60, TimeUnit.SECONDS`. |
| --- | --- |
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!:the time unit for the`keepAliveTime`argument |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if parallelism is less than or equal to zero, or is greater than implementation limit, or if maximumPoolSize is less than parallelism, of if the keepAliveTime is less than or equal to zero. |
| `java.lang.NullPointerException` | if the factory is null |
| `java.lang.SecurityException` | if a security manager exists and the caller is not permitted to modify threads because it does not hold`("modifyThread")` |
| --- | --- |

## Public methods

### awaitQuiescence

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun awaitQuiescence(
    timeout: Long, 
    unit: TimeUnit!
): Boolean
```

If called by a ForkJoinTask operating in this pool, equivalent in effect to [ForkJoinTask.helpQuiesce](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#helpQuiesce()). Otherwise, waits and/or attempts to assist performing tasks until this pool [isQuiescent](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#isQuiescent())or the indicated timeout elapses.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the maximum time to wait |
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!:the time unit of the timeout argument |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if quiescent;`false`if the timeout elapsed. |

### awaitTermination

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun awaitTermination(
    timeout: Long, 
    unit: TimeUnit!
): Boolean
```

Blocks until all tasks have completed execution after a shutdown request, or the timeout occurs, or the current thread is interrupted, whichever happens first. Because the [commonPool()](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#commonPool())never terminates until program shutdown, when applied to the common pool, this method is equivalent to [awaitQuiescence(long,java.util.concurrent.TimeUnit)](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#awaitQuiescence(kotlin.Long,%20java.util.concurrent.TimeUnit))but always returns`false`.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the maximum time to wait |
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!:the time unit of the timeout argument |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this executor terminated and`false`if the timeout elapsed before termination |

| Exceptions ||
|----------------------------------|------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |

### close

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Unless this is the [commonPool()](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#commonPool()), initiates an orderly shutdown in which previously submitted tasks are executed, but no new tasks will be accepted, and waits until all tasks have completed execution and the executor has terminated.

If already terminated, or this is the [commonPool()](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#commonPool()), this method has no effect on execution, and does not wait. Otherwise, if interrupted while waiting, this method stops all executing tasks as if by invoking [shutdownNow()](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#shutdownNow()). It then continues to wait until all actively executing tasks have completed. Tasks that were awaiting execution are not executed. The interrupt status will be re-asserted before this method returns.

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.lang.SecurityException` | if a security manager exists and shutting down this ExecutorService may manipulate threads that the caller is not permitted to modify because it does not hold`("modifyThread")`, or the security manager's`checkAccess`method denies access. |

### commonPool

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun commonPool(): ForkJoinPool!
```

Returns the common pool instance. This pool is statically constructed; its run state is unaffected by attempts to [shutdown](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#shutdown())or [shutdownNow](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#shutdownNow()). However this pool and any ongoing processing are automatically terminated upon program [System.exit](https://developer.android.com/reference/kotlin/java/lang/System.html#exit(kotlin.Int)). Any program that relies on asynchronous task processing to complete before program termination should invoke`commonPool().` [awaitQuiescence](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#awaitQuiescence(kotlin.Long,%20java.util.concurrent.TimeUnit)), before exit.

| Return ||
|----------------------------------------------------------------------------------------------------|--------------------------|
| [ForkJoinPool](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#)! | the common pool instance |

### execute

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun execute(task: Runnable!): Unit
```

| Parameters ||
|-----------|-------------------|
| `command` | the runnable task |

| Exceptions ||
|---------------------------------------------------|-----------------------------------------------|
| `java.util.concurrent.RejectedExecutionException` | if the task cannot be scheduled for execution |
| `java.lang.NullPointerException` | if the task is null |

### execute

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun execute(task: ForkJoinTask<*>!): Unit
```

Arranges for (asynchronous) execution of the given task.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------|
| `task` | [ForkJoinTask](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask)\<\*\>!:the task |

| Exceptions ||
|---------------------------------------------------|-----------------------------------------------|
| `java.lang.NullPointerException` | if the task is null |
| `java.util.concurrent.RejectedExecutionException` | if the task cannot be scheduled for execution |

### externalSubmit

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Any!> externalSubmit(task: ForkJoinTask<T>!): ForkJoinTask<T>!
```

Submits the given task as if submitted from a non-`ForkJoinTask`client. The task is added to a scheduling queue for submissions to the pool even when called from a thread in the pool.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------|
| `task` | [ForkJoinTask](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask)\<T\>!:the task to submit |
| `<T>` | the type of the task's result |

| Return ||
|------------------------------------------------------------------------------------------------------|----------|
| [ForkJoinTask](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask)<T>! | the task |

| Exceptions ||
|---------------------------------------------------|-----------------------------------------------|
| `java.lang.NullPointerException` | if the task is null |
| `java.util.concurrent.RejectedExecutionException` | if the task cannot be scheduled for execution |

### getActiveThreadCount

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getActiveThreadCount(): Int
```

Returns an estimate of the number of threads that are currently stealing or executing tasks. This method may overestimate the number of active threads.

| Return ||
|----------------------------------------------------------------------------|------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of active threads |

### getAsyncMode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAsyncMode(): Boolean
```

Returns`true`if this pool uses local first-in-first-out scheduling mode for forked tasks that are never joined.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this pool uses async mode |

### getCommonPoolParallelism

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getCommonPoolParallelism(): Int
```

Returns the targeted parallelism level of the common pool.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the targeted parallelism level of the common pool |

### getFactory

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFactory(): ForkJoinPool.ForkJoinWorkerThreadFactory!
```

Returns the factory used for constructing new workers.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [ForkJoinPool.ForkJoinWorkerThreadFactory](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool.ForkJoinWorkerThreadFactory)! | the factory used for constructing new workers |

### getParallelism

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParallelism(): Int
```

Returns the targeted parallelism level of this pool.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the targeted parallelism level of this pool |

### getPoolSize

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPoolSize(): Int
```

Returns the number of worker threads that have started but not yet terminated. The result returned by this method may differ from [getParallelism](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#getParallelism())when threads are created to maintain parallelism when others are cooperatively blocked.

| Return ||
|----------------------------------------------------------------------------|------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of worker threads |

### getQueuedSubmissionCount

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getQueuedSubmissionCount(): Int
```

Returns an estimate of the number of tasks submitted to this pool that have not yet begun executing. This method may take time proportional to the number of submissions.

| Return ||
|----------------------------------------------------------------------------|----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of queued submissions |

### getQueuedTaskCount

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getQueuedTaskCount(): Long
```

Returns an estimate of the total number of tasks currently held in queues by worker threads (but not including tasks submitted to the pool that have not begun executing). This value is only an approximation, obtained by iterating across all threads in the pool. This method may be useful for tuning task granularities.

| Return ||
|------------------------------------------------------------------------------|----------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the number of queued tasks |

**See Also**

- [java.util.concurrent.ForkJoinWorkerThread#getQueuedTaskCount()](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinWorkerThread#getQueuedTaskCount()) 

### getRunningThreadCount

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRunningThreadCount(): Int
```

Returns an estimate of the number of worker threads that are not blocked waiting to join tasks or for other managed synchronization. This method may overestimate the number of running threads.

| Return ||
|----------------------------------------------------------------------------|------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of worker threads |

### getStealCount

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStealCount(): Long
```

Returns an estimate of the total number of completed tasks that were executed by a thread other than their submitter. The reported value underestimates the actual total number of steals when the pool is not quiescent. This value may be useful for monitoring and tuning fork/join programs: in general, steal counts should be high enough to keep threads busy, but low enough to avoid overhead and contention across threads.

| Return ||
|------------------------------------------------------------------------------|----------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the number of steals |

### getUncaughtExceptionHandler

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUncaughtExceptionHandler(): Thread.UncaughtExceptionHandler!
```

Returns the handler for internal worker threads that terminate due to unrecoverable errors encountered while executing tasks.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| [Thread.UncaughtExceptionHandler](https://developer.android.com/reference/kotlin/java/lang/Thread.UncaughtExceptionHandler.html#)! | the handler, or`null`if none |

### hasQueuedSubmissions

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasQueuedSubmissions(): Boolean
```

Returns`true`if there are any tasks submitted to this pool that have not yet begun executing.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if there are any queued submissions |

### invoke

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Any!> invoke(task: ForkJoinTask<T>!): T
```

Performs the given task, returning its result upon completion. If the computation encounters an unchecked Exception or Error, it is rethrown as the outcome of this invocation. Rethrown exceptions behave in the same way as regular exceptions, but, when possible, contain stack traces (as displayed for example using`ex.printStackTrace()`) of both the current thread as well as the thread actually encountering the exception; minimally only the latter.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------|
| `task` | [ForkJoinTask](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask)\<T\>!:the task |
| `<T>` | the type of the task's result |

| Return ||
|---|-------------------|
| T | the task's result |

| Exceptions ||
|---------------------------------------------------|-----------------------------------------------|
| `java.lang.NullPointerException` | if the task is null |
| `java.util.concurrent.RejectedExecutionException` | if the task cannot be scheduled for execution |

### invokeAll

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Any!> invokeAll(tasks: MutableCollection<out Callable<T>!>!): MutableList<Future<T>!>!
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tasks` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<out [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable)\<T\>!\>!:the collection of tasks |
| `<T>` | the type of the values returned from the tasks |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)<T>!>! | a list of Futures representing the tasks, in the same sequential order as produced by the iterator for the given task list, each of which has completed |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting, in which case unfinished tasks are cancelled |
| `java.lang.NullPointerException` | if tasks or any of its elements are`null` |
| `java.util.concurrent.RejectedExecutionException` | if any task cannot be scheduled for execution |
| --- | --- |

### invokeAll

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Any!> invokeAll(
    tasks: MutableCollection<out Callable<T>!>!, 
    timeout: Long, 
    unit: TimeUnit!
): MutableList<Future<T>!>!
```

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tasks` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<out [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable)\<T\>!\>!:the collection of tasks |
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the maximum time to wait |
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!:the time unit of the timeout argument |
| --- | --- |
| `<T>` | the type of the values returned from the tasks |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)<T>!>! | a list of Futures representing the tasks, in the same sequential order as produced by the iterator for the given task list. If the operation did not time out, each task will have completed. If it did time out, some of these tasks will not have completed. |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting, in which case unfinished tasks are cancelled |
| `java.lang.NullPointerException` | if tasks, any of its elements, or unit are`null` |
| `java.util.concurrent.RejectedExecutionException` | if any task cannot be scheduled for execution |
| --- | --- |

### invokeAny

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Any!> invokeAny(tasks: MutableCollection<out Callable<T>!>!): T
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tasks` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<out [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable)\<T\>!\>!:the collection of tasks |
| `<T>` | the type of the values returned from the tasks |

| Return ||
|---|-----------------------------------------|
| T | the result returned by one of the tasks |

| Exceptions ||
|---------------------------------------------------|------------------------------------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |
| `java.lang.NullPointerException` | if tasks or any element task subject to execution is`null` |
| `java.lang.IllegalArgumentException` | if tasks is empty |
| --- | --- |
| `java.util.concurrent.ExecutionException` | if no task successfully completes |
| `java.util.concurrent.RejectedExecutionException` | if tasks cannot be scheduled for execution |

### invokeAny

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Any!> invokeAny(
    tasks: MutableCollection<out Callable<T>!>!, 
    timeout: Long, 
    unit: TimeUnit!
): T
```

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tasks` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<out [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable)\<T\>!\>!:the collection of tasks |
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the maximum time to wait |
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!:the time unit of the timeout argument |
| --- | --- |
| `<T>` | the type of the values returned from the tasks |

| Return ||
|---|-----------------------------------------|
| T | the result returned by one of the tasks |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |
| `java.lang.NullPointerException` | if tasks, or unit, or any element task subject to execution is`null` |
| `java.util.concurrent.TimeoutException` | if the given timeout elapses before any task successfully completes |
| --- | --- |
| `java.util.concurrent.ExecutionException` | if no task successfully completes |
| `java.util.concurrent.RejectedExecutionException` | if tasks cannot be scheduled for execution |

### isQuiescent

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isQuiescent(): Boolean
```

Returns`true`if all worker threads are currently idle. An idle worker is one that cannot obtain a task to execute because none are available to steal from other threads, and there are no pending submissions to the pool. This method is conservative; it might not return`true`immediately upon idleness of all threads, but will eventually become true if threads remain inactive.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if all threads are currently idle |

### isShutdown

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isShutdown(): Boolean
```

Returns`true`if this pool has been shut down.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this pool has been shut down |

### isTerminated

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isTerminated(): Boolean
```

Returns`true`if all tasks have completed following shut down.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if all tasks have completed following shut down |

### isTerminating

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isTerminating(): Boolean
```

Returns`true`if the process of termination has commenced but not yet completed. This method may be useful for debugging. A return of`true`reported a sufficient period after shutdown may indicate that submitted tasks have ignored or suppressed interruption, or are waiting for I/O, causing this executor not to properly terminate. (See the advisory notes for class [ForkJoinTask](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask) stating that tasks should not normally entail blocking operations. But if they do, they must abort them on interrupt.)

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if terminating but not yet terminated |

### lazySubmit

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Any!> lazySubmit(task: ForkJoinTask<T>!): ForkJoinTask<T>!
```

Submits the given task without guaranteeing that it will eventually execute in the absence of available active threads. In some contexts, this method may reduce contention and overhead by relying on context-specific knowledge that existing threads (possibly including the calling thread if operating in this pool) will eventually be available to execute the task.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------|
| `task` | [ForkJoinTask](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask)\<T\>!:the task |
| `<T>` | the type of the task's result |

| Return ||
|------------------------------------------------------------------------------------------------------|----------|
| [ForkJoinTask](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask)<T>! | the task |

| Exceptions ||
|---------------------------------------------------|-----------------------------------------------|
| `java.lang.NullPointerException` | if the task is null |
| `java.util.concurrent.RejectedExecutionException` | if the task cannot be scheduled for execution |

### managedBlock

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun managedBlock(blocker: ForkJoinPool.ManagedBlocker!): Unit
```

Runs the given possibly blocking task. When [running in a ForkJoinPool](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#inForkJoinPool()), this method possibly arranges for a spare thread to be activated if necessary to ensure sufficient parallelism while the current thread is blocked in [blocker.block()](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool.ManagedBlocker#block()).

This method repeatedly calls`blocker.isReleasable()`and`blocker.block()`until either method returns`true`. Every call to`blocker.block()`is preceded by a call to`blocker.isReleasable()`that returned`false`.

If not running in a ForkJoinPool, this method is behaviorally equivalent to 

```kotlin
<code>while (!blocker.isReleasable())
    if (blocker.block())
      break;</code>
```
If running in a ForkJoinPool, the pool may first be expanded to ensure sufficient parallelism available during the call to`blocker.block()`.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `blocker` | [ForkJoinPool.ManagedBlocker](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool.ManagedBlocker)!:the blocker task |

| Exceptions ||
|----------------------------------|---------------------------|
| `java.lang.InterruptedException` | if`blocker.block()`did so |

### setParallelism

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setParallelism(size: Int): Int
```

Changes the target parallelism of this pool, controlling the future creation, use, and termination of worker threads. Applications include contexts in which the number of available processors changes over time.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------|
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the target parallelism level |

| Return ||
|----------------------------------------------------------------------------|---------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the previous parallelism level. |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if size is less than 1 or greater than the maximum supported by this pool. |
| `java.lang.UnsupportedOperationException` | this is the [commonPool()](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#commonPool())and parallelism level was set by System property {@systemProperty \* java.util.concurrent.ForkJoinPool.common.parallelism}. |
| `java.lang.SecurityException` | if a security manager exists and the caller is not permitted to modify threads because it does not hold`("modifyThread")` |
| --- | --- |

### shutdown

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun shutdown(): Unit
```

Possibly initiates an orderly shutdown in which previously submitted tasks are executed, but no new tasks will be accepted. Invocation has no effect on execution state if this is the [commonPool()](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#commonPool()), and no additional effect if already shut down. Tasks that are in the process of being submitted concurrently during the course of this method may or may not be rejected.

| Exceptions ||
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and the caller is not permitted to modify threads because it does not hold`("modifyThread")` |

### shutdownNow

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun shutdownNow(): MutableList<Runnable!>!
```

Possibly attempts to cancel and/or stop all tasks, and reject all subsequently submitted tasks. Invocation has no effect on execution state if this is the [commonPool()](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#commonPool()), and no additional effect if already shut down. Otherwise, tasks that are in the process of being submitted or executed concurrently during the course of this method may or may not be rejected. This method cancels both existing and unexecuted tasks, in order to permit termination in the presence of task dependencies. So the method always returns an empty list (unlike the case for some other Executors).

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!>! | an empty list |

| Exceptions ||
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and the caller is not permitted to modify threads because it does not hold`("modifyThread")` |

### submit

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun submit(task: Runnable!): ForkJoinTask<*>!
```

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------|
| `task` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!:the task to submit |

| Return ||
|------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| [ForkJoinTask](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask)<*>! | a Future representing pending completion of the task |

| Exceptions ||
|---------------------------------------------------|-----------------------------------------------|
| `java.util.concurrent.RejectedExecutionException` | if the task cannot be scheduled for execution |
| `java.lang.NullPointerException` | if the task is null |

### submit

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Any!> submit(
    task: Runnable!, 
    result: T
): ForkJoinTask<T>!
```

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------|
| `task` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!:the task to submit |
| `result` | T:the result to return |
| `<T>` | the type of the result |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| [ForkJoinTask](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask)<T>! | a Future representing pending completion of the task |

| Exceptions ||
|---------------------------------------------------|-----------------------------------------------|
| `java.util.concurrent.RejectedExecutionException` | if the task cannot be scheduled for execution |
| `java.lang.NullPointerException` | if the task is null |

### submit

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Any!> submit(task: Callable<T>!): ForkJoinTask<T>!
```

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------|
| `task` | [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable)\<T\>!:the task to submit |
| `<T>` | the type of the task's result |

| Return ||
|------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| [ForkJoinTask](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask)<T>! | a Future representing pending completion of the task |

| Exceptions ||
|---------------------------------------------------|-----------------------------------------------|
| `java.util.concurrent.RejectedExecutionException` | if the task cannot be scheduled for execution |
| `java.lang.NullPointerException` | if the task is null |

### submit

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Any!> submit(task: ForkJoinTask<T>!): ForkJoinTask<T>!
```

Submits a ForkJoinTask for execution.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------|
| `task` | [ForkJoinTask](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask)\<T\>!:the task to submit |
| `<T>` | the type of the task's result |

| Return ||
|------------------------------------------------------------------------------------------------------|----------|
| [ForkJoinTask](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask)<T>! | the task |

| Exceptions ||
|---------------------------------------------------|-----------------------------------------------|
| `java.lang.NullPointerException` | if the task is null |
| `java.util.concurrent.RejectedExecutionException` | if the task cannot be scheduled for execution |

### toString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string identifying this pool, as well as its state, including indications of run state, parallelism level, and worker and task counts.

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string identifying this pool, as well as its state |

## Protected methods

### drainTasksTo

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun drainTasksTo(c: MutableCollection<in ForkJoinTask<*>!>!): Int
```

Removes all available unexecuted submitted and forked tasks from scheduling queues and adds them to the given collection, without altering their execution status. These may include artificially generated or wrapped tasks. This method is designed to be invoked only when the pool is known to be quiescent. Invocations at other times may not remove all tasks. A failure encountered while attempting to add elements to collection`c`may result in elements being in neither, either or both collections when the associated exception is thrown. The behavior of this operation is undefined if the specified collection is modified while the operation is in progress.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<in [ForkJoinTask](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask)\<\*\>!\>!:the collection to transfer elements into |

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of elements transferred |

### newTaskFor

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun <T : Any!> newTaskFor(
    runnable: Runnable!, 
    value: T
): RunnableFuture<T>!
```

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------|
| `runnable` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!:the runnable task being wrapped |
| `value` | T:the default value for the returned future |
| `<T>` | the type of the given value |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [RunnableFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/RunnableFuture)<T>! | a`RunnableFuture`which, when run, will run the underlying runnable and which, as a`Future`, will yield the given value as its result and provide for cancellation of the underlying task |

### newTaskFor

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun <T : Any!> newTaskFor(callable: Callable<T>!): RunnableFuture<T>!
```

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------|
| `callable` | [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable)\<T\>!:the callable task being wrapped |
| `<T>` | the type of the callable's result |

| Return ||
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [RunnableFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/RunnableFuture)<T>! | a`RunnableFuture`which, when run, will call the underlying callable and which, as a`Future`, will yield the callable's result as its result and provide for cancellation of the underlying task |

### pollSubmission

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun pollSubmission(): ForkJoinTask<*>!
```

Removes and returns the next unexecuted submission if one is available. This method may be useful in extensions to this class that re-assign work in systems with multiple pools.

| Return ||
|------------------------------------------------------------------------------------------------------|--------------------------------------|
| [ForkJoinTask](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask)<*>! | the next submission, or`null`if none |

## Properties

### defaultForkJoinWorkerThreadFactory

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val defaultForkJoinWorkerThreadFactory: ForkJoinPool.ForkJoinWorkerThreadFactory!
```

Creates a new ForkJoinWorkerThread. This factory is used unless overridden in ForkJoinPool constructors.
