# CompletionService

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CompletionService

```
interface CompletionService<V : Any!>
```

| [java.util.concurrent.CompletionService](https://developer.android.com/reference/kotlin/java/util/concurrent/CompletionService#) |

| Known Direct Subclasses [ExecutorCompletionService](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorCompletionService) |----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ExecutorCompletionService](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorCompletionService) | A [CompletionService](https://developer.android.com/reference/kotlin/java/util/concurrent/CompletionService#) that uses a supplied [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor) to execute tasks. | |
| --- | --- | --- | --- | --- | --- | --- |

A service that decouples the production of new asynchronous tasks from the consumption of the results of completed tasks. Producers`submit`tasks for execution. Consumers`take`completed tasks and process their results in the order they complete. A`CompletionService`can for example be used to manage asynchronous I/O, in which tasks that perform reads are submitted in one part of a program or system, and then acted upon in a different part of the program when the reads complete, possibly in a different order than they were requested.

Typically, a`CompletionService`relies on a separate [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor) to actually execute the tasks, in which case the`CompletionService`only manages an internal completion queue. The [ExecutorCompletionService](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorCompletionService) class provides an implementation of this approach.

Memory consistency effects: Actions in a thread prior to submitting a task to a`CompletionService` [*happen-before*](https://developer.android.com/reference/kotlin/java/util/concurrent/package-summary#MemoryVisibility) actions taken by that task, which in turn*happen-before* actions following a successful return from the corresponding`take()`.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)\<V\>! | [poll](https://developer.android.com/reference/kotlin/java/util/concurrent/CompletionService#poll())`()` Retrieves and removes the Future representing the next completed task, or`null`if none are present. |
| abstract [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)\<V\>! | [poll](https://developer.android.com/reference/kotlin/java/util/concurrent/CompletionService#poll(kotlin.Long,%20java.util.concurrent.TimeUnit))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` Retrieves and removes the Future representing the next completed task, waiting if necessary up to the specified wait time if none are yet present. |
| abstract [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)\<V\>! | [submit](https://developer.android.com/reference/kotlin/java/util/concurrent/CompletionService#submit(java.lang.Runnable,%20java.util.concurrent.CompletionService.V))`(`task:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`, `result:` `V`)` Submits a Runnable task for execution and returns a Future representing that task. |
| --- | --- |
| abstract [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)\<V\>! | [submit](https://developer.android.com/reference/kotlin/java/util/concurrent/CompletionService#submit(java.util.concurrent.Callable))`(`task:` ` [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable)<V>!`)` Submits a value-returning task for execution and returns a Future representing the pending results of the task. |
| abstract [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)\<V\>! | [take](https://developer.android.com/reference/kotlin/java/util/concurrent/CompletionService#take())`()` Retrieves and removes the Future representing the next completed task, waiting if none are yet present. |

## Public methods

### poll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun poll(): Future<V>!
```

Retrieves and removes the Future representing the next completed task, or`null`if none are present.

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)<V>! | the Future representing the next completed task, or`null`if none are present |

### poll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun poll(
    timeout: Long, 
    unit: TimeUnit!
): Future<V>!
```

Retrieves and removes the Future representing the next completed task, waiting if necessary up to the specified wait time if none are yet present.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):how long to wait before giving up, in units of`unit` |
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!:a`TimeUnit`determining how to interpret the`timeout`parameter |

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)<V>! | the Future representing the next completed task or`null`if the specified waiting time elapses before one is present |

| Exceptions ||
|----------------------------------|------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |

### submit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun submit(
    task: Runnable!, 
    result: V
): Future<V>!
```

Submits a Runnable task for execution and returns a Future representing that task. Upon completion, this task may be taken or polled.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------|
| `task` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!:the task to submit |
| `result` | V:the result to return upon successful completion |

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)<V>! | a Future representing pending completion of the task, and whose`get()`method will return the given result value upon completion |

| Exceptions ||
|---------------------------------------------------|-----------------------------------------------|
| `java.util.concurrent.RejectedExecutionException` | if the task cannot be scheduled for execution |
| `java.lang.NullPointerException` | if the task is null |

### submit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun submit(task: Callable<V>!): Future<V>!
```

Submits a value-returning task for execution and returns a Future representing the pending results of the task. Upon completion, this task may be taken or polled.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------|
| `task` | [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable)\<V\>!:the task to submit |

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------------|
| [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)<V>! | a Future representing pending completion of the task |

| Exceptions ||
|---------------------------------------------------|-----------------------------------------------|
| `java.util.concurrent.RejectedExecutionException` | if the task cannot be scheduled for execution |
| `java.lang.NullPointerException` | if the task is null |

### take

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun take(): Future<V>!
```

Retrieves and removes the Future representing the next completed task, waiting if none are yet present.

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------|
| [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)<V>! | the Future representing the next completed task |

| Exceptions ||
|----------------------------------|------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |
