# ExecutorService

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ExecutorService

```
interface ExecutorService : AutoCloseable, Executor
```

| [java.util.concurrent.ExecutorService](../java/util/concurrent/ExecutorService.md) |

| Known Direct Subclasses [AbstractExecutorService](../java/util/concurrent/AbstractExecutorService.md), [ScheduledExecutorService](../java/util/concurrent/ScheduledExecutorService.md) |--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AbstractExecutorService](../java/util/concurrent/AbstractExecutorService.md) | Provides default implementations of [ExecutorService](../java/util/concurrent/ExecutorService.md) execution methods. | | [ScheduledExecutorService](../java/util/concurrent/ScheduledExecutorService.md) | An [ExecutorService](../java/util/concurrent/ExecutorService.md) that can schedule commands to run after a given delay, or to execute periodically. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ForkJoinPool](../java/util/concurrent/ForkJoinPool.md), [ScheduledThreadPoolExecutor](../java/util/concurrent/ScheduledThreadPoolExecutor.md), [ScheduledThreadPoolExecutor](../java/util/concurrent/ScheduledThreadPoolExecutor.md), [ThreadPoolExecutor](../java/util/concurrent/ThreadPoolExecutor.md) |--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ForkJoinPool](../java/util/concurrent/ForkJoinPool.md) | An [ExecutorService](../java/util/concurrent/ExecutorService.md) for running [ForkJoinTask](../java/util/concurrent/ForkJoinTask.md) s. | | [ScheduledThreadPoolExecutor](../java/util/concurrent/ScheduledThreadPoolExecutor.md) | A [ThreadPoolExecutor](../java/util/concurrent/ThreadPoolExecutor.md) that can additionally schedule commands to run after a given delay, or to execute periodically. | | [ScheduledThreadPoolExecutor](../java/util/concurrent/ScheduledThreadPoolExecutor.md) | A [ThreadPoolExecutor](../java/util/concurrent/ThreadPoolExecutor.md) that can additionally schedule commands to run after a given delay, or to execute periodically. | | [ThreadPoolExecutor](../java/util/concurrent/ThreadPoolExecutor.md) | An [ExecutorService](../java/util/concurrent/ExecutorService.md) that executes each submitted task using one of possibly several pooled threads, normally configured using [Executors](../java/util/concurrent/Executors.md) factory methods. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

An [Executor](../java/util/concurrent/Executor.md) that provides methods to manage termination and methods that can produce a [Future](../java/util/concurrent/Future.md) for tracking progress of one or more asynchronous tasks.

An`ExecutorService`can be shut down, which will cause it to reject new tasks. Two different methods are provided for shutting down an`ExecutorService`. The [shutdown](../java/util/concurrent/ExecutorService.md))method will allow previously submitted tasks to execute before terminating, while the [shutdownNow](../java/util/concurrent/ExecutorService.md))method prevents waiting tasks from starting and attempts to stop currently executing tasks. Upon termination, an executor has no tasks actively executing, no tasks awaiting execution, and no new tasks can be submitted. An unused`ExecutorService`should be shut down to allow reclamation of its resources.

Method`submit`extends base method [java.util.concurrent.Executor#execute(java.lang.Runnable)](../java/util/concurrent/Executor.md))by creating and returning a [Future](../java/util/concurrent/Future.md) that can be used to cancel execution and/or wait for completion. Methods`invokeAny`and`invokeAll`perform the most commonly useful forms of bulk execution, executing a collection of tasks and then waiting for at least one, or all, to complete. (Class [ExecutorCompletionService](../java/util/concurrent/ExecutorCompletionService.md) can be used to write customized variants of these methods.)

The [Executors](../java/util/concurrent/Executors.md) class provides factory methods for the executor services provided in this package.

## Usage Examples

Here is a sketch of a network service in which threads in a thread pool service incoming requests. It uses the preconfigured java.util.concurrent.Executors#newFixedThreadPool factory method: 

```kotlin
<code>class NetworkService implements Runnable {
    private final ServerSocket serverSocket;
    private final ExecutorService pool;
 
    public NetworkService(int port, int poolSize)
        throws IOException {
      serverSocket = new ServerSocket(port);
      pool = Executors.newFixedThreadPool(poolSize);
    }
 
    public void run() { // run the service
      try {
        for (;;) {
          pool.execute(new Handler(serverSocket.accept()));
        }
      } catch (IOException ex) {
        pool.shutdown();
      }
    }
  }
 
  class Handler implements Runnable {
    private final Socket socket;
    Handler(Socket socket) { this.socket = socket; }
    public void run() {
      // read and service request on socket
    }
  }</code>
```
An`ExecutorService`may also be established and closed (shutdown, blocking until terminated) as follows; illustrating with a different`Executors`factory method: 

```kotlin
<code>try (ExecutorService e =  Executors.newWorkStealingPool()) {
    // submit or execute many tasks with e ...
  }</code>
```
Further customization is also possible. For example, the following method shuts down an`ExecutorService`in two phases, first by calling`shutdown`to reject incoming tasks, and then calling`shutdownNow`, if necessary, to cancel any lingering tasks: 

```kotlin
<code>void shutdownAndAwaitTermination(ExecutorService pool) {
    pool.shutdown(); // Disable new tasks from being submitted
    try {
      // Wait a while for existing tasks to terminate
      if (!pool.awaitTermination(60, TimeUnit.SECONDS)) {
        pool.shutdownNow(); // Cancel currently executing tasks
        // Wait a while for tasks to respond to being cancelled
        if (!pool.awaitTermination(60, TimeUnit.SECONDS))
            System.err.println("Pool did not terminate");
      }
    } catch (InterruptedException ex) {
      // (Re-)Cancel if current thread also interrupted
      pool.shutdownNow();
      // Preserve interrupt status
      Thread.currentThread().interrupt();
    }
  }</code>
```

Memory consistency effects: Actions in a thread prior to the submission of a`Runnable`or`Callable`task to an`ExecutorService` [*happen-before*](../java/util/concurrent/_package.md) any actions taken by that task, which in turn*happen-before* the result is retrieved via`Future.get()`.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [awaitTermination](../java/util/concurrent/ExecutorService.md))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](../java/util/concurrent/TimeUnit.md)!`)` Blocks until all tasks have completed execution after a shutdown request, or the timeout occurs, or the current thread is interrupted, whichever happens first. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../java/util/concurrent/ExecutorService.md))`()` Initiates an orderly shutdown in which previously submitted tasks are executed, but no new tasks will be accepted. |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Future](../java/util/concurrent/Future.md)\<T\>!\>! | [invokeAll](../java/util/concurrent/ExecutorService.md))`(`tasks:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` ` [Callable](../java/util/concurrent/Callable.md)<T>!>!`)` Executes the given tasks, returning a list of Futures holding their status and results when all complete. |
| --- | --- |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Future](../java/util/concurrent/Future.md)\<T\>!\>! | [invokeAll](../java/util/concurrent/ExecutorService.md))`(`tasks:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` ` [Callable](../java/util/concurrent/Callable.md)<T>!>!`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](../java/util/concurrent/TimeUnit.md)!`)` Executes the given tasks, returning a list of Futures holding their status and results when all complete or the timeout expires, whichever happens first. |
| abstractT | [invokeAny](../java/util/concurrent/ExecutorService.md))`(`tasks:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` ` [Callable](../java/util/concurrent/Callable.md)<T>!>!`)` Executes the given tasks, returning the result of one that has completed successfully (i.e., without throwing an exception), if any do. |
| abstractT | [invokeAny](../java/util/concurrent/ExecutorService.md))`(`tasks:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` ` [Callable](../java/util/concurrent/Callable.md)<T>!>!`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](../java/util/concurrent/TimeUnit.md)!`)` Executes the given tasks, returning the result of one that has completed successfully (i.e., without throwing an exception), if any do before the given timeout elapses. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isShutdown](../java/util/concurrent/ExecutorService.md))`()` Returns`true`if this executor has been shut down. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTerminated](../java/util/concurrent/ExecutorService.md))`()` Returns`true`if all tasks have completed following shut down. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [shutdown](../java/util/concurrent/ExecutorService.md))`()` Initiates an orderly shutdown in which previously submitted tasks are executed, but no new tasks will be accepted. |
| --- | --- |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Runnable](../java/lang/Runnable.md)!\>! | [shutdownNow](../java/util/concurrent/ExecutorService.md))`()` Attempts to stop all actively executing tasks, halts the processing of waiting tasks, and returns a list of the tasks that were awaiting execution. |
| abstract [Future](../java/util/concurrent/Future.md)\<\*\>! | [submit](../java/util/concurrent/ExecutorService.md))`(`task:` ` [Runnable](../java/lang/Runnable.md)!`)` Submits a Runnable task for execution and returns a Future representing that task. |
| abstract [Future](../java/util/concurrent/Future.md)\<T\>! | [submit](../java/util/concurrent/ExecutorService.md))`(`task:` ` [Runnable](../java/lang/Runnable.md)!`, `result:` `T`)` Submits a Runnable task for execution and returns a Future representing that task. |
| --- | --- |
| abstract [Future](../java/util/concurrent/Future.md)\<T\>! | [submit](../java/util/concurrent/ExecutorService.md))`(`task:` ` [Callable](../java/util/concurrent/Callable.md)<T>!`)` Submits a value-returning task for execution and returns a Future representing the pending results of the task. |

| Inherited functions ||
|---|---|
| From class [Executor](../java/util/concurrent/Executor.md) |------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [execute](../java/util/concurrent/Executor.md))`(`command:` ` [Runnable](../java/lang/Runnable.md)!`)` <br /> Executes the given command at some time in the future. The command may execute in a new thread, in a pooled thread, or in the calling thread, at the discretion of the`Executor`implementation. <br /> | ||

## Public methods

### awaitTermination

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun awaitTermination(
    timeout: Long, 
    unit: TimeUnit!
): Boolean
```

Blocks until all tasks have completed execution after a shutdown request, or the timeout occurs, or the current thread is interrupted, whichever happens first.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the maximum time to wait |
| `unit` | [TimeUnit](../java/util/concurrent/TimeUnit.md)!:the time unit of the timeout argument |

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

Initiates an orderly shutdown in which previously submitted tasks are executed, but no new tasks will be accepted. This method waits until all tasks have completed execution and the executor has terminated.

If interrupted while waiting, this method stops all executing tasks as if by invoking [shutdownNow()](../java/util/concurrent/ExecutorService.md)). It then continues to wait until all actively executing tasks have completed. Tasks that were awaiting execution are not executed. The interrupt status will be re-asserted before this method returns.

If already terminated, invoking this method has no effect.

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.lang.SecurityException` | if a security manager exists and shutting down this ExecutorService may manipulate threads that the caller is not permitted to modify because it does not hold`("modifyThread")`, or the security manager's`checkAccess`method denies access. |

### invokeAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <T : Any!> invokeAll(tasks: MutableCollection<out Callable<T>!>!): MutableList<Future<T>!>!
```

Executes the given tasks, returning a list of Futures holding their status and results when all complete. [Future.isDone](../java/util/concurrent/Future.md))is`true`for each element of the returned list. Note that a*completed*task could have terminated either normally or by throwing an exception. The results of this method are undefined if the given collection is modified while this operation is in progress.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tasks` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<out [Callable](../java/util/concurrent/Callable.md)\<T\>!\>!:the collection of tasks |
| `<T>` | the type of the values returned from the tasks |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Future](../java/util/concurrent/Future.md)<T>!>! | a list of Futures representing the tasks, in the same sequential order as produced by the iterator for the given task list, each of which has completed |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting, in which case unfinished tasks are cancelled |
| `java.lang.NullPointerException` | if tasks or any of its elements are`null` |
| `java.util.concurrent.RejectedExecutionException` | if any task cannot be scheduled for execution |
| --- | --- |

### invokeAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <T : Any!> invokeAll(
    tasks: MutableCollection<out Callable<T>!>!, 
    timeout: Long, 
    unit: TimeUnit!
): MutableList<Future<T>!>!
```

Executes the given tasks, returning a list of Futures holding their status and results when all complete or the timeout expires, whichever happens first. [Future.isDone](../java/util/concurrent/Future.md))is`true`for each element of the returned list. Upon return, tasks that have not completed are cancelled. Note that a*completed*task could have terminated either normally or by throwing an exception. The results of this method are undefined if the given collection is modified while this operation is in progress.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tasks` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<out [Callable](../java/util/concurrent/Callable.md)\<T\>!\>!:the collection of tasks |
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the maximum time to wait |
| `unit` | [TimeUnit](../java/util/concurrent/TimeUnit.md)!:the time unit of the timeout argument |
| --- | --- |
| `<T>` | the type of the values returned from the tasks |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Future](../java/util/concurrent/Future.md)<T>!>! | a list of Futures representing the tasks, in the same sequential order as produced by the iterator for the given task list. If the operation did not time out, each task will have completed. If it did time out, some of these tasks will not have completed. |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting, in which case unfinished tasks are cancelled |
| `java.lang.NullPointerException` | if tasks, any of its elements, or unit are`null` |
| `java.util.concurrent.RejectedExecutionException` | if any task cannot be scheduled for execution |
| --- | --- |

### invokeAny

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <T : Any!> invokeAny(tasks: MutableCollection<out Callable<T>!>!): T
```

Executes the given tasks, returning the result of one that has completed successfully (i.e., without throwing an exception), if any do. Upon normal or exceptional return, tasks that have not completed are cancelled. The results of this method are undefined if the given collection is modified while this operation is in progress.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tasks` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<out [Callable](../java/util/concurrent/Callable.md)\<T\>!\>!:the collection of tasks |
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

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <T : Any!> invokeAny(
    tasks: MutableCollection<out Callable<T>!>!, 
    timeout: Long, 
    unit: TimeUnit!
): T
```

Executes the given tasks, returning the result of one that has completed successfully (i.e., without throwing an exception), if any do before the given timeout elapses. Upon normal or exceptional return, tasks that have not completed are cancelled. The results of this method are undefined if the given collection is modified while this operation is in progress.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tasks` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<out [Callable](../java/util/concurrent/Callable.md)\<T\>!\>!:the collection of tasks |
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the maximum time to wait |
| `unit` | [TimeUnit](../java/util/concurrent/TimeUnit.md)!:the time unit of the timeout argument |
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

### isShutdown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isShutdown(): Boolean
```

Returns`true`if this executor has been shut down.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this executor has been shut down |

### isTerminated

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isTerminated(): Boolean
```

Returns`true`if all tasks have completed following shut down. Note that`isTerminated`is never`true`unless either`shutdown`or`shutdownNow`was called first.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if all tasks have completed following shut down |

### shutdown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun shutdown(): Unit
```

Initiates an orderly shutdown in which previously submitted tasks are executed, but no new tasks will be accepted. Invocation has no additional effect if already shut down.

This method does not wait for previously submitted tasks to complete execution. Use [awaitTermination](../java/util/concurrent/ExecutorService.md))to do that. 

### shutdownNow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun shutdownNow(): MutableList<Runnable!>!
```

Attempts to stop all actively executing tasks, halts the processing of waiting tasks, and returns a list of the tasks that were awaiting execution.

This method does not wait for actively executing tasks to terminate. Use [awaitTermination](../java/util/concurrent/ExecutorService.md))to do that.

There are no guarantees beyond best-effort attempts to stop processing actively executing tasks. For example, typical implementations will cancel via [Thread.interrupt](../java/lang/Thread.md)), so any task that fails to respond to interrupts may never terminate.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Runnable](../java/lang/Runnable.md)!>! | list of tasks that never commenced execution |

### submit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun submit(task: Runnable!): Future<*>!
```

Submits a Runnable task for execution and returns a Future representing that task. The Future's`get`method will return`null`upon*successful*completion.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------|
| `task` | [Runnable](../java/lang/Runnable.md)!:the task to submit |

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------------|
| [Future](../java/util/concurrent/Future.md)<*>! | a Future representing pending completion of the task |

| Exceptions ||
|---------------------------------------------------|-----------------------------------------------|
| `java.util.concurrent.RejectedExecutionException` | if the task cannot be scheduled for execution |
| `java.lang.NullPointerException` | if the task is null |

### submit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <T : Any!> submit(
    task: Runnable!, 
    result: T
): Future<T>!
```

Submits a Runnable task for execution and returns a Future representing that task. The Future's`get`method will return the given result upon successful completion.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------|
| `task` | [Runnable](../java/lang/Runnable.md)!:the task to submit |
| `result` | T:the result to return |
| `<T>` | the type of the result |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------------|
| [Future](../java/util/concurrent/Future.md)<T>! | a Future representing pending completion of the task |

| Exceptions ||
|---------------------------------------------------|-----------------------------------------------|
| `java.util.concurrent.RejectedExecutionException` | if the task cannot be scheduled for execution |
| `java.lang.NullPointerException` | if the task is null |

### submit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <T : Any!> submit(task: Callable<T>!): Future<T>!
```

Submits a value-returning task for execution and returns a Future representing the pending results of the task. The Future's`get`method will return the task's result upon successful completion.

If you would like to immediately block waiting for a task, you can use constructions of the form`result = exec.submit(aCallable).get();`

Note: The [Executors](../java/util/concurrent/Executors.md) class includes a set of methods that can convert some other common closure-like objects, for example, [java.security.PrivilegedAction](../java/security/PrivilegedAction.md) to [Callable](../java/util/concurrent/Callable.md) form so they can be submitted.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------|
| `task` | [Callable](../java/util/concurrent/Callable.md)\<T\>!:the task to submit |
| `<T>` | the type of the task's result |

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------------|
| [Future](../java/util/concurrent/Future.md)<T>! | a Future representing pending completion of the task |

| Exceptions ||
|---------------------------------------------------|-----------------------------------------------|
| `java.util.concurrent.RejectedExecutionException` | if the task cannot be scheduled for execution |
| `java.lang.NullPointerException` | if the task is null |
