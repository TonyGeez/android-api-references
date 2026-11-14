# FutureTask

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FutureTask

```
open class FutureTask<V : Any!> : RunnableFuture<V>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.concurrent.FutureTask](https://developer.android.com/reference/kotlin/java/util/concurrent/FutureTask#) |

A cancellable asynchronous computation. This class provides a base implementation of [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future), with methods to start and cancel a computation, query to see if the computation is complete, and retrieve the result of the computation. The result can only be retrieved when the computation has completed; the`get`methods will block if the computation has not yet completed. Once the computation has completed, the computation cannot be restarted or cancelled (unless the computation is invoked using [runAndReset](https://developer.android.com/reference/kotlin/java/util/concurrent/FutureTask#runAndReset())).

A`FutureTask`can be used to wrap a [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable) or [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#) object. Because`FutureTask`implements`Runnable`, a`FutureTask`can be submitted to an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor) for execution.

In addition to serving as a standalone class, this class provides`protected`functionality that may be useful when creating customized task classes.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FutureTask](https://developer.android.com/reference/kotlin/java/util/concurrent/FutureTask#FutureTask(java.lang.Runnable,%20java.util.concurrent.FutureTask.V))`(`runnable:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`, `result:` `V`)` Creates a`FutureTask`that will, upon running, execute the given`Runnable`, and arrange that`get`will return the given result on successful completion. |
| [FutureTask](https://developer.android.com/reference/kotlin/java/util/concurrent/FutureTask#FutureTask(java.util.concurrent.Callable))`(`callable:` ` [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable)<V>!`)` Creates a`FutureTask`that will, upon running, execute the given`Callable`. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [cancel](https://developer.android.com/reference/kotlin/java/util/concurrent/FutureTask#cancel(kotlin.Boolean))`(`mayInterruptIfRunning:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| open [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)! | [exceptionNow](https://developer.android.com/reference/kotlin/java/util/concurrent/FutureTask#exceptionNow())`()` <br /> |
| openV | [get](https://developer.android.com/reference/kotlin/java/util/concurrent/FutureTask#get())`()` <br /> |
| --- | --- |
| openV | [get](https://developer.android.com/reference/kotlin/java/util/concurrent/FutureTask#get(kotlin.Long,%20java.util.concurrent.TimeUnit))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCancelled](https://developer.android.com/reference/kotlin/java/util/concurrent/FutureTask#isCancelled())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDone](https://developer.android.com/reference/kotlin/java/util/concurrent/FutureTask#isDone())`()` <br /> |
| --- | --- |
| openV | [resultNow](https://developer.android.com/reference/kotlin/java/util/concurrent/FutureTask#resultNow())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [run](https://developer.android.com/reference/kotlin/java/util/concurrent/FutureTask#run())`()` <br /> |
| open [Future.State](https://developer.android.com/reference/kotlin/java/util/concurrent/Future.State)! | [state](https://developer.android.com/reference/kotlin/java/util/concurrent/FutureTask#state())`()` <br /> |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/concurrent/FutureTask#toString())`()` Returns a string representation of this FutureTask. |

| Protected methods ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [done](https://developer.android.com/reference/kotlin/java/util/concurrent/FutureTask#done())`()` Protected method invoked when this task transitions to state`isDone`(whether normally or via cancellation). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [runAndReset](https://developer.android.com/reference/kotlin/java/util/concurrent/FutureTask#runAndReset())`()` Executes the computation without setting its result, and then resets this future to initial state, failing to do so if the computation encounters an exception or is cancelled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](https://developer.android.com/reference/kotlin/java/util/concurrent/FutureTask#set(java.util.concurrent.FutureTask.V))`(`v:` `V`)` Sets the result of this future to the given value unless this future has already been set or has been cancelled. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setException](https://developer.android.com/reference/kotlin/java/util/concurrent/FutureTask#setException(kotlin.Throwable))`(`t:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Causes this future to report an [ExecutionException](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutionException) with the given throwable as its cause, unless this future has already been set or has been cancelled. |

## Public constructors

### FutureTask

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FutureTask(
    runnable: Runnable!, 
    result: V)
```

Creates a`FutureTask`that will, upon running, execute the given`Runnable`, and arrange that`get`will return the given result on successful completion.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `runnable` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!:the runnable task |
| `result` | V:the result to return on successful completion. If you don't need a particular result, consider using constructions of the form:`Future<?> f = new FutureTask<Void>(runnable, null)` |

| Exceptions ||
|----------------------------------|-------------------------|
| `java.lang.NullPointerException` | if the runnable is null |

### FutureTask

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FutureTask(callable: Callable<V>!)
```

Creates a`FutureTask`that will, upon running, execute the given`Callable`.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------|
| `callable` | [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable)\<V\>!:the callable task |

| Exceptions ||
|----------------------------------|-------------------------|
| `java.lang.NullPointerException` | if the callable is null |

## Public methods

### cancel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun cancel(mayInterruptIfRunning: Boolean): Boolean
```

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

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------------|
| [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)! | the exception thrown by the task |

| Exceptions ||
|-----------------------------------|---------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the task has not completed, the task completed normally, or the task was cancelled |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(): V
```

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
open fun get(
    timeout: Long, 
    unit: TimeUnit!
): V
```

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the maximum time to wait |
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!:the time unit of the timeout argument |

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
open fun isCancelled(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this task was cancelled before it completed |

### isDone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isDone(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this task completed |

### resultNow

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun resultNow(): V
```

| Return ||
|---|---------------------|
| V | the computed result |

| Exceptions ||
|-----------------------------------|--------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the task has not completed or the task did not complete with a result |

### run

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun run(): Unit
```  

### state

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun state(): Future.State!
```  

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string representation of this FutureTask.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of this FutureTask |

## Protected methods

### done

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun done(): Unit
```

Protected method invoked when this task transitions to state`isDone`(whether normally or via cancellation). The default implementation does nothing. Subclasses may override this method to invoke completion callbacks or perform bookkeeping. Note that you can query status inside the implementation of this method to determine whether this task has been cancelled. 

### runAndReset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun runAndReset(): Boolean
```

Executes the computation without setting its result, and then resets this future to initial state, failing to do so if the computation encounters an exception or is cancelled. This is designed for use with tasks that intrinsically execute more than once.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successfully run and reset |

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun set(v: V): Unit
```

Sets the result of this future to the given value unless this future has already been set or has been cancelled.

This method is invoked internally by the #run method upon successful completion of the computation.

| Parameters ||
|-----|-------------|
| `v` | V:the value |

### setException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun setException(t: Throwable!): Unit
```

Causes this future to report an [ExecutionException](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutionException) with the given throwable as its cause, unless this future has already been set or has been cancelled.

This method is invoked internally by the #run method upon failure of the computation.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------|
| `t` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause of failure |
