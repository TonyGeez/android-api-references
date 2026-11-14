Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RecursiveTask

```
abstract class RecursiveTask<V : Any!> : ForkJoinTask<V>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.concurrent.ForkJoinTask](ForkJoinTask.md)\<V\> ||
| | ↳ | [java.util.concurrent.RecursiveTask](RecursiveTask.md) |

A recursive result-bearing ForkJoinTask.

For example, here is a task-based program for computing Factorials:

```kotlin
<code>import java.util.concurrent.RecursiveTask;
  import java.math.BigInteger;
  public class Factorial {
    static class FactorialTask extends RecursiveTask&lt;BigInteger&gt; {
      private final int from, to;
      FactorialTask(int from, int to) { this.from = from; this.to = to; }
      protected BigInteger compute() {
        int range = to - from;
        if (range == 0) {                       // base case
          return BigInteger.valueOf(from);
        } else if (range == 1) {                // too small to parallelize
          return BigInteger.valueOf(from).multiply(BigInteger.valueOf(to));
        } else {                                // split in half
          int mid = from + range / 2;
          FactorialTask leftTask = new FactorialTask(from, mid);
          leftTask.fork();         // perform about half the work locally
          return new FactorialTask(mid + 1, to).compute()
                 .multiply(leftTask.join());
        }
      }
    }
    static BigInteger factorial(int n) { // uses ForkJoinPool.commonPool()
      return (n &lt;= 1) ? BigInteger.ONE : new FactorialTask(1, n).invoke();
    }
    public static void main(String[] args) {
      System.out.println(factorial(Integer.parseInt(args[0])));
    }
  }</code>
```

## Summary

| Public constructors ||
|---|---|
| RecursiveTask Constructor for subclasses to call. |

| Public methods ||
|---|---|
| V | getRawResult Returns the result that would be returned by join, even if this task completed abnormally, or `null` if this task is not known to have been completed. |

| Protected methods ||
|---|---|
| abstract V | compute The main computation performed by this task. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | exec Implements execution conventions for RecursiveTask. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setRawResult Forces the given value to be returned as a result. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class ForkJoinTask |---|---| | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask<*>!` | adapt Returns a new `ForkJoinTask` that performs the `run` method of the given `Runnable` as its action, and returns a null result upon join. <br /> | | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask<T>!` | adapt Returns a new `ForkJoinTask` that performs the `run` method of the given `Runnable` as its action, and returns the given result upon join. <br /> | | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask<T>!` | adapt Returns a new `ForkJoinTask` that performs the `call` method of the given `Callable` as its action, and returns its result upon join, translating any checked exceptions encountered into `RuntimeException`. <br /> | | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask<T>!` | adaptInterruptible Returns a new `ForkJoinTask` that performs the `call` method of the given `Callable` as its action, and returns its result upon join, translating any checked exceptions encountered into `RuntimeException`. Additionally, invocations of `cancel` with `mayInterruptIfRunning true` will attempt to interrupt the thread performing the task. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | cancel Attempts to cancel execution of this task. This attempt will fail if the task has already completed or could not be cancelled for some other reason. If successful, and this task has not started when `cancel` is called, execution of this task is suppressed. After this method returns successfully, unless there is an intervening call to reinitialize, subsequent calls to isCancelled, isDone, and `cancel` will return `true` and calls to join and related methods will result in `CancellationException`. This method may be overridden in subclasses, but if so, must still ensure that these properties hold. In particular, the `cancel` method itself must not throw exceptions. This method is designed to be invoked by *other* tasks. To terminate the current task, you can just return or throw an unchecked exception from its computation method, or invoke completeExceptionally. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | compareAndSetForkJoinTaskTag Atomically conditionally sets the tag value for this task. Among other applications, tags can be used as visit markers in tasks operating on graphs, as in methods that check: `if (task.compareAndSetForkJoinTaskTag((short)0, (short)1))` before processing, otherwise exiting because the node has already been visited. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | complete Completes this task, and if not already aborted or cancelled, returning the given value as the result of subsequent invocations of `join` and related operations. This method may be used to provide results for asynchronous tasks, or to provide alternative handling for tasks that would not otherwise complete normally. Its use in other situations is discouraged. This method is overridable, but overridden versions must invoke `super` implementation to maintain guarantees. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | completeExceptionally Completes this task abnormally, and if not already aborted or cancelled, causes it to throw the given exception upon `join` and related operations. This method may be used to induce exceptions in asynchronous tasks, or to force completion of tasks that would not otherwise complete. Its use in other situations is discouraged. This method is overridable, but overridden versions must invoke `super` implementation to maintain guarantees. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html!` | exceptionNow Returns the exception thrown by the task, without waiting. This method is for cases where the caller knows that the task has already completed with an exception. <br /> | | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask<V>!` | fork Arranges to asynchronously execute this task in the pool the current task is running in, if applicable, or using the commonPool if not inForkJoinPool. While it is not necessarily enforced, it is a usage error to fork a task more than once unless it has completed and been reinitialized. Subsequent modifications to the state of this task or any data it operates on are not necessarily consistently observable by any thread other than the one executing it unless preceded by a call to join or related methods, or a call to isDone returning `true`. <br /> | | `V` | get Waits if necessary for the computation to complete, and then retrieves its result. <br /> | | `V` | get Waits if necessary for at most the given time for the computation to complete, and then retrieves its result, if available. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html!` | getException Returns the exception thrown by the base computation, or a `CancellationException` if cancelled, or `null` if none or if the method has not yet completed. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | getForkJoinTaskTag Returns the tag for this task. <br /> | | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool!` | getPool Returns the pool hosting the current thread, or `null` if the current thread is executing outside of any ForkJoinPool. This method returns `null` if and only if inForkJoinPool returns `false`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getQueuedTaskCount Returns an estimate of the number of tasks that have been forked by the current worker thread but not yet executed. This value may be useful for heuristic decisions about whether to fork other tasks. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getSurplusQueuedTaskCount Returns an estimate of how many more locally queued tasks are held by the current worker thread than there are other worker threads that might steal them, or zero if this thread is not operating in a ForkJoinPool. This value may be useful for heuristic decisions about whether to fork other tasks. In many usages of ForkJoinTasks, at steady state, each worker should aim to maintain a small constant surplus (for example, 3) of tasks, and to process computations locally if this threshold is exceeded. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | helpQuiesce Possibly executes tasks until the pool hosting the current task [is quiescent](ForkJoinPool.md)). This method may be of use in designs in which many tasks are forked, but none are explicitly joined, instead executing them until all are processed. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | inForkJoinPool Returns `true` if the current thread is a ForkJoinWorkerThread executing as a ForkJoinPool computation. <br /> | | `V` | invoke Commences performing this task, awaits its completion if necessary, and returns its result, or throws an (unchecked) `RuntimeException` or `Error` if the underlying computation did so. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<T>!` | invokeAll Forks all tasks in the specified collection, returning when `isDone` holds for each task or an (unchecked) exception is encountered, in which case the exception is rethrown. If more than one task encounters an exception, then this method throws any one of these exceptions. If any task encounters an exception, others may be cancelled. However, the execution status of individual tasks is not guaranteed upon exceptional return. The status of each task may be obtained using getException and related methods to check if they have been cancelled, completed normally or exceptionally, or left unprocessed. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | invokeAll Forks the given tasks, returning when `isDone` holds for each task or an (unchecked) exception is encountered, in which case the exception is rethrown. If more than one task encounters an exception, then this method throws any one of these exceptions. If any task encounters an exception, the other may be cancelled. However, the execution status of individual tasks is not guaranteed upon exceptional return. The status of each task may be obtained using getException and related methods to check if they have been cancelled, completed normally or exceptionally, or left unprocessed. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | invokeAll Forks the given tasks, returning when `isDone` holds for each task or an (unchecked) exception is encountered, in which case the exception is rethrown. If more than one task encounters an exception, then this method throws any one of these exceptions. If any task encounters an exception, others may be cancelled. However, the execution status of individual tasks is not guaranteed upon exceptional return. The status of each task may be obtained using getException and related methods to check if they have been cancelled, completed normally or exceptionally, or left unprocessed. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isCancelled Returns `true` if this task was cancelled before it completed normally. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isCompletedAbnormally Returns `true` if this task threw an exception or was cancelled. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isCompletedNormally Returns `true` if this task completed without throwing an exception and was not cancelled. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isDone Returns `true` if this task completed. Completion may be due to normal termination, an exception, or cancellation -- in all of these cases, this method will return `true`. <br /> | | `V` | join Returns the result of the computation when it [is done](ForkJoinTask.md)). This method differs from get in that abnormal completion results in `RuntimeException` or `Error`, not `ExecutionException`, and that interrupts of the calling thread do *not* cause the method to abruptly return by throwing `InterruptedException`. <br /> | | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask<*>!` | peekNextLocalTask Returns, but does not unschedule or execute, a task queued by the current thread but not yet executed, if one is immediately available. There is no guarantee that this task will actually be polled or executed next. Conversely, this method may return null even if a task exists but cannot be accessed without contention with other threads. This method is designed primarily to support extensions, and is unlikely to be useful otherwise. <br /> | | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask<*>!` | pollNextLocalTask Unschedules and returns, without executing, the next task queued by the current thread but not yet executed, if the current thread is operating in a ForkJoinPool. This method is designed primarily to support extensions, and is unlikely to be useful otherwise. <br /> | | `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask<*>!` | pollTask If the current thread is operating in a ForkJoinPool, unschedules and returns, without executing, the next task queued by the current thread but not yet executed, if one is available, or if not available, a task that was forked by some other thread, if available. Availability may be transient, so a `null` result does not necessarily imply quiescence of the pool this task is operating in. This method is designed primarily to support extensions, and is unlikely to be useful otherwise. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | quietlyComplete Completes this task normally without setting a value. The most recent value established by setRawResult (or `null` by default) will be returned as the result of subsequent invocations of `join` and related operations. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | quietlyInvoke Commences performing this task and awaits its completion if necessary, without returning its result or throwing its exception. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | quietlyJoin Joins this task, without returning its result or throwing its exception. This method may be useful when processing collections of tasks when some have been cancelled or otherwise known to have aborted. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | quietlyJoin Tries to join this task, returning true if it completed (possibly exceptionally) before the given timeout and the current thread has not been interrupted. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | quietlyJoinUninterruptibly Tries to join this task, returning true if it completed (possibly exceptionally) before the given timeout. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | reinitialize Resets the internal bookkeeping state of this task, allowing a subsequent `fork`. This method allows repeated reuse of this task, but only if reuse occurs when this task has either never been forked, or has been forked, then completed and all outstanding joins of this task have also completed. Effects under any other usage conditions are not guaranteed. This method may be useful when executing pre-constructed trees of subtasks in loops. Upon completion of this method, `isDone()` reports `false`, and `getException()` reports `null`. However, the value returned by `getRawResult` is unaffected. To clear this value, you can invoke `setRawResult(null)`. <br /> | | `V` | resultNow Returns the computed result, without waiting. This method is for cases where the caller knows that the task has already completed successfully, for example when filtering a stream of Future objects for the successful tasks and using a mapping operation to obtain a stream of results. {@snippet lang=java : \* results = futures.stream() \* .filter(f -\> f.state() == Future.State.SUCCESS) \* .map(Future::resultNow) \* .toList(); \* } <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | setForkJoinTaskTag Atomically sets the tag value for this task and returns the old value. <br /> | | `https://developer.android.com/reference/kotlin/java/util/concurrent/Future.State!` | state {@return the computation state} <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | tryUnfork Tries to unschedule this task for execution. This method will typically (but is not guaranteed to) succeed if this task is the most recently forked task by the current thread, and has not commenced executing in another thread. This method may be useful when arranging alternative local processing of tasks that could have been, but were not, stolen. <br /> | ||

## Public constructors

### RecursiveTask

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
RecursiveTask()
```

Constructor for subclasses to call.

## Public methods

### getRawResult

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRawResult(): V
```

Returns the result that would be returned by join, even if this task completed abnormally, or `null` if this task is not known to have been completed. This method is designed to aid debugging, as well as to support extensions. Its use in any other context is discouraged.

| Return ||
|---|---|
| `V` | the result, or `null` if not completed |

## Protected methods

### compute

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun compute(): V
```

The main computation performed by this task.

| Return ||
|---|---|
| `V` | the result of the computation |

### exec

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun exec(): Boolean
```

Implements execution conventions for RecursiveTask.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this task is known to have completed normally |

### setRawResult

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun setRawResult(value: V): Unit
```

Forces the given value to be returned as a result. This method is designed to support extensions, and should not in general be called otherwise.

| Parameters ||
|---|---|
| `value` | V: the value |
