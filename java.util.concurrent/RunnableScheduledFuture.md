# RunnableScheduledFuture

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RunnableScheduledFuture

```
interface RunnableScheduledFuture<V : Any!> : RunnableFuture<V>, ScheduledFuture<V>
```

| [java.util.concurrent.RunnableScheduledFuture](RunnableScheduledFuture.md) |

A [ScheduledFuture](ScheduledFuture.md) that is [Runnable](../java.lang/Runnable.md). Successful execution of the`run`method causes completion of the`Future`and allows access to its results.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPeriodic](RunnableScheduledFuture.md))`()` Returns`true`if this task is periodic. |

| Inherited functions ||
|---|---|
| From class [Future](Future.md) |---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [cancel](Future.md))`(`mayInterruptIfRunning:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Attempts to cancel execution of this task. This method has no effect if the task is already completed or cancelled, or could not be cancelled for some other reason. Otherwise, if this task has not started when`cancel`is called, this task should never run. If the task has already started, then the`mayInterruptIfRunning`parameter determines whether the thread executing this task (when known by the implementation) is interrupted in an attempt to stop the task. The return value from this method does not necessarily indicate whether the task is now cancelled; use [isCancelled](Future.md)). <br /> | | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)! | [exceptionNow](Future.md))`()` <br /> Returns the exception thrown by the task, without waiting. This method is for cases where the caller knows that the task has already completed with an exception. <br /> | | V | [get](Future.md))`()` <br /> Waits if necessary for the computation to complete, and then retrieves its result. <br /> | | V | [get](Future.md))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` <br /> Waits if necessary for at most the given time for the computation to complete, and then retrieves its result, if available. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCancelled](Future.md))`()` <br /> Returns`true`if this task was cancelled before it completed normally. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDone](Future.md))`()` <br /> Returns`true`if this task completed. Completion may be due to normal termination, an exception, or cancellation -- in all of these cases, this method will return`true`. <br /> | | V | [resultNow](Future.md))`()` <br /> Returns the computed result, without waiting. This method is for cases where the caller knows that the task has already completed successfully, for example when filtering a stream of Future objects for the successful tasks and using a mapping operation to obtain a stream of results. {@snippet lang=java : \* results = futures.stream() \* .filter(f -\> f.state() == Future.State.SUCCESS) \* .map(Future::resultNow) \* .toList(); \* } <br /> | | [Future.State](../java/util/concurrent/Future.State.md)! | [state](Future.md))`()` <br /> {@return the computation state} <br /> | ||
| From class [RunnableFuture](RunnableFuture.md) |------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [run](RunnableFuture.md))`()` <br /> Sets this Future to the result of its computation unless it has been cancelled. <br /> | ||

## Public methods

### isPeriodic

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isPeriodic(): Boolean
```

Returns`true`if this task is periodic. A periodic task may re-run according to some schedule. A non-periodic task can be run only once.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this task is periodic |
