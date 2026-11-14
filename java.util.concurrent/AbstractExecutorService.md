# AbstractExecutorService

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AbstractExecutorService

```
abstract class AbstractExecutorService : ExecutorService
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.concurrent.AbstractExecutorService](AbstractExecutorService.md) |

| Known Direct Subclasses [ForkJoinPool](ForkJoinPool.md), [ThreadPoolExecutor](ThreadPoolExecutor.md) |--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ForkJoinPool](ForkJoinPool.md) | An [ExecutorService](ExecutorService.md) for running [ForkJoinTask](ForkJoinTask.md) s. | | [ThreadPoolExecutor](ThreadPoolExecutor.md) | An [ExecutorService](ExecutorService.md) that executes each submitted task using one of possibly several pooled threads, normally configured using [Executors](Executors.md) factory methods. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ScheduledThreadPoolExecutor](ScheduledThreadPoolExecutor.md) |--------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ScheduledThreadPoolExecutor](ScheduledThreadPoolExecutor.md) | A [ThreadPoolExecutor](ThreadPoolExecutor.md) that can additionally schedule commands to run after a given delay, or to execute periodically. | |
| --- | --- | --- | --- | --- | --- | --- |

Provides default implementations of [ExecutorService](ExecutorService.md) execution methods. This class implements the`submit`,`invokeAny`and`invokeAll`methods using a [RunnableFuture](RunnableFuture.md) returned by`newTaskFor`, which defaults to the [FutureTask](FutureTask.md) class provided in this package. For example, the implementation of`submit(Runnable)`creates an associated`RunnableFuture`that is executed and returned. Subclasses may override the`newTaskFor`methods to return`RunnableFuture`implementations other than`FutureTask`.

**Extension example.** Here is a sketch of a class that customizes [ThreadPoolExecutor](ThreadPoolExecutor.md) to use a`CustomTask`class instead of the default`FutureTask`: 

```kotlin
<code>public class CustomThreadPoolExecutor extends ThreadPoolExecutor {
 
    static class CustomTask&lt;V&gt; implements RunnableFuture&lt;V&gt; { ... }
 
    protected &lt;V&gt; RunnableFuture&lt;V&gt; newTaskFor(Callable&lt;V&gt; c) {
        return new CustomTask&lt;V&gt;(c);
    }
    protected &lt;V&gt; RunnableFuture&lt;V&gt; newTaskFor(Runnable r, V v) {
        return new CustomTask&lt;V&gt;(r, v);
    }
    // ... add constructors, etc.
  }</code>
```

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AbstractExecutorService](AbstractExecutorService.md))`()` Constructor for subclasses to call. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Future](Future.md)\<T\>!\>! | [invokeAll](AbstractExecutorService.md))`(`tasks:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` ` [Callable](Callable.md)<T>!>!`)` <br /> |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Future](Future.md)\<T\>!\>! | [invokeAll](AbstractExecutorService.md))`(`tasks:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` ` [Callable](Callable.md)<T>!>!`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` <br /> |
| openT | [invokeAny](AbstractExecutorService.md))`(`tasks:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` ` [Callable](Callable.md)<T>!>!`)` <br /> |
| --- | --- |
| openT | [invokeAny](AbstractExecutorService.md))`(`tasks:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` ` [Callable](Callable.md)<T>!>!`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` <br /> |
| open [Future](Future.md)\<\*\>! | [submit](AbstractExecutorService.md))`(`task:` ` [Runnable](../java.lang/Runnable.md)!`)` <br /> |
| open [Future](Future.md)\<T\>! | [submit](AbstractExecutorService.md))`(`task:` ` [Runnable](../java.lang/Runnable.md)!`, `result:` `T`)` <br /> |
| --- | --- |
| open [Future](Future.md)\<T\>! | [submit](AbstractExecutorService.md))`(`task:` ` [Callable](Callable.md)<T>!`)` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [RunnableFuture](RunnableFuture.md)\<T\>! | [newTaskFor](AbstractExecutorService.md))`(`runnable:` ` [Runnable](../java.lang/Runnable.md)!`, `value:` `T`)` Returns a`RunnableFuture`for the given runnable and default value. |
| open [RunnableFuture](RunnableFuture.md)\<T\>! | [newTaskFor](AbstractExecutorService.md))`(`callable:` ` [Callable](Callable.md)<T>!`)` Returns a`RunnableFuture`for the given callable task. |

| Inherited functions ||
|---|---|
| From class [ExecutorService](ExecutorService.md) |------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [awaitTermination](ExecutorService.md))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` <br /> Blocks until all tasks have completed execution after a shutdown request, or the timeout occurs, or the current thread is interrupted, whichever happens first. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](ExecutorService.md))`()` <br /> Initiates an orderly shutdown in which previously submitted tasks are executed, but no new tasks will be accepted. This method waits until all tasks have completed execution and the executor has terminated. If interrupted while waiting, this method stops all executing tasks as if by invoking [shutdownNow()](ExecutorService.md)). It then continues to wait until all actively executing tasks have completed. Tasks that were awaiting execution are not executed. The interrupt status will be re-asserted before this method returns. If already terminated, invoking this method has no effect. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isShutdown](ExecutorService.md))`()` <br /> Returns`true`if this executor has been shut down. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTerminated](ExecutorService.md))`()` <br /> Returns`true`if all tasks have completed following shut down. Note that`isTerminated`is never`true`unless either`shutdown`or`shutdownNow`was called first. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [shutdown](ExecutorService.md))`()` <br /> Initiates an orderly shutdown in which previously submitted tasks are executed, but no new tasks will be accepted. Invocation has no additional effect if already shut down. This method does not wait for previously submitted tasks to complete execution. Use [awaitTermination](ExecutorService.md))to do that. <br /> | | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Runnable](../java.lang/Runnable.md)!>! | [shutdownNow](ExecutorService.md))`()` <br /> Attempts to stop all actively executing tasks, halts the processing of waiting tasks, and returns a list of the tasks that were awaiting execution. This method does not wait for actively executing tasks to terminate. Use [awaitTermination](ExecutorService.md))to do that. There are no guarantees beyond best-effort attempts to stop processing actively executing tasks. For example, typical implementations will cancel via [Thread.interrupt](../java.lang/Thread.md)), so any task that fails to respond to interrupts may never terminate. <br /> | ||
| From class [Executor](Executor.md) |------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [execute](Executor.md))`(`command:` ` [Runnable](../java.lang/Runnable.md)!`)` <br /> Executes the given command at some time in the future. The command may execute in a new thread, in a pooled thread, or in the calling thread, at the discretion of the`Executor`implementation. <br /> | ||

## Public constructors

### AbstractExecutorService

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AbstractExecutorService()
```

Constructor for subclasses to call.

## Public methods

### invokeAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Any!> invokeAll(tasks: MutableCollection<out Callable<T>!>!): MutableList<Future<T>!>!
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tasks` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<out [Callable](Callable.md)\<T\>!\>!:the collection of tasks |
| `<T>` | the type of the values returned from the tasks |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Future](Future.md)<T>!>! | a list of Futures representing the tasks, in the same sequential order as produced by the iterator for the given task list, each of which has completed |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting, in which case unfinished tasks are cancelled |
| `java.lang.NullPointerException` | if tasks or any of its elements are`null` |
| `java.util.concurrent.RejectedExecutionException` | if any task cannot be scheduled for execution |
| --- | --- |

### invokeAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Any!> invokeAll(
    tasks: MutableCollection<out Callable<T>!>!, 
    timeout: Long, 
    unit: TimeUnit!
): MutableList<Future<T>!>!
```

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tasks` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<out [Callable](Callable.md)\<T\>!\>!:the collection of tasks |
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the maximum time to wait |
| `unit` | [TimeUnit](TimeUnit.md)!:the time unit of the timeout argument |
| --- | --- |
| `<T>` | the type of the values returned from the tasks |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Future](Future.md)<T>!>! | a list of Futures representing the tasks, in the same sequential order as produced by the iterator for the given task list. If the operation did not time out, each task will have completed. If it did time out, some of these tasks will not have completed. |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting, in which case unfinished tasks are cancelled |
| `java.lang.NullPointerException` | if tasks, any of its elements, or unit are`null` |
| `java.util.concurrent.RejectedExecutionException` | if any task cannot be scheduled for execution |
| --- | --- |

### invokeAny

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Any!> invokeAny(tasks: MutableCollection<out Callable<T>!>!): T
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tasks` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<out [Callable](Callable.md)\<T\>!\>!:the collection of tasks |
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
open fun <T : Any!> invokeAny(
    tasks: MutableCollection<out Callable<T>!>!, 
    timeout: Long, 
    unit: TimeUnit!
): T
```

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tasks` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<out [Callable](Callable.md)\<T\>!\>!:the collection of tasks |
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the maximum time to wait |
| `unit` | [TimeUnit](TimeUnit.md)!:the time unit of the timeout argument |
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

### newTaskFor

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun <T : Any!> newTaskFor(
    runnable: Runnable!, 
    value: T
): RunnableFuture<T>!
```

Returns a`RunnableFuture`for the given runnable and default value.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------|
| `runnable` | [Runnable](../java.lang/Runnable.md)!:the runnable task being wrapped |
| `value` | T:the default value for the returned future |
| `<T>` | the type of the given value |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [RunnableFuture](RunnableFuture.md)<T>! | a`RunnableFuture`which, when run, will run the underlying runnable and which, as a`Future`, will yield the given value as its result and provide for cancellation of the underlying task |

### newTaskFor

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun <T : Any!> newTaskFor(callable: Callable<T>!): RunnableFuture<T>!
```

Returns a`RunnableFuture`for the given callable task.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------|
| `callable` | [Callable](Callable.md)\<T\>!:the callable task being wrapped |
| `<T>` | the type of the callable's result |

| Return ||
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [RunnableFuture](RunnableFuture.md)<T>! | a`RunnableFuture`which, when run, will call the underlying callable and which, as a`Future`, will yield the callable's result as its result and provide for cancellation of the underlying task |
