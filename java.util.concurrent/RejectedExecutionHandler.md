# RejectedExecutionHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RejectedExecutionHandler

```
interface RejectedExecutionHandler
```

| [java.util.concurrent.RejectedExecutionHandler](RejectedExecutionHandler.md) |

| Known Direct Subclasses [ThreadPoolExecutor.AbortPolicy](../java/util/concurrent/ThreadPoolExecutor.AbortPolicy.md), [ThreadPoolExecutor.CallerRunsPolicy](../java/util/concurrent/ThreadPoolExecutor.CallerRunsPolicy.md), [ThreadPoolExecutor.DiscardOldestPolicy](../java/util/concurrent/ThreadPoolExecutor.DiscardOldestPolicy.md), [ThreadPoolExecutor.DiscardPolicy](../java/util/concurrent/ThreadPoolExecutor.DiscardPolicy.md) |------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ThreadPoolExecutor.AbortPolicy](../java/util/concurrent/ThreadPoolExecutor.AbortPolicy.md) | A handler for rejected tasks that throws a [RejectedExecutionException](RejectedExecutionException.md). | | [ThreadPoolExecutor.CallerRunsPolicy](../java/util/concurrent/ThreadPoolExecutor.CallerRunsPolicy.md) | A handler for rejected tasks that runs the rejected task directly in the calling thread of the`execute`method, unless the executor has been shut down, in which case the task is discarded. | | [ThreadPoolExecutor.DiscardOldestPolicy](../java/util/concurrent/ThreadPoolExecutor.DiscardOldestPolicy.md) | A handler for rejected tasks that discards the oldest unhandled request and then retries`execute`, unless the executor is shut down, in which case the task is discarded. | | [ThreadPoolExecutor.DiscardPolicy](../java/util/concurrent/ThreadPoolExecutor.DiscardPolicy.md) | A handler for rejected tasks that silently discards the rejected task. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A handler for tasks that cannot be executed by a [ThreadPoolExecutor](ThreadPoolExecutor.md).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [rejectedExecution](RejectedExecutionHandler.md))`(`r:` ` [Runnable](../java.lang/Runnable.md)!`, `executor:` ` [ThreadPoolExecutor](ThreadPoolExecutor.md)!`)` Method that may be invoked by a [ThreadPoolExecutor](ThreadPoolExecutor.md) when [execute](ThreadPoolExecutor.md))cannot accept a task. |

## Public methods

### rejectedExecution

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun rejectedExecution(
    r: Runnable!, 
    executor: ThreadPoolExecutor!
): Unit
```

Method that may be invoked by a [ThreadPoolExecutor](ThreadPoolExecutor.md) when [execute](ThreadPoolExecutor.md))cannot accept a task. This may occur when no more threads or queue slots are available because their bounds would be exceeded, or upon shutdown of the Executor.

In the absence of other alternatives, the method may throw an unchecked [RejectedExecutionException](RejectedExecutionException.md), which will be propagated to the caller of`execute`.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `r` | [Runnable](../java.lang/Runnable.md)!:the runnable task requested to be executed |
| `executor` | [ThreadPoolExecutor](ThreadPoolExecutor.md)!:the executor attempting to execute this task |

| Exceptions ||
|---------------------------------------------------|-----------------------|
| `java.util.concurrent.RejectedExecutionException` | if there is no remedy |
