Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ForkJoinTask

```
abstract class ForkJoinTask<V : Any!> : Future<V>, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.concurrent.ForkJoinTask](ForkJoinTask.md) |

| Known Direct Subclasses [CountedCompleter](CountedCompleter.md), [RecursiveAction](RecursiveAction.md), [RecursiveTask](RecursiveTask.md) |---|---| | [CountedCompleter](CountedCompleter.md) | A `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#` with a completion action performed when triggered and there are no remaining pending actions. | | [RecursiveAction](RecursiveAction.md) | A recursive resultless `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#`. | | [RecursiveTask](RecursiveTask.md) | A recursive result-bearing `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#`. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Abstract base class for tasks that run within a `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool`. A `ForkJoinTask` is a thread-like entity that is much lighter weight than a normal thread. Huge numbers of tasks and subtasks may be hosted by a small number of actual threads in a ForkJoinPool, at the price of some usage limitations.

A "main" `ForkJoinTask` begins execution when it is explicitly submitted to a `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool`, or, if not already engaged in a ForkJoin computation, commenced in the `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#commonPool()` via `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#fork()`, `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#invoke()`, or related methods. Once started, it will usually in turn start other subtasks. As indicated by the name of this class, many programs using `ForkJoinTask` employ only methods `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#fork()` and `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#join()`, or derivatives such as `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#invokeAll(java.util.concurrent.ForkJoinTask)`. However, this class also provides a number of other methods that can come into play in advanced usages, as well as extension mechanics that allow support of new forms of fork/join processing.

A `ForkJoinTask` is a lightweight form of `https://developer.android.com/reference/kotlin/java/util/concurrent/Future`. The efficiency of `ForkJoinTask`s stems from a set of restrictions (that are only partially statically enforceable) reflecting their main use as computational tasks calculating pure functions or operating on purely isolated objects. The primary coordination mechanisms are `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#fork()`, that arranges asynchronous execution, and `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#join()`, that doesn't proceed until the task's result has been computed. Computations should ideally avoid `synchronized` methods or blocks, and should minimize other blocking synchronization apart from joining other tasks or using synchronizers such as Phasers that are advertised to cooperate with fork/join scheduling. Subdividable tasks should also not perform blocking I/O, and should ideally access variables that are completely independent of those accessed by other running tasks. These guidelines are loosely enforced by not permitting checked exceptions such as `IOExceptions` to be thrown. However, computations may still encounter unchecked exceptions, that are rethrown to callers attempting to join them. These exceptions may additionally include `https://developer.android.com/reference/kotlin/java/util/concurrent/RejectedExecutionException` stemming from internal resource exhaustion, such as failure to allocate internal task queues. Rethrown exceptions behave in the same way as regular exceptions, but, when possible, contain stack traces (as displayed for example using `ex.printStackTrace()`) of both the thread that initiated the computation as well as the thread actually encountering the exception; minimally only the latter.

It is possible to define and use ForkJoinTasks that may block, but doing so requires three further considerations: (1) Completion of few if any *other* tasks should be dependent on a task that blocks on external synchronization or I/O. Event-style async tasks that are never joined (for example, those subclassing `https://developer.android.com/reference/kotlin/java/util/concurrent/CountedCompleter`) often fall into this category. (2) To minimize resource impact, tasks should be small; ideally performing only the (possibly) blocking action. (3) Unless the `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool.ManagedBlocker` API is used, or the number of possibly blocked tasks is known to be less than the pool's `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#getParallelism()` level, the pool cannot guarantee that enough threads will be available to ensure progress or good performance.

The primary method for awaiting completion and extracting results of a task is `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#join()`, but there are several variants: The java.util.concurrent.Future#get methods support interruptible and/or timed waits for completion and report results using `Future` conventions. Method `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#invoke()` is semantically equivalent to `fork(); join()` but always attempts to begin execution in the current thread. The "*quiet* " forms of these methods do not extract results or report exceptions. These may be useful when a set of tasks are being executed, and you need to delay processing of results or exceptions until all complete. Method `invokeAll` (available in multiple versions) performs the most common form of parallel invocation: forking a set of tasks and joining them all.

In the most typical usages, a fork-join pair act like a call (fork) and return (join) from a parallel recursive function. As is the case with other forms of recursive calls, returns (joins) should be performed innermost-first. For example, `a.fork(); b.fork(); b.join(); a.join();` is likely to be substantially more efficient than joining `a` before `b`.

The execution status of tasks may be queried at several levels of detail: `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#isDone()` is true if a task completed in any way (including the case where a task was cancelled without executing); `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#isCompletedNormally()` is true if a task completed without cancellation or encountering an exception; `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#isCancelled()` is true if the task was cancelled (in which case `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#getException()` returns a `https://developer.android.com/reference/kotlin/java/util/concurrent/CancellationException`); and `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#isCompletedAbnormally()` is true if a task was either cancelled or encountered an exception, in which case `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#getException()` will return either the encountered exception or `https://developer.android.com/reference/kotlin/java/util/concurrent/CancellationException`.

The ForkJoinTask class is not usually directly subclassed. Instead, you subclass one of the abstract classes that support a particular style of fork/join processing, typically `https://developer.android.com/reference/kotlin/java/util/concurrent/RecursiveAction` for most computations that do not return results, `https://developer.android.com/reference/kotlin/java/util/concurrent/RecursiveTask` for those that do, and `https://developer.android.com/reference/kotlin/java/util/concurrent/CountedCompleter` for those in which completed actions trigger other actions. Normally, a concrete ForkJoinTask subclass declares fields comprising its parameters, established in a constructor, and then defines a `compute` method that somehow uses the control methods supplied by this base class.

Method `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#join()` and its variants are appropriate for use only when completion dependencies are acyclic; that is, the parallel computation can be described as a directed acyclic graph (DAG). Otherwise, executions may encounter a form of deadlock as tasks cyclically wait for each other. However, this framework supports other methods and techniques (for example the use of `https://developer.android.com/reference/kotlin/java/util/concurrent/Phaser`, `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#helpQuiesce()`, and `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#complete(java.util.concurrent.ForkJoinTask.V)`) that may be of use in constructing custom subclasses for problems that are not statically structured as DAGs. To support such usages, a ForkJoinTask may be atomically *tagged* with a `short` value using `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#setForkJoinTaskTag(kotlin.Short)` or `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#compareAndSetForkJoinTaskTag(kotlin.Short,%20kotlin.Short)` and checked using `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#getForkJoinTaskTag()`. The ForkJoinTask implementation does not use these `protected` methods or tags for any purpose, but they may be of use in the construction of specialized subclasses. For example, parallel graph traversals can use the supplied methods to avoid revisiting nodes/tasks that have already been processed. (Method names for tagging are bulky in part to encourage definition of methods that reflect their usage patterns.)

Most base support methods are `final`, to prevent overriding of implementations that are intrinsically tied to the underlying lightweight task scheduling framework. Developers creating new basic styles of fork/join processing should minimally implement `protected` methods `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#exec()`, `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#setRawResult(java.util.concurrent.ForkJoinTask.V)`, and `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#getRawResult()`, while also introducing an abstract computational method that can be implemented in its subclasses, possibly relying on other `protected` methods provided by this class.

ForkJoinTasks should perform relatively small amounts of computation. Large tasks should be split into smaller subtasks, usually via recursive decomposition. As a very rough rule of thumb, a task should perform more than 100 and less than 10000 basic computational steps, and should avoid indefinite looping. If tasks are too big, then parallelism cannot improve throughput. If too small, then memory and internal task maintenance overhead may overwhelm processing.

This class provides `adapt` methods for `https://developer.android.com/reference/kotlin/java/lang/Runnable.html#` and `https://developer.android.com/reference/kotlin/java/util/concurrent/Callable`, that may be of use when mixing execution of `ForkJoinTasks` with other kinds of tasks. When all tasks are of this form, consider using a pool constructed in *asyncMode*.

ForkJoinTasks are `Serializable`, which enables them to be used in extensions such as remote execution frameworks. It is sensible to serialize tasks only before or after, but not during, execution. Serialization is not relied on during execution itself.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#ForkJoinTask()()` Constructor for subclasses to call. |

| Public methods ||
|---|---|
| open static [ForkJoinTask](ForkJoinTask.md)\<\*\>! | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#adapt(java.lang.Runnable)(runnable: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#!)` Returns a new `ForkJoinTask` that performs the `run` method of the given `Runnable` as its action, and returns a null result upon `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#join()`. |
| open static [ForkJoinTask](ForkJoinTask.md)\<T\>! | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#adapt(java.lang.Runnable,%20java.util.concurrent.ForkJoinTask.adapt.T)(runnable: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#!, result: T)` Returns a new `ForkJoinTask` that performs the `run` method of the given `Runnable` as its action, and returns the given result upon `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#join()`. |
| open static [ForkJoinTask](ForkJoinTask.md)\<T\>! | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#adapt(java.util.concurrent.Callable)(callable: https://developer.android.com/reference/kotlin/java/util/concurrent/Callable<out T>!)` Returns a new `ForkJoinTask` that performs the `call` method of the given `Callable` as its action, and returns its result upon `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#join()`, translating any checked exceptions encountered into `RuntimeException`. |
| --- | --- |
| open static [ForkJoinTask](ForkJoinTask.md)\<T\>! | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#adaptInterruptible(java.util.concurrent.Callable)(callable: https://developer.android.com/reference/kotlin/java/util/concurrent/Callable<out T>!)` Returns a new `ForkJoinTask` that performs the `call` method of the given `Callable` as its action, and returns its result upon `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#join()`, translating any checked exceptions encountered into `RuntimeException`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#cancel(kotlin.Boolean)(mayInterruptIfRunning: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Attempts to cancel execution of this task. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#compareAndSetForkJoinTaskTag(kotlin.Short,%20kotlin.Short)(expect: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html, update: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Atomically conditionally sets the tag value for this task. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#complete(java.util.concurrent.ForkJoinTask.V)(value: V)` Completes this task, and if not already aborted or cancelled, returning the given value as the result of subsequent invocations of `join` and related operations. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#completeExceptionally(kotlin.Throwable)(ex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html!)` Completes this task abnormally, and if not already aborted or cancelled, causes it to throw the given exception upon `join` and related operations. |
| open [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)! | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#exceptionNow()()` Returns the exception thrown by the task, without waiting. |
| --- | --- |
| [ForkJoinTask](ForkJoinTask.md)\<V\>! | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#fork()()` Arranges to asynchronously execute this task in the pool the current task is running in, if applicable, or using the `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#commonPool()` if not `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#inForkJoinPool()`. |
| V | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#get()()` Waits if necessary for the computation to complete, and then retrieves its result. |
| V | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#get(kotlin.Long,%20java.util.concurrent.TimeUnit)(timeout: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, unit: https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit!)` Waits if necessary for at most the given time for the computation to complete, and then retrieves its result, if available. |
| --- | --- |
| [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)! | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#getException()()` Returns the exception thrown by the base computation, or a `CancellationException` if cancelled, or `null` if none or if the method has not yet completed. |
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#getForkJoinTaskTag()()` Returns the tag for this task. |
| open static [ForkJoinPool](ForkJoinPool.md)! | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#getPool()()` Returns the pool hosting the current thread, or `null` if the current thread is executing outside of any ForkJoinPool. |
| --- | --- |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#getQueuedTaskCount()()` Returns an estimate of the number of tasks that have been forked by the current worker thread but not yet executed. |
| abstract V | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#getRawResult()()` Returns the result that would be returned by `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#join()`, even if this task completed abnormally, or `null` if this task is not known to have been completed. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#getSurplusQueuedTaskCount()()` Returns an estimate of how many more locally queued tasks are held by the current worker thread than there are other worker threads that might steal them, or zero if this thread is not operating in a ForkJoinPool. |
| --- | --- |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#helpQuiesce()()` Possibly executes tasks until the pool hosting the current task [is quiescent](ForkJoinPool.md)). |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#inForkJoinPool()()` Returns `true` if the current thread is a `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinWorkerThread` executing as a ForkJoinPool computation. |
| V | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#invoke()()` Commences performing this task, awaits its completion if necessary, and returns its result, or throws an (unchecked) `RuntimeException` or `Error` if the underlying computation did so. |
| --- | --- |
| open static [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<T\>! | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#invokeAll(kotlin.collections.MutableCollection)(tasks: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<T>!)` Forks all tasks in the specified collection, returning when `isDone` holds for each task or an (unchecked) exception is encountered, in which case the exception is rethrown. |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#invokeAll(java.util.concurrent.ForkJoinTask,%20java.util.concurrent.ForkJoinTask)(t1: https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#<*>!, t2: https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#<*>!)` Forks the given tasks, returning when `isDone` holds for each task or an (unchecked) exception is encountered, in which case the exception is rethrown. |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#invokeAll(java.util.concurrent.ForkJoinTask)(vararg tasks: https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#<*>!)` Forks the given tasks, returning when `isDone` holds for each task or an (unchecked) exception is encountered, in which case the exception is rethrown. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#isCancelled()()` Returns `true` if this task was cancelled before it completed normally. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#isCompletedAbnormally()()` Returns `true` if this task threw an exception or was cancelled. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#isCompletedNormally()()` Returns `true` if this task completed without throwing an exception and was not cancelled. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#isDone()()` Returns `true` if this task completed. |
| V | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#join()()` Returns the result of the computation when it [is done](ForkJoinTask.md)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#quietlyComplete()()` Completes this task normally without setting a value. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#quietlyInvoke()()` Commences performing this task and awaits its completion if necessary, without returning its result or throwing its exception. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#quietlyJoin()()` Joins this task, without returning its result or throwing its exception. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#quietlyJoin(kotlin.Long,%20java.util.concurrent.TimeUnit)(timeout: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, unit: https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit!)` Tries to join this task, returning true if it completed (possibly exceptionally) before the given timeout and the current thread has not been interrupted. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#quietlyJoinUninterruptibly(kotlin.Long,%20java.util.concurrent.TimeUnit)(timeout: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, unit: https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit!)` Tries to join this task, returning true if it completed (possibly exceptionally) before the given timeout. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#reinitialize()()` Resets the internal bookkeeping state of this task, allowing a subsequent `fork`. |
| open V | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#resultNow()()` Returns the computed result, without waiting. |
| --- | --- |
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#setForkJoinTaskTag(kotlin.Short)(newValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Atomically sets the tag value for this task and returns the old value. |
| open [Future.State](../java/util/concurrent/Future.State.md)! | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#state()()` {@return the computation state} |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#tryUnfork()()` Tries to unschedule this task for execution. |
| --- | --- |

| Protected methods ||
|---|---|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#exec()()` Immediately performs the base action of this task and returns true if, upon return from this method, this task is guaranteed to have completed. |
| open static [ForkJoinTask](ForkJoinTask.md)\<\*\>! | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#peekNextLocalTask()()` Returns, but does not unschedule or execute, a task queued by the current thread but not yet executed, if one is immediately available. |
| open static [ForkJoinTask](ForkJoinTask.md)\<\*\>! | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#pollNextLocalTask()()` Unschedules and returns, without executing, the next task queued by the current thread but not yet executed, if the current thread is operating in a ForkJoinPool. |
| --- | --- |
| open static [ForkJoinTask](ForkJoinTask.md)\<\*\>! | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#pollTask()()` If the current thread is operating in a ForkJoinPool, unschedules and returns, without executing, the next task queued by the current thread but not yet executed, if one is available, or if not available, a task that was forked by some other thread, if available. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#setRawResult(java.util.concurrent.ForkJoinTask.V)(value: V)` Forces the given value to be returned as a result. |

## Public constructors

### ForkJoinTask

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ForkJoinTask()
```

Constructor for subclasses to call.

## Public methods

### adapt

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun adapt(runnable: Runnable!): ForkJoinTask<*>!
```

Returns a new `ForkJoinTask` that performs the `run` method of the given `Runnable` as its action, and returns a null result upon `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#join()`.

| Parameters ||
|---|---|
| `runnable` | [Runnable](../java.lang/Runnable.md)!: the runnable action |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#<*>!` | the task |

### adapt

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <T : Any!> adapt(
    runnable: Runnable!, 
    result: T
): ForkJoinTask<T>!
```

Returns a new `ForkJoinTask` that performs the `run` method of the given `Runnable` as its action, and returns the given result upon `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#join()`.

| Parameters ||
|---|---|
| `<T>` | the type of the result |
| `runnable` | [Runnable](../java.lang/Runnable.md)!: the runnable action |
| `result` | T: the result upon completion |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#<T>!` | the task |

### adapt

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <T : Any!> adapt(callable: Callable<out T>!): ForkJoinTask<T>!
```

Returns a new `ForkJoinTask` that performs the `call` method of the given `Callable` as its action, and returns its result upon `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#join()`, translating any checked exceptions encountered into `RuntimeException`.

| Parameters ||
|---|---|
| `<T>` | the type of the callable's result |
| `callable` | [Callable](Callable.md)\<out T\>!: the callable action |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#<T>!` | the task |

### adaptInterruptible

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <T : Any!> adaptInterruptible(callable: Callable<out T>!): ForkJoinTask<T>!
```

Returns a new `ForkJoinTask` that performs the `call` method of the given `Callable` as its action, and returns its result upon `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#join()`, translating any checked exceptions encountered into `RuntimeException`. Additionally, invocations of `cancel` with `mayInterruptIfRunning true` will attempt to interrupt the thread performing the task.

| Parameters ||
|---|---|
| `<T>` | the type of the callable's result |
| `callable` | [Callable](Callable.md)\<out T\>!: the callable action |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#<T>!` | the task |

### cancel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun cancel(mayInterruptIfRunning: Boolean): Boolean
```

Attempts to cancel execution of this task. This attempt will fail if the task has already completed or could not be cancelled for some other reason. If successful, and this task has not started when `cancel` is called, execution of this task is suppressed. After this method returns successfully, unless there is an intervening call to `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#reinitialize()`, subsequent calls to `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#isCancelled()`, `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#isDone()`, and `cancel` will return `true` and calls to `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#join()` and related methods will result in `CancellationException`.

This method may be overridden in subclasses, but if so, must still ensure that these properties hold. In particular, the `cancel` method itself must not throw exceptions.

This method is designed to be invoked by *other* tasks. To terminate the current task, you can just return or throw an unchecked exception from its computation method, or invoke `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#completeExceptionally(kotlin.Throwable)`.

| Parameters ||
|---|---|
| `mayInterruptIfRunning` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): this value has no effect in the default implementation because interrupts are not used to control cancellation. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this task is now cancelled |

### compareAndSetForkJoinTaskTag

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun compareAndSetForkJoinTaskTag(
    expect: Short, 
    update: Short
): Boolean
```

Atomically conditionally sets the tag value for this task. Among other applications, tags can be used as visit markers in tasks operating on graphs, as in methods that check: `if (task.compareAndSetForkJoinTaskTag((short)0, (short)1))` before processing, otherwise exiting because the node has already been visited.

| Parameters ||
|---|---|
| `expect` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): the expected tag value |
| `update` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): the new tag value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if successful; i.e., the current value was equal to `expect` and was changed to `update`. |

### complete

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun complete(value: V): Unit
```

Completes this task, and if not already aborted or cancelled, returning the given value as the result of subsequent invocations of `join` and related operations. This method may be used to provide results for asynchronous tasks, or to provide alternative handling for tasks that would not otherwise complete normally. Its use in other situations is discouraged. This method is overridable, but overridden versions must invoke `super` implementation to maintain guarantees.

| Parameters ||
|---|---|
| `value` | V: the result value for this task |

### completeExceptionally

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun completeExceptionally(ex: Throwable!): Unit
```

Completes this task abnormally, and if not already aborted or cancelled, causes it to throw the given exception upon `join` and related operations. This method may be used to induce exceptions in asynchronous tasks, or to force completion of tasks that would not otherwise complete. Its use in other situations is discouraged. This method is overridable, but overridden versions must invoke `super` implementation to maintain guarantees.

| Parameters ||
|---|---|
| `ex` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: the exception to throw. If this exception is not a `RuntimeException` or `Error`, the actual exception thrown will be a `RuntimeException` with cause `ex`. |

### exceptionNow

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun exceptionNow(): Throwable!
```

Returns the exception thrown by the task, without waiting.

This method is for cases where the caller knows that the task has already completed with an exception.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html!` | the exception thrown by the task |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the task has not completed, the task completed normally, or the task was cancelled |

### fork

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun fork(): ForkJoinTask<V>!
```

Arranges to asynchronously execute this task in the pool the current task is running in, if applicable, or using the `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#commonPool()` if not `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#inForkJoinPool()`. While it is not necessarily enforced, it is a usage error to fork a task more than once unless it has completed and been reinitialized. Subsequent modifications to the state of this task or any data it operates on are not necessarily consistently observable by any thread other than the one executing it unless preceded by a call to `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#join()` or related methods, or a call to `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#isDone()` returning `true`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#<V>!` | `this`, to simplify usage |

### get

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun get(): V
```

Waits if necessary for the computation to complete, and then retrieves its result.

| Return ||
|---|---|
| `V` | the computed result |

| Exceptions ||
|---|---|
| `java.lang.InterruptedException` | if the current thread is not a member of a ForkJoinPool and was interrupted while waiting |
| `java.util.concurrent.CancellationException` | if the computation was cancelled |
| `java.util.concurrent.ExecutionException` | if the computation threw an exception |
| --- | --- |

### get

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun get(
    timeout: Long, 
    unit: TimeUnit!
): V
```

Waits if necessary for at most the given time for the computation to complete, and then retrieves its result, if available.

| Parameters ||
|---|---|
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the maximum time to wait |
| `unit` | [TimeUnit](TimeUnit.md)!: the time unit of the timeout argument |

| Return ||
|---|---|
| `V` | the computed result |

| Exceptions ||
|---|---|
| `java.lang.InterruptedException` | if the current thread is not a member of a ForkJoinPool and was interrupted while waiting |
| `java.util.concurrent.CancellationException` | if the computation was cancelled |
| `java.util.concurrent.ExecutionException` | if the computation threw an exception |
| --- | --- |
| `java.util.concurrent.TimeoutException` | if the wait timed out |

### getException

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getException(): Throwable!
```

Returns the exception thrown by the base computation, or a `CancellationException` if cancelled, or `null` if none or if the method has not yet completed.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html!` | the exception, or `null` if none |

### getForkJoinTaskTag

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getForkJoinTaskTag(): Short
```

Returns the tag for this task.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | the tag for this task |

### getPool

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getPool(): ForkJoinPool!
```

Returns the pool hosting the current thread, or `null` if the current thread is executing outside of any ForkJoinPool.

This method returns `null` if and only if `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#inForkJoinPool()` returns `false`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool!` | the pool, or `null` if none |

### getQueuedTaskCount

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getQueuedTaskCount(): Int
```

Returns an estimate of the number of tasks that have been forked by the current worker thread but not yet executed. This value may be useful for heuristic decisions about whether to fork other tasks.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of tasks |

### getRawResult

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getRawResult(): V
```

Returns the result that would be returned by `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#join()`, even if this task completed abnormally, or `null` if this task is not known to have been completed. This method is designed to aid debugging, as well as to support extensions. Its use in any other context is discouraged.

| Return ||
|---|---|
| `V` | the result, or `null` if not completed |

### getSurplusQueuedTaskCount

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getSurplusQueuedTaskCount(): Int
```

Returns an estimate of how many more locally queued tasks are held by the current worker thread than there are other worker threads that might steal them, or zero if this thread is not operating in a ForkJoinPool. This value may be useful for heuristic decisions about whether to fork other tasks. In many usages of ForkJoinTasks, at steady state, each worker should aim to maintain a small constant surplus (for example, 3) of tasks, and to process computations locally if this threshold is exceeded.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the surplus number of tasks, which may be negative |

### helpQuiesce

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun helpQuiesce(): Unit
```

Possibly executes tasks until the pool hosting the current task [is quiescent](ForkJoinPool.md)). This method may be of use in designs in which many tasks are forked, but none are explicitly joined, instead executing them until all are processed.

### inForkJoinPool

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun inForkJoinPool(): Boolean
```

Returns `true` if the current thread is a `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinWorkerThread` executing as a ForkJoinPool computation.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the current thread is a `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinWorkerThread` executing as a ForkJoinPool computation, or `false` otherwise |

### invoke

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun invoke(): V
```

Commences performing this task, awaits its completion if necessary, and returns its result, or throws an (unchecked) `RuntimeException` or `Error` if the underlying computation did so.

| Return ||
|---|---|
| `V` | the computed result |

### invokeAll

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <T : ForkJoinTask<*>!> invokeAll(tasks: MutableCollection<T>!): MutableCollection<T>!
```

Forks all tasks in the specified collection, returning when `isDone` holds for each task or an (unchecked) exception is encountered, in which case the exception is rethrown. If more than one task encounters an exception, then this method throws any one of these exceptions. If any task encounters an exception, others may be cancelled. However, the execution status of individual tasks is not guaranteed upon exceptional return. The status of each task may be obtained using `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#getException()` and related methods to check if they have been cancelled, completed normally or exceptionally, or left unprocessed.

| Parameters ||
|---|---|
| `<T>` | the type of the values returned from the tasks |
| `tasks` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<T\>!: the collection of tasks |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<T>!` | the tasks argument, to simplify usage |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if tasks or any element are null |

### invokeAll

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun invokeAll(
    t1: ForkJoinTask<*>!, 
    t2: ForkJoinTask<*>!
): Unit
```

Forks the given tasks, returning when `isDone` holds for each task or an (unchecked) exception is encountered, in which case the exception is rethrown. If more than one task encounters an exception, then this method throws any one of these exceptions. If any task encounters an exception, the other may be cancelled. However, the execution status of individual tasks is not guaranteed upon exceptional return. The status of each task may be obtained using `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#getException()` and related methods to check if they have been cancelled, completed normally or exceptionally, or left unprocessed.

| Parameters ||
|---|---|
| `t1` | [ForkJoinTask](ForkJoinTask.md)\<\*\>!: the first task |
| `t2` | [ForkJoinTask](ForkJoinTask.md)\<\*\>!: the second task |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if any task is null |

### invokeAll

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun invokeAll(vararg tasks: ForkJoinTask<*>!): Unit
```

Forks the given tasks, returning when `isDone` holds for each task or an (unchecked) exception is encountered, in which case the exception is rethrown. If more than one task encounters an exception, then this method throws any one of these exceptions. If any task encounters an exception, others may be cancelled. However, the execution status of individual tasks is not guaranteed upon exceptional return. The status of each task may be obtained using `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#getException()` and related methods to check if they have been cancelled, completed normally or exceptionally, or left unprocessed.

| Parameters ||
|---|---|
| `tasks` | [ForkJoinTask](ForkJoinTask.md)\<\*\>!: the tasks |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if any task is null |

### isCancelled

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isCancelled(): Boolean
```

Returns `true` if this task was cancelled before it completed normally.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this task was cancelled before it completed |

### isCompletedAbnormally

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isCompletedAbnormally(): Boolean
```

Returns `true` if this task threw an exception or was cancelled.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this task threw an exception or was cancelled |

### isCompletedNormally

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isCompletedNormally(): Boolean
```

Returns `true` if this task completed without throwing an exception and was not cancelled.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this task completed without throwing an exception and was not cancelled |

### isDone

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isDone(): Boolean
```

Returns `true` if this task completed. Completion may be due to normal termination, an exception, or cancellation -- in all of these cases, this method will return `true`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this task completed |

### join

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun join(): V
```

Returns the result of the computation when it [is done](ForkJoinTask.md)). This method differs from `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#get()` in that abnormal completion results in `RuntimeException` or `Error`, not `ExecutionException`, and that interrupts of the calling thread do *not* cause the method to abruptly return by throwing `InterruptedException`.

| Return ||
|---|---|
| `V` | the computed result |

### quietlyComplete

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun quietlyComplete(): Unit
```

Completes this task normally without setting a value. The most recent value established by `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#setRawResult(java.util.concurrent.ForkJoinTask.V)` (or `null` by default) will be returned as the result of subsequent invocations of `join` and related operations.

### quietlyInvoke

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun quietlyInvoke(): Unit
```

Commences performing this task and awaits its completion if necessary, without returning its result or throwing its exception.

### quietlyJoin

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun quietlyJoin(): Unit
```

Joins this task, without returning its result or throwing its exception. This method may be useful when processing collections of tasks when some have been cancelled or otherwise known to have aborted.

### quietlyJoin

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun quietlyJoin(
    timeout: Long, 
    unit: TimeUnit!
): Boolean
```

Tries to join this task, returning true if it completed (possibly exceptionally) before the given timeout and the current thread has not been interrupted.

| Parameters ||
|---|---|
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the maximum time to wait |
| `unit` | [TimeUnit](TimeUnit.md)!: the time unit of the timeout argument |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this task completed |

| Exceptions ||
|---|---|
| `java.lang.InterruptedException` | if the current thread was interrupted while waiting |

### quietlyJoinUninterruptibly

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun quietlyJoinUninterruptibly(
    timeout: Long, 
    unit: TimeUnit!
): Boolean
```

Tries to join this task, returning true if it completed (possibly exceptionally) before the given timeout.

| Parameters ||
|---|---|
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the maximum time to wait |
| `unit` | [TimeUnit](TimeUnit.md)!: the time unit of the timeout argument |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this task completed |

### reinitialize

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun reinitialize(): Unit
```

Resets the internal bookkeeping state of this task, allowing a subsequent `fork`. This method allows repeated reuse of this task, but only if reuse occurs when this task has either never been forked, or has been forked, then completed and all outstanding joins of this task have also completed. Effects under any other usage conditions are not guaranteed. This method may be useful when executing pre-constructed trees of subtasks in loops.

Upon completion of this method, `isDone()` reports `false`, and `getException()` reports `null`. However, the value returned by `getRawResult` is unaffected. To clear this value, you can invoke `setRawResult(null)`.

### resultNow

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun resultNow(): V
```

Returns the computed result, without waiting.

This method is for cases where the caller knows that the task has already completed successfully, for example when filtering a stream of Future objects for the successful tasks and using a mapping operation to obtain a stream of results. {@snippet lang=java : \* results = futures.stream() \* .filter(f -\> f.state() == Future.State.SUCCESS) \* .map(Future::resultNow) \* .toList(); \* }

| Return ||
|---|---|
| `V` | the computed result |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the task has not completed or the task did not complete with a result |

### setForkJoinTaskTag

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setForkJoinTaskTag(newValue: Short): Short
```

Atomically sets the tag value for this task and returns the old value.

| Parameters ||
|---|---|
| `newValue` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): the new tag value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | the previous value of the tag |

### state

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun state(): Future.State!
```

{@return the computation state}

### tryUnfork

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun tryUnfork(): Boolean
```

Tries to unschedule this task for execution. This method will typically (but is not guaranteed to) succeed if this task is the most recently forked task by the current thread, and has not commenced executing in another thread. This method may be useful when arranging alternative local processing of tasks that could have been, but were not, stolen.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if unforked |

## Protected methods

### exec

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun exec(): Boolean
```

Immediately performs the base action of this task and returns true if, upon return from this method, this task is guaranteed to have completed. This method may return false otherwise, to indicate that this task is not necessarily complete (or is not known to be complete), for example in asynchronous actions that require explicit invocations of completion methods. This method may also throw an (unchecked) exception to indicate abnormal exit. This method is designed to support extensions, and should not in general be called otherwise.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this task is known to have completed normally |

### peekNextLocalTask

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open static fun peekNextLocalTask(): ForkJoinTask<*>!
```

Returns, but does not unschedule or execute, a task queued by the current thread but not yet executed, if one is immediately available. There is no guarantee that this task will actually be polled or executed next. Conversely, this method may return null even if a task exists but cannot be accessed without contention with other threads. This method is designed primarily to support extensions, and is unlikely to be useful otherwise.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#<*>!` | the next task, or `null` if none are available |

### pollNextLocalTask

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open static fun pollNextLocalTask(): ForkJoinTask<*>!
```

Unschedules and returns, without executing, the next task queued by the current thread but not yet executed, if the current thread is operating in a ForkJoinPool. This method is designed primarily to support extensions, and is unlikely to be useful otherwise.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#<*>!` | the next task, or `null` if none are available |

### pollTask

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open static fun pollTask(): ForkJoinTask<*>!
```

If the current thread is operating in a ForkJoinPool, unschedules and returns, without executing, the next task queued by the current thread but not yet executed, if one is available, or if not available, a task that was forked by some other thread, if available. Availability may be transient, so a `null` result does not necessarily imply quiescence of the pool this task is operating in. This method is designed primarily to support extensions, and is unlikely to be useful otherwise.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask#<*>!` | a task, or `null` if none are available |

### setRawResult

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun setRawResult(value: V): Unit
```

Forces the given value to be returned as a result. This method is designed to support extensions, and should not in general be called otherwise.

| Parameters ||
|---|---|
| `value` | V: the value |
