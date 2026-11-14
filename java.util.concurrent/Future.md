# Future

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Future

```
interface Future<V : Any!>
```

| [java.util.concurrent.Future](Future.md) |

| Known Direct Subclasses [CompletableFuture](CompletableFuture.md), [ForkJoinTask](ForkJoinTask.md), [RunnableFuture](RunnableFuture.md), [ScheduledFuture](ScheduledFuture.md) |------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CompletableFuture](CompletableFuture.md) | A [Future](Future.md) that may be explicitly completed (setting its value and status), and may be used as a [CompletionStage](CompletionStage.md), supporting dependent functions and actions that trigger upon its completion. | | [ForkJoinTask](ForkJoinTask.md) | Abstract base class for tasks that run within a [ForkJoinPool](ForkJoinPool.md). | | [RunnableFuture](RunnableFuture.md) | A [Future](Future.md) that is [Runnable](../java.lang/Runnable.md). | | [ScheduledFuture](ScheduledFuture.md) | A delayed result-bearing action that can be cancelled. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [CountedCompleter](CountedCompleter.md), [FutureTask](FutureTask.md), [RecursiveAction](RecursiveAction.md), [RecursiveTask](RecursiveTask.md), [RunnableScheduledFuture](RunnableScheduledFuture.md) [RunnableScheduledFuture](RunnableScheduledFuture.md) |------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CountedCompleter](CountedCompleter.md) | A [ForkJoinTask](ForkJoinTask.md) with a completion action performed when triggered and there are no remaining pending actions. | | [FutureTask](FutureTask.md) | A cancellable asynchronous computation. | | [RecursiveAction](RecursiveAction.md) | A recursive resultless [ForkJoinTask](ForkJoinTask.md). | | [RecursiveTask](RecursiveTask.md) | A recursive result-bearing [ForkJoinTask](ForkJoinTask.md). | | [RunnableScheduledFuture](RunnableScheduledFuture.md) | A [ScheduledFuture](ScheduledFuture.md) that is [Runnable](../java.lang/Runnable.md). | | [RunnableScheduledFuture](RunnableScheduledFuture.md) | A [ScheduledFuture](ScheduledFuture.md) that is [Runnable](../java.lang/Runnable.md). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A represents the result of an asynchronous computation. Methods are provided to check if the computation is complete, to wait for its completion, and to retrieve the result of the computation. The result can only be retrieved using method`get`when the computation has completed, blocking if necessary until it is ready. Cancellation is performed by the`cancel`method. Additional methods are provided to determine if the task completed normally or was cancelled. Once a computation has completed, the computation cannot be cancelled. If you would like to use a for the sake of cancellability but not provide a usable result, you can declare types of the form`Future<?>`and return`null`as a result of the underlying task.

**Sample Usage**(Note that the following classes are all made-up.) 

```kotlin
<code>interface ArchiveSearcher { String search(String target); }
  class App {
    ExecutorService executor = ...;
    ArchiveSearcher searcher = ...;
    void showSearch(String target) throws InterruptedException {
      Callable&lt;String&gt; task = () -&gt; searcher.search(target);
      Future&lt;String&gt; future = executor.submit(task);
      displayOtherThings(); // do other things while searching
      try {
        displayText(future.get()); // use future
      } catch (ExecutionException ex) { cleanup(); return; }
    }
  }</code>
```
The [FutureTask](FutureTask.md) class is an implementation of`Future`that implements`Runnable`, and so may be executed by an`Executor`. For example, the above construction with`submit`could be replaced by: 

```kotlin
<code>FutureTask&lt;String&gt; future = new FutureTask&lt;&gt;(task);
  executor.execute(future);</code>
```

Memory consistency effects: Actions taken by the asynchronous computation [*happen-before*](_package.md) actions following the corresponding`Future.get()`in another thread.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------|
| | [State](../java/util/concurrent/Future.State.md) Represents the computation state. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [cancel](Future.md))`(`mayInterruptIfRunning:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Attempts to cancel execution of this task. |
| open [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)! | [exceptionNow](Future.md))`()` Returns the exception thrown by the task, without waiting. |
| abstractV | [get](Future.md))`()` Waits if necessary for the computation to complete, and then retrieves its result. |
| --- | --- |
| abstractV | [get](Future.md))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` Waits if necessary for at most the given time for the computation to complete, and then retrieves its result, if available. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCancelled](Future.md))`()` Returns`true`if this task was cancelled before it completed normally. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDone](Future.md))`()` Returns`true`if this task completed. |
| --- | --- |
| openV | [resultNow](Future.md))`()` Returns the computed result, without waiting. |
| open [Future.State](../java/util/concurrent/Future.State.md)! | [state](Future.md))`()` {@return the computation state} |

## Public methods

### cancel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun cancel(mayInterruptIfRunning: Boolean): Boolean
```

Attempts to cancel execution of this task. This method has no effect if the task is already completed or cancelled, or could not be cancelled for some other reason. Otherwise, if this task has not started when`cancel`is called, this task should never run. If the task has already started, then the`mayInterruptIfRunning`parameter determines whether the thread executing this task (when known by the implementation) is interrupted in an attempt to stop the task.

The return value from this method does not necessarily indicate whether the task is now cancelled; use [isCancelled](Future.md)).

| Parameters ||
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mayInterruptIfRunning` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if the thread executing this task should be interrupted (if the thread is known to the implementation); otherwise, in-progress tasks are allowed to complete |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `false`if the task could not be cancelled, typically because it has already completed;`true`otherwise. If two or more threads cause a task to be cancelled, then at least one of them returns`true`. Implementations may provide stronger guarantees. |

### exceptionNow

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun exceptionNow(): Throwable!
```

Returns the exception thrown by the task, without waiting.

This method is for cases where the caller knows that the task has already completed with an exception.

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------------|
| [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)! | the exception thrown by the task |

| Exceptions ||
|-----------------------------------|---------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the task has not completed, the task completed normally, or the task was cancelled |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun get(): V
```

Waits if necessary for the computation to complete, and then retrieves its result.

| Return ||
|---|---------------------|
| V | the computed result |

| Exceptions ||
|----------------------------------------------|-----------------------------------------------------|
| `java.util.concurrent.CancellationException` | if the computation was cancelled |
| `java.util.concurrent.ExecutionException` | if the computation threw an exception |
| `java.lang.InterruptedException` | if the current thread was interrupted while waiting |
| --- | --- |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun get(
    timeout: Long, 
    unit: TimeUnit!
): V
```

Waits if necessary for at most the given time for the computation to complete, and then retrieves its result, if available.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the maximum time to wait |
| `unit` | [TimeUnit](TimeUnit.md)!:the time unit of the timeout argument |

| Return ||
|---|---------------------|
| V | the computed result |

| Exceptions ||
|----------------------------------------------|-----------------------------------------------------|
| `java.util.concurrent.CancellationException` | if the computation was cancelled |
| `java.util.concurrent.ExecutionException` | if the computation threw an exception |
| `java.lang.InterruptedException` | if the current thread was interrupted while waiting |
| --- | --- |
| `java.util.concurrent.TimeoutException` | if the wait timed out |

### isCancelled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isCancelled(): Boolean
```

Returns`true`if this task was cancelled before it completed normally.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this task was cancelled before it completed |

### isDone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isDone(): Boolean
```

Returns`true`if this task completed. Completion may be due to normal termination, an exception, or cancellation -- in all of these cases, this method will return`true`.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this task completed |

### resultNow

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun resultNow(): V
```

Returns the computed result, without waiting.

This method is for cases where the caller knows that the task has already completed successfully, for example when filtering a stream of Future objects for the successful tasks and using a mapping operation to obtain a stream of results. {@snippet lang=java : \* results = futures.stream() \* .filter(f -\> f.state() == Future.State.SUCCESS) \* .map(Future::resultNow) \* .toList(); \* }

| Return ||
|---|---------------------|
| V | the computed result |

| Exceptions ||
|-----------------------------------|--------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the task has not completed or the task did not complete with a result |

### state

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun state(): Future.State!
```

{@return the computation state}
