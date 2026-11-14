# RecursiveAction

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RecursiveAction

```
abstract class RecursiveAction : ForkJoinTask<Void!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.concurrent.ForkJoinTask](ForkJoinTask.md)\< [java.lang.Void](../java.lang/Void.md)\> ||
| | ↳ | [java.util.concurrent.RecursiveAction](RecursiveAction.md) |

A recursive resultless [ForkJoinTask](ForkJoinTask.md). This class establishes conventions to parameterize resultless actions as`Void``ForkJoinTask`s. Because`null`is the only valid value of type`Void`, methods such as`join`always return`null`upon completion.

**Sample Usages.** Here is a simple but complete ForkJoin sort that sorts a given`long[]`array: 

```kotlin
<code>static class SortTask extends RecursiveAction {
    final long[] array; final int lo, hi;
    SortTask(long[] array, int lo, int hi) {
      this.array = array; this.lo = lo; this.hi = hi;
    }
    SortTask(long[] array) { this(array, 0, array.length); }
    protected void compute() {
      if (hi - lo &lt; THRESHOLD)
        sortSequentially(lo, hi);
      else {
        int mid = (lo + hi) &gt;&gt;&gt; 1;
        invokeAll(new SortTask(array, lo, mid),
                  new SortTask(array, mid, hi));
        merge(lo, mid, hi);
      }
    }
    // implementation details follow:
    static final int THRESHOLD = 1000;
    void sortSequentially(int lo, int hi) {
      Arrays.sort(array, lo, hi);
    }
    void merge(int lo, int mid, int hi) {
      long[] buf = Arrays.copyOfRange(array, lo, mid);
      for (int i = 0, j = lo, k = mid; i &lt; buf.length; j++)
        array[j] = (k == hi || buf[i] &lt; array[k]) ?
          buf[i++] : array[k++];
    }
  }</code>
```
You could then sort`anArray`by creating`new SortTask(anArray)`and invoking it in a ForkJoinPool. As a more concrete simple example, the following task increments each element of an array: 

```kotlin
<code>class IncrementTask extends RecursiveAction {
    final long[] array; final int lo, hi;
    IncrementTask(long[] array, int lo, int hi) {
      this.array = array; this.lo = lo; this.hi = hi;
    }
    protected void compute() {
      if (hi - lo &lt; THRESHOLD) {
        for (int i = lo; i &lt; hi; ++i)
          array[i]++;
      }
      else {
        int mid = (lo + hi) &gt;&gt;&gt; 1;
        invokeAll(new IncrementTask(array, lo, mid),
                  new IncrementTask(array, mid, hi));
      }
    }
  }</code>
```

The following example illustrates some refinements and idioms that may lead to better performance: RecursiveActions need not be fully recursive, so long as they maintain the basic divide-and-conquer approach. Here is a class that sums the squares of each element of a double array, by subdividing out only the right-hand-sides of repeated divisions by two, and keeping track of them with a chain of`next`references. It uses a dynamic threshold based on method`getSurplusQueuedTaskCount`, but counterbalances potential excess partitioning by directly performing leaf actions on unstolen tasks rather than further subdividing. 

```kotlin
<code>double sumOfSquares(ForkJoinPool pool, double[] array) {
    int n = array.length;
    Applyer a = new Applyer(array, 0, n, null);
    pool.invoke(a);
    return a.result;
  }
 
  class Applyer extends RecursiveAction {
    final double[] array;
    final int lo, hi;
    double result;
    Applyer next; // keeps track of right-hand-side tasks
    Applyer(double[] array, int lo, int hi, Applyer next) {
      this.array = array; this.lo = lo; this.hi = hi;
      this.next = next;
    }
 
    double atLeaf(int l, int h) {
      double sum = 0;
      for (int i = l; i &lt; h; ++i) // perform leftmost base step
        sum += array[i] * array[i];
      return sum;
    }
 
    protected void compute() {
      int l = lo;
      int h = hi;
      Applyer right = null;
      while (h - l &gt; 1 &amp;&amp; getSurplusQueuedTaskCount() &lt;= 3) {
        int mid = (l + h) &gt;&gt;&gt; 1;
        right = new Applyer(array, mid, h, right);
        right.fork();
        h = mid;
      }
      double sum = atLeaf(l, h);
      while (right != null) {
        if (right.tryUnfork()) // directly calculate if not stolen
          sum += right.atLeaf(right.lo, right.hi);
        else {
          right.join();
          sum += right.result;
        }
        right = right.next;
      }
      result = sum;
    }
  }</code>
```

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RecursiveAction](RecursiveAction.md))`()` Constructor for subclasses to call. |

| Public methods ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [Void](../java.lang/Void.md)! | [getRawResult](RecursiveAction.md))`()` Always returns`null`. |

| Protected methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [compute](RecursiveAction.md))`()` The main computation performed by this task. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [exec](RecursiveAction.md))`()` Implements execution conventions for RecursiveActions. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRawResult](RecursiveAction.md))`(`mustBeNull:` ` [Void](../java.lang/Void.md)!`)` Requires null completion value. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [ForkJoinTask](ForkJoinTask.md) |-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ForkJoinTask](ForkJoinTask.md)<*>! | [adapt](ForkJoinTask.md))`(`runnable:` ` [Runnable](../java.lang/Runnable.md)!`)` <br /> Returns a new`ForkJoinTask`that performs the`run`method of the given`Runnable`as its action, and returns a null result upon [join](ForkJoinTask.md)). <br /> | | [ForkJoinTask](ForkJoinTask.md)<T>! | [adapt](ForkJoinTask.md))`(`runnable:` ` [Runnable](../java.lang/Runnable.md)!`, `result:` `T`)` <br /> Returns a new`ForkJoinTask`that performs the`run`method of the given`Runnable`as its action, and returns the given result upon [join](ForkJoinTask.md)). <br /> | | [ForkJoinTask](ForkJoinTask.md)<T>! | [adapt](ForkJoinTask.md))`(`callable:` ` [Callable](Callable.md)<out` `T>!`)` <br /> Returns a new`ForkJoinTask`that performs the`call`method of the given`Callable`as its action, and returns its result upon [join](ForkJoinTask.md)), translating any checked exceptions encountered into`RuntimeException`. <br /> | | [ForkJoinTask](ForkJoinTask.md)<T>! | [adaptInterruptible](ForkJoinTask.md))`(`callable:` ` [Callable](Callable.md)<out` `T>!`)` <br /> Returns a new`ForkJoinTask`that performs the`call`method of the given`Callable`as its action, and returns its result upon [join](ForkJoinTask.md)), translating any checked exceptions encountered into`RuntimeException`. Additionally, invocations of`cancel`with`mayInterruptIfRunning true`will attempt to interrupt the thread performing the task. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [cancel](ForkJoinTask.md))`(`mayInterruptIfRunning:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Attempts to cancel execution of this task. This attempt will fail if the task has already completed or could not be cancelled for some other reason. If successful, and this task has not started when`cancel`is called, execution of this task is suppressed. After this method returns successfully, unless there is an intervening call to [reinitialize](ForkJoinTask.md)), subsequent calls to [isCancelled](ForkJoinTask.md)), [isDone](ForkJoinTask.md)), and`cancel`will return`true`and calls to [join](ForkJoinTask.md))and related methods will result in`CancellationException`. This method may be overridden in subclasses, but if so, must still ensure that these properties hold. In particular, the`cancel`method itself must not throw exceptions. This method is designed to be invoked by*other* tasks. To terminate the current task, you can just return or throw an unchecked exception from its computation method, or invoke [completeExceptionally(java.lang.Throwable)](ForkJoinTask.md)). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [compareAndSetForkJoinTaskTag](ForkJoinTask.md))`(`expect:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`, `update:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` <br /> Atomically conditionally sets the tag value for this task. Among other applications, tags can be used as visit markers in tasks operating on graphs, as in methods that check:`if (task.compareAndSetForkJoinTaskTag((short)0, (short)1))`before processing, otherwise exiting because the node has already been visited. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [complete](ForkJoinTask.md))`(`value:` `V`)` <br /> Completes this task, and if not already aborted or cancelled, returning the given value as the result of subsequent invocations of`join`and related operations. This method may be used to provide results for asynchronous tasks, or to provide alternative handling for tasks that would not otherwise complete normally. Its use in other situations is discouraged. This method is overridable, but overridden versions must invoke`super`implementation to maintain guarantees. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [completeExceptionally](ForkJoinTask.md))`(`ex:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> Completes this task abnormally, and if not already aborted or cancelled, causes it to throw the given exception upon`join`and related operations. This method may be used to induce exceptions in asynchronous tasks, or to force completion of tasks that would not otherwise complete. Its use in other situations is discouraged. This method is overridable, but overridden versions must invoke`super`implementation to maintain guarantees. <br /> | | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)! | [exceptionNow](ForkJoinTask.md))`()` <br /> | | [ForkJoinTask](ForkJoinTask.md)<V>! | [fork](ForkJoinTask.md))`()` <br /> Arranges to asynchronously execute this task in the pool the current task is running in, if applicable, or using the [java.util.concurrent.ForkJoinPool#commonPool()](ForkJoinPool.md))if not [inForkJoinPool](ForkJoinTask.md)). While it is not necessarily enforced, it is a usage error to fork a task more than once unless it has completed and been reinitialized. Subsequent modifications to the state of this task or any data it operates on are not necessarily consistently observable by any thread other than the one executing it unless preceded by a call to [join](ForkJoinTask.md))or related methods, or a call to [isDone](ForkJoinTask.md))returning`true`. <br /> | | V | [get](ForkJoinTask.md))`()` <br /> Waits if necessary for the computation to complete, and then retrieves its result. <br /> | | V | [get](ForkJoinTask.md))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` <br /> Waits if necessary for at most the given time for the computation to complete, and then retrieves its result, if available. <br /> | | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)! | [getException](ForkJoinTask.md))`()` <br /> Returns the exception thrown by the base computation, or a`CancellationException`if cancelled, or`null`if none or if the method has not yet completed. <br /> | | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getForkJoinTaskTag](ForkJoinTask.md))`()` <br /> Returns the tag for this task. <br /> | | [ForkJoinPool](ForkJoinPool.md)! | [getPool](ForkJoinTask.md))`()` <br /> Returns the pool hosting the current thread, or`null`if the current thread is executing outside of any ForkJoinPool. This method returns`null`if and only if [inForkJoinPool](ForkJoinTask.md))returns`false`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getQueuedTaskCount](ForkJoinTask.md))`()` <br /> Returns an estimate of the number of tasks that have been forked by the current worker thread but not yet executed. This value may be useful for heuristic decisions about whether to fork other tasks. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSurplusQueuedTaskCount](ForkJoinTask.md))`()` <br /> Returns an estimate of how many more locally queued tasks are held by the current worker thread than there are other worker threads that might steal them, or zero if this thread is not operating in a ForkJoinPool. This value may be useful for heuristic decisions about whether to fork other tasks. In many usages of ForkJoinTasks, at steady state, each worker should aim to maintain a small constant surplus (for example, 3) of tasks, and to process computations locally if this threshold is exceeded. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [helpQuiesce](ForkJoinTask.md))`()` <br /> Possibly executes tasks until the pool hosting the current task [is quiescent](ForkJoinPool.md)). This method may be of use in designs in which many tasks are forked, but none are explicitly joined, instead executing them until all are processed. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [inForkJoinPool](ForkJoinTask.md))`()` <br /> Returns`true`if the current thread is a [ForkJoinWorkerThread](ForkJoinWorkerThread.md) executing as a ForkJoinPool computation. <br /> | | V | [invoke](ForkJoinTask.md))`()` <br /> Commences performing this task, awaits its completion if necessary, and returns its result, or throws an (unchecked)`RuntimeException`or`Error`if the underlying computation did so. <br /> | | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<T>! | [invokeAll](ForkJoinTask.md))`(`tasks:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<T>!`)` <br /> Forks all tasks in the specified collection, returning when`isDone`holds for each task or an (unchecked) exception is encountered, in which case the exception is rethrown. If more than one task encounters an exception, then this method throws any one of these exceptions. If any task encounters an exception, others may be cancelled. However, the execution status of individual tasks is not guaranteed upon exceptional return. The status of each task may be obtained using [getException()](ForkJoinTask.md))and related methods to check if they have been cancelled, completed normally or exceptionally, or left unprocessed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [invokeAll](ForkJoinTask.md))`(`t1:` ` [ForkJoinTask](ForkJoinTask.md)<*>!`, `t2:` ` [ForkJoinTask](ForkJoinTask.md)<*>!`)` <br /> Forks the given tasks, returning when`isDone`holds for each task or an (unchecked) exception is encountered, in which case the exception is rethrown. If more than one task encounters an exception, then this method throws any one of these exceptions. If any task encounters an exception, the other may be cancelled. However, the execution status of individual tasks is not guaranteed upon exceptional return. The status of each task may be obtained using [getException()](ForkJoinTask.md))and related methods to check if they have been cancelled, completed normally or exceptionally, or left unprocessed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [invokeAll](ForkJoinTask.md))`(`vararg` `tasks:` ` [ForkJoinTask](ForkJoinTask.md)<*>!`)` <br /> Forks the given tasks, returning when`isDone`holds for each task or an (unchecked) exception is encountered, in which case the exception is rethrown. If more than one task encounters an exception, then this method throws any one of these exceptions. If any task encounters an exception, others may be cancelled. However, the execution status of individual tasks is not guaranteed upon exceptional return. The status of each task may be obtained using [getException()](ForkJoinTask.md))and related methods to check if they have been cancelled, completed normally or exceptionally, or left unprocessed. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCancelled](ForkJoinTask.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCompletedAbnormally](ForkJoinTask.md))`()` <br /> Returns`true`if this task threw an exception or was cancelled. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCompletedNormally](ForkJoinTask.md))`()` <br /> Returns`true`if this task completed without throwing an exception and was not cancelled. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDone](ForkJoinTask.md))`()` <br /> | | V | [join](ForkJoinTask.md))`()` <br /> Returns the result of the computation when it [is done](ForkJoinTask.md)). This method differs from [get()](ForkJoinTask.md))in that abnormal completion results in`RuntimeException`or`Error`, not`ExecutionException`, and that interrupts of the calling thread do*not* cause the method to abruptly return by throwing`InterruptedException`. <br /> | | [ForkJoinTask](ForkJoinTask.md)<*>! | [peekNextLocalTask](ForkJoinTask.md))`()` <br /> Returns, but does not unschedule or execute, a task queued by the current thread but not yet executed, if one is immediately available. There is no guarantee that this task will actually be polled or executed next. Conversely, this method may return null even if a task exists but cannot be accessed without contention with other threads. This method is designed primarily to support extensions, and is unlikely to be useful otherwise. <br /> | | [ForkJoinTask](ForkJoinTask.md)<*>! | [pollNextLocalTask](ForkJoinTask.md))`()` <br /> Unschedules and returns, without executing, the next task queued by the current thread but not yet executed, if the current thread is operating in a ForkJoinPool. This method is designed primarily to support extensions, and is unlikely to be useful otherwise. <br /> | | [ForkJoinTask](ForkJoinTask.md)<*>! | [pollTask](ForkJoinTask.md))`()` <br /> If the current thread is operating in a ForkJoinPool, unschedules and returns, without executing, the next task queued by the current thread but not yet executed, if one is available, or if not available, a task that was forked by some other thread, if available. Availability may be transient, so a`null`result does not necessarily imply quiescence of the pool this task is operating in. This method is designed primarily to support extensions, and is unlikely to be useful otherwise. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [quietlyComplete](ForkJoinTask.md))`()` <br /> Completes this task normally without setting a value. The most recent value established by [setRawResult](ForkJoinTask.md))(or`null`by default) will be returned as the result of subsequent invocations of`join`and related operations. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [quietlyInvoke](ForkJoinTask.md))`()` <br /> Commences performing this task and awaits its completion if necessary, without returning its result or throwing its exception. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [quietlyJoin](ForkJoinTask.md))`()` <br /> Joins this task, without returning its result or throwing its exception. This method may be useful when processing collections of tasks when some have been cancelled or otherwise known to have aborted. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [quietlyJoin](ForkJoinTask.md))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` <br /> Tries to join this task, returning true if it completed (possibly exceptionally) before the given timeout and the current thread has not been interrupted. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [quietlyJoinUninterruptibly](ForkJoinTask.md))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` <br /> Tries to join this task, returning true if it completed (possibly exceptionally) before the given timeout. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reinitialize](ForkJoinTask.md))`()` <br /> Resets the internal bookkeeping state of this task, allowing a subsequent`fork`. This method allows repeated reuse of this task, but only if reuse occurs when this task has either never been forked, or has been forked, then completed and all outstanding joins of this task have also completed. Effects under any other usage conditions are not guaranteed. This method may be useful when executing pre-constructed trees of subtasks in loops. Upon completion of this method,`isDone()`reports`false`, and`getException()`reports`null`. However, the value returned by`getRawResult`is unaffected. To clear this value, you can invoke`setRawResult(null)`. <br /> | | V | [resultNow](ForkJoinTask.md))`()` <br /> | | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [setForkJoinTaskTag](ForkJoinTask.md))`(`newValue:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` <br /> Atomically sets the tag value for this task and returns the old value. <br /> | | [Future.State](../java/util/concurrent/Future.State.md)! | [state](ForkJoinTask.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [tryUnfork](ForkJoinTask.md))`()` <br /> Tries to unschedule this task for execution. This method will typically (but is not guaranteed to) succeed if this task is the most recently forked task by the current thread, and has not commenced executing in another thread. This method may be useful when arranging alternative local processing of tasks that could have been, but were not, stolen. <br /> | ||

## Public constructors

### RecursiveAction

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RecursiveAction()
```

Constructor for subclasses to call.

## Public methods

### getRawResult

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRawResult(): Void!
```

Always returns`null`.

| Return ||
|------------------------------------------------------------------------------|--------------|
| [Void](../java.lang/Void.md)! | `null`always |

## Protected methods

### compute

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun compute(): Unit
```

The main computation performed by this task. 

### exec

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun exec(): Boolean
```

Implements execution conventions for RecursiveActions.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this task is known to have completed normally |

### setRawResult

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun setRawResult(mustBeNull: Void!): Unit
```

Requires null completion value.

| Parameters ||
|---------|-----------|
| `value` | the value |
