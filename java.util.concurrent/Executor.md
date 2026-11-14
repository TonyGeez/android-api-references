# Executor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Executor

```
interface Executor
```

| [java.util.concurrent.Executor](Executor.md) |

| Known Direct Subclasses [ExecutorService](ExecutorService.md) |--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ExecutorService](ExecutorService.md) | An [Executor](Executor.md) that provides methods to manage termination and methods that can produce a [Future](Future.md) for tracking progress of one or more asynchronous tasks. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AbstractExecutorService](AbstractExecutorService.md), [ForkJoinPool](ForkJoinPool.md), [ScheduledExecutorService](ScheduledExecutorService.md), [ScheduledThreadPoolExecutor](ScheduledThreadPoolExecutor.md), [ScheduledThreadPoolExecutor](ScheduledThreadPoolExecutor.md), [ThreadPoolExecutor](ThreadPoolExecutor.md) |--------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AbstractExecutorService](AbstractExecutorService.md) | Provides default implementations of [ExecutorService](ExecutorService.md) execution methods. | | [ForkJoinPool](ForkJoinPool.md) | An [ExecutorService](ExecutorService.md) for running [ForkJoinTask](ForkJoinTask.md) s. | | [ScheduledExecutorService](ScheduledExecutorService.md) | An [ExecutorService](ExecutorService.md) that can schedule commands to run after a given delay, or to execute periodically. | | [ScheduledThreadPoolExecutor](ScheduledThreadPoolExecutor.md) | A [ThreadPoolExecutor](ThreadPoolExecutor.md) that can additionally schedule commands to run after a given delay, or to execute periodically. | | [ScheduledThreadPoolExecutor](ScheduledThreadPoolExecutor.md) | A [ThreadPoolExecutor](ThreadPoolExecutor.md) that can additionally schedule commands to run after a given delay, or to execute periodically. | | [ThreadPoolExecutor](ThreadPoolExecutor.md) | An [ExecutorService](ExecutorService.md) that executes each submitted task using one of possibly several pooled threads, normally configured using [Executors](Executors.md) factory methods. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

An object that executes submitted [Runnable](../java.lang/Runnable.md) tasks. This interface provides a way of decoupling task submission from the mechanics of how each task will be run, including details of thread use, scheduling, etc. An`Executor`is normally used instead of explicitly creating threads. For example, rather than invoking`new Thread(new RunnableTask()).start()`for each of a set of tasks, you might use: 

```kotlin
<code>Executor executor = anExecutor();
  executor.execute(new RunnableTask1());
  executor.execute(new RunnableTask2());
  ...</code>
```
However, the`Executor`interface does not strictly require that execution be asynchronous. In the simplest case, an executor can run the submitted task immediately in the caller's thread: 

```kotlin
<code>class DirectExecutor implements Executor {
    public void execute(Runnable r) {
      r.run();
    }
  }</code>
```
More typically, tasks are executed in some thread other than the caller's thread. The executor below spawns a new thread for each task. 

```kotlin
<code>class ThreadPerTaskExecutor implements Executor {
    public void execute(Runnable r) {
      new Thread(r).start();
    }
  }</code>
```
Many`Executor`implementations impose some sort of limitation on how and when tasks are scheduled. The executor below serializes the submission of tasks to a second executor, illustrating a composite executor. 

```kotlin
<code>class SerialExecutor implements Executor {
    final Queue&lt;Runnable&gt; tasks = new ArrayDeque&lt;&gt;();
    final Executor executor;
    Runnable active;
 
    SerialExecutor(Executor executor) {
      this.executor = executor;
    }
 
    public synchronized void execute(Runnable r) {
      tasks.add(() -&gt; {
        try {
          r.run();
        } finally {
          scheduleNext();
        }
      });
      if (active == null) {
        scheduleNext();
      }
    }
 
    protected synchronized void scheduleNext() {
      if ((active = tasks.poll()) != null) {
        executor.execute(active);
      }
    }
  }</code>
```
The`Executor`implementations provided in this package implement [ExecutorService](ExecutorService.md), which is a more extensive interface. The [ThreadPoolExecutor](ThreadPoolExecutor.md) class provides an extensible thread pool implementation. The [Executors](Executors.md) class provides convenient factory methods for these Executors.

<br />

Memory consistency effects: Actions in a thread prior to submitting a`Runnable`object to an`Executor` [*happen-before*](_package.md) its execution begins, perhaps in another thread.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [execute](Executor.md))`(`command:` ` [Runnable](../java.lang/Runnable.md)!`)` Executes the given command at some time in the future. |

## Public methods

### execute

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun execute(command: Runnable!): Unit
```

Executes the given command at some time in the future. The command may execute in a new thread, in a pooled thread, or in the calling thread, at the discretion of the`Executor`implementation.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------|
| `command` | [Runnable](../java.lang/Runnable.md)!:the runnable task |

| Exceptions ||
|---------------------------------------------------|-----------------------------------------------|
| `java.util.concurrent.RejectedExecutionException` | if this task cannot be accepted for execution |
| `java.lang.NullPointerException` | if command is null |
