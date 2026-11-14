# RejectedExecutionHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RejectedExecutionHandler

```
interface RejectedExecutionHandler
```

| [java.util.concurrent.RejectedExecutionHandler](https://developer.android.com/reference/kotlin/java/util/concurrent/RejectedExecutionHandler#) |

| Known Direct Subclasses [ThreadPoolExecutor.AbortPolicy](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor.AbortPolicy), [ThreadPoolExecutor.CallerRunsPolicy](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor.CallerRunsPolicy), [ThreadPoolExecutor.DiscardOldestPolicy](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor.DiscardOldestPolicy), [ThreadPoolExecutor.DiscardPolicy](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor.DiscardPolicy) |------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ThreadPoolExecutor.AbortPolicy](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor.AbortPolicy) | A handler for rejected tasks that throws a [RejectedExecutionException](https://developer.android.com/reference/kotlin/java/util/concurrent/RejectedExecutionException). | | [ThreadPoolExecutor.CallerRunsPolicy](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor.CallerRunsPolicy) | A handler for rejected tasks that runs the rejected task directly in the calling thread of the`execute`method, unless the executor has been shut down, in which case the task is discarded. | | [ThreadPoolExecutor.DiscardOldestPolicy](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor.DiscardOldestPolicy) | A handler for rejected tasks that discards the oldest unhandled request and then retries`execute`, unless the executor is shut down, in which case the task is discarded. | | [ThreadPoolExecutor.DiscardPolicy](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor.DiscardPolicy) | A handler for rejected tasks that silently discards the rejected task. | |

A handler for tasks that cannot be executed by a [ThreadPoolExecutor](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [rejectedExecution](https://developer.android.com/reference/kotlin/java/util/concurrent/RejectedExecutionHandler#rejectedExecution(java.lang.Runnable,%20java.util.concurrent.ThreadPoolExecutor))`(`r:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`, `executor:` ` [ThreadPoolExecutor](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor)!`)` Method that may be invoked by a [ThreadPoolExecutor](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor) when [execute](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#execute(java.lang.Runnable))cannot accept a task. |

## Public methods

### rejectedExecution

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun rejectedExecution(
    r: Runnable!, 
    executor: ThreadPoolExecutor!
): Unit
```

Method that may be invoked by a [ThreadPoolExecutor](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor) when [execute](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor#execute(java.lang.Runnable))cannot accept a task. This may occur when no more threads or queue slots are available because their bounds would be exceeded, or upon shutdown of the Executor.

In the absence of other alternatives, the method may throw an unchecked [RejectedExecutionException](https://developer.android.com/reference/kotlin/java/util/concurrent/RejectedExecutionException), which will be propagated to the caller of`execute`.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `r` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!:the runnable task requested to be executed |
| `executor` | [ThreadPoolExecutor](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor)!:the executor attempting to execute this task |

| Exceptions ||
|---------------------------------------------------|-----------------------|
| `java.util.concurrent.RejectedExecutionException` | if there is no remedy |
