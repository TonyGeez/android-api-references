# ExecutorCompletionService

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ExecutorCompletionService

```
open class ExecutorCompletionService<V : Any!> : CompletionService<V>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.util.concurrent.ExecutorCompletionService](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorCompletionService#) |

A [CompletionService](https://developer.android.com/reference/kotlin/java/util/concurrent/CompletionService) that uses a supplied [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor) to execute tasks. This class arranges that submitted tasks are, upon completion, placed on a queue accessible using`take`. The class is lightweight enough to be suitable for transient use when processing groups of tasks.

**Usage Examples.** Suppose you have a set of solvers for a certain problem, each returning a value of some type`Result`, and would like to run them concurrently, processing the results of each of them that return a non-null value, in some method`use(Result r)`. You could write this as: 

```kotlin
<code>void solve(Executor e,
             Collection&lt;Callable&lt;Result&gt;&gt; solvers)
      throws InterruptedException, ExecutionException {
    CompletionService&lt;Result&gt; cs
        = new ExecutorCompletionService&lt;&gt;(e);
    solvers.forEach(cs::submit);
    for (int i = solvers.size(); i &gt; 0; i--) {
      Result r = cs.take().get();
      if (r != null)
        use(r);
    }
  }</code>
```
Suppose instead that you would like to use the first non-null result of the set of tasks, ignoring any that encounter exceptions, and cancelling all other tasks when the first one is ready: 

```kotlin
<code>void solve(Executor e,
             Collection&lt;Callable&lt;Result&gt;&gt; solvers)
      throws InterruptedException {
    CompletionService&lt;Result&gt; cs
        = new ExecutorCompletionService&lt;&gt;(e);
    int n = solvers.size();
    List&lt;Future&lt;Result&gt;&gt; futures = new ArrayList&lt;&gt;(n);
    Result result = null;
    try {
      solvers.forEach(solver -&gt; futures.add(cs.submit(solver)));
      for (int i = n; i &gt; 0; i--) {
        try {
          Result r = cs.take().get();
          if (r != null) {
            result = r;
            break;
          }
        } catch (ExecutionException ignore) {}
      }
    } finally {
      futures.forEach(future -&gt; future.cancel(true));
    }
 
    if (result != null)
      use(result);
  }</code>
```

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ExecutorCompletionService](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorCompletionService#ExecutorCompletionService(java.util.concurrent.Executor))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor)!`)` Creates an ExecutorCompletionService using the supplied executor for base task execution and a [LinkedBlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingQueue) as a completion queue. |
| [ExecutorCompletionService](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorCompletionService#ExecutorCompletionService(java.util.concurrent.Executor,%20java.util.concurrent.BlockingQueue))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor)!`, `completionQueue:` ` [BlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue)< [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)<V>!>!`)` Creates an ExecutorCompletionService using the supplied executor for base task execution and the supplied queue as its completion queue. |

| Public methods ||
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)\<V\>! | [poll](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorCompletionService#poll())`()` <br /> |
| open [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)\<V\>! | [poll](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorCompletionService#poll(kotlin.Long,%20java.util.concurrent.TimeUnit))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` <br /> |
| open [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)\<V\>! | [submit](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorCompletionService#submit(java.lang.Runnable,%20java.util.concurrent.ExecutorCompletionService.V))`(`task:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`, `result:` `V`)` <br /> |
| open [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)\<V\>! | [submit](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorCompletionService#submit(java.util.concurrent.Callable))`(`task:` ` [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable)<V>!`)` <br /> |
| open [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)\<V\>! | [take](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorCompletionService#take())`()` <br /> |

## Public constructors

### ExecutorCompletionService

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ExecutorCompletionService(executor: Executor!)
```

Creates an ExecutorCompletionService using the supplied executor for base task execution and a [LinkedBlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingQueue) as a completion queue.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor)!:the executor to use |

| Exceptions ||
|----------------------------------|----------------------|
| `java.lang.NullPointerException` | if executor is`null` |

### ExecutorCompletionService

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ExecutorCompletionService(
    executor: Executor!, 
    completionQueue: BlockingQueue<Future<V>!>!)
```

Creates an ExecutorCompletionService using the supplied executor for base task execution and the supplied queue as its completion queue.

| Parameters ||
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor)!:the executor to use |
| `completionQueue` | [BlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue)\< [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)\<V\>!\>!:the queue to use as the completion queue normally one dedicated for use by this service. This queue is treated as unbounded -- failed attempted`Queue.add`operations for completed tasks cause them not to be retrievable. |

| Exceptions ||
|----------------------------------|------------------------------------------|
| `java.lang.NullPointerException` | if executor or completionQueue are`null` |

## Public methods

### poll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun poll(): Future<V>!
```

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)<V>! | the Future representing the next completed task, or`null`if none are present |

### poll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun poll(
    timeout: Long, 
    unit: TimeUnit!
): Future<V>!
```

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
open fun submit(
    task: Runnable!, 
    result: V
): Future<V>!
```

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
open fun submit(task: Callable<V>!): Future<V>!
```

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
open fun take(): Future<V>!
```

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------|
| [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future)<V>! | the Future representing the next completed task |

| Exceptions ||
|----------------------------------|------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |
