# RunnableFuture

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RunnableFuture

```
interface RunnableFuture<V : Any!> : Future<V>, Runnable
```

| [java.util.concurrent.RunnableFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/RunnableFuture#) |

| Known Direct Subclasses [FutureTask](https://developer.android.com/reference/kotlin/java/util/concurrent/FutureTask), [RunnableScheduledFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/RunnableScheduledFuture) |------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [FutureTask](https://developer.android.com/reference/kotlin/java/util/concurrent/FutureTask) | A cancellable asynchronous computation. | | [RunnableScheduledFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/RunnableScheduledFuture) | A [ScheduledFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledFuture) that is [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future) that is [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#). Successful execution of the`run`method causes completion of the`Future`and allows access to its results.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [run](https://developer.android.com/reference/kotlin/java/util/concurrent/RunnableFuture#run())`()` Sets this Future to the result of its computation unless it has been cancelled. |

| Inherited functions ||
|---|---|
| From class [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future) |---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [cancel](https://developer.android.com/reference/kotlin/java/util/concurrent/Future#cancel(kotlin.Boolean))`(`mayInterruptIfRunning:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Attempts to cancel execution of this task. This method has no effect if the task is already completed or cancelled, or could not be cancelled for some other reason. Otherwise, if this task has not started when`cancel`is called, this task should never run. If the task has already started, then the`mayInterruptIfRunning`parameter determines whether the thread executing this task (when known by the implementation) is interrupted in an attempt to stop the task. The return value from this method does not necessarily indicate whether the task is now cancelled; use [isCancelled](https://developer.android.com/reference/kotlin/java/util/concurrent/Future#isCancelled()). <br /> | | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)! | [exceptionNow](https://developer.android.com/reference/kotlin/java/util/concurrent/Future#exceptionNow())`()` <br /> Returns the exception thrown by the task, without waiting. This method is for cases where the caller knows that the task has already completed with an exception. <br /> | | V | [get](https://developer.android.com/reference/kotlin/java/util/concurrent/Future#get())`()` <br /> Waits if necessary for the computation to complete, and then retrieves its result. <br /> | | V | [get](https://developer.android.com/reference/kotlin/java/util/concurrent/Future#get(kotlin.Long,%20java.util.concurrent.TimeUnit))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` <br /> Waits if necessary for at most the given time for the computation to complete, and then retrieves its result, if available. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCancelled](https://developer.android.com/reference/kotlin/java/util/concurrent/Future#isCancelled())`()` <br /> Returns`true`if this task was cancelled before it completed normally. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDone](https://developer.android.com/reference/kotlin/java/util/concurrent/Future#isDone())`()` <br /> Returns`true`if this task completed. Completion may be due to normal termination, an exception, or cancellation -- in all of these cases, this method will return`true`. <br /> | | V | [resultNow](https://developer.android.com/reference/kotlin/java/util/concurrent/Future#resultNow())`()` <br /> Returns the computed result, without waiting. This method is for cases where the caller knows that the task has already completed successfully, for example when filtering a stream of Future objects for the successful tasks and using a mapping operation to obtain a stream of results. {@snippet lang=java : \* results = futures.stream() \* .filter(f -\> f.state() == Future.State.SUCCESS) \* .map(Future::resultNow) \* .toList(); \* } <br /> | | [Future.State](https://developer.android.com/reference/kotlin/java/util/concurrent/Future.State)! | [state](https://developer.android.com/reference/kotlin/java/util/concurrent/Future#state())`()` <br /> {@return the computation state} <br /> | ||

## Public methods

### run

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun run(): Unit
```

Sets this Future to the result of its computation unless it has been cancelled.
