# Executors

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Executors

```
open class Executors
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.concurrent.Executors](Executors.md) |

Factory and utility methods for [Executor](Executor.md), [ExecutorService](ExecutorService.md), [ScheduledExecutorService](ScheduledExecutorService.md), [ThreadFactory](ThreadFactory.md), and [Callable](Callable.md) classes defined in this package. This class supports the following kinds of methods:

- Methods that create and return an [ExecutorService](ExecutorService.md) set up with commonly useful configuration settings.
- Methods that create and return a [ScheduledExecutorService](ScheduledExecutorService.md) set up with commonly useful configuration settings.
- Methods that create and return a "wrapped" ExecutorService, that disables reconfiguration by making implementation-specific methods inaccessible.
- Methods that create and return a [ThreadFactory](ThreadFactory.md) that sets newly created threads to a known state.
- Methods that create and return a [Callable](Callable.md) out of other closure-like forms, so they can be used in execution methods requiring`Callable`.

<br />

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Callable](Callable.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | [callable](Executors.md))`(`task:` ` [Runnable](../java.lang/Runnable.md)!`)` Returns a [Callable](Callable.md) object that, when called, runs the given task and returns`null`. |
| openstatic [Callable](Callable.md)\<T\>! | [callable](Executors.md))`(`task:` ` [Runnable](../java.lang/Runnable.md)!`, `result:` `T`)` Returns a [Callable](Callable.md) object that, when called, runs the given task and returns the given result. |
| openstatic [Callable](Callable.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | [callable](Executors.md))`(`action:` ` [PrivilegedAction](../java.security/PrivilegedAction.md)<*>!`)` Returns a [Callable](Callable.md) object that, when called, runs the given privileged action and returns its result. |
| --- | --- |
| openstatic [Callable](Callable.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | [callable](Executors.md))`(`action:` ` [PrivilegedExceptionAction](../java.security/PrivilegedExceptionAction.md)<*>!`)` Returns a [Callable](Callable.md) object that, when called, runs the given privileged exception action and returns its result. |
| openstatic [ThreadFactory](ThreadFactory.md)! | [defaultThreadFactory](Executors.md))`()` Returns a default thread factory used to create new threads. |
| openstatic [ExecutorService](ExecutorService.md)! | [newCachedThreadPool](Executors.md))`()` Creates a thread pool that creates new threads as needed, but will reuse previously constructed threads when they are available. |
| --- | --- |
| openstatic [ExecutorService](ExecutorService.md)! | [newCachedThreadPool](Executors.md))`(`threadFactory:` ` [ThreadFactory](ThreadFactory.md)!`)` Creates a thread pool that creates new threads as needed, but will reuse previously constructed threads when they are available, and uses the provided ThreadFactory to create new threads when needed. |
| openstatic [ExecutorService](ExecutorService.md)! | [newFixedThreadPool](Executors.md))`(`nThreads:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a thread pool that reuses a fixed number of threads operating off a shared unbounded queue. |
| openstatic [ExecutorService](ExecutorService.md)! | [newFixedThreadPool](Executors.md))`(`nThreads:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `threadFactory:` ` [ThreadFactory](ThreadFactory.md)!`)` Creates a thread pool that reuses a fixed number of threads operating off a shared unbounded queue, using the provided ThreadFactory to create new threads when needed. |
| --- | --- |
| openstatic [ScheduledExecutorService](ScheduledExecutorService.md)! | [newScheduledThreadPool](Executors.md))`(`corePoolSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a thread pool that can schedule commands to run after a given delay, or to execute periodically. |
| openstatic [ScheduledExecutorService](ScheduledExecutorService.md)! | [newScheduledThreadPool](Executors.md))`(`corePoolSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `threadFactory:` ` [ThreadFactory](ThreadFactory.md)!`)` Creates a thread pool that can schedule commands to run after a given delay, or to execute periodically. |
| openstatic [ExecutorService](ExecutorService.md)! | [newSingleThreadExecutor](Executors.md))`()` Creates an Executor that uses a single worker thread operating off an unbounded queue. |
| --- | --- |
| openstatic [ExecutorService](ExecutorService.md)! | [newSingleThreadExecutor](Executors.md))`(`threadFactory:` ` [ThreadFactory](ThreadFactory.md)!`)` Creates an Executor that uses a single worker thread operating off an unbounded queue, and uses the provided ThreadFactory to create a new thread when needed. |
| openstatic [ScheduledExecutorService](ScheduledExecutorService.md)! | [newSingleThreadScheduledExecutor](Executors.md))`()` Creates a single-threaded executor that can schedule commands to run after a given delay, or to execute periodically. |
| openstatic [ScheduledExecutorService](ScheduledExecutorService.md)! | [newSingleThreadScheduledExecutor](Executors.md))`(`threadFactory:` ` [ThreadFactory](ThreadFactory.md)!`)` Creates a single-threaded executor that can schedule commands to run after a given delay, or to execute periodically. |
| --- | --- |
| openstatic [ExecutorService](ExecutorService.md)! | [newWorkStealingPool](Executors.md))`()` Creates a work-stealing thread pool using the number of [available processors](../java.lang/Runtime.md))as its target parallelism level. |
| openstatic [ExecutorService](ExecutorService.md)! | [newWorkStealingPool](Executors.md))`(`parallelism:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a thread pool that maintains enough threads to support the given parallelism level, and may use multiple queues to reduce contention. |
| openstatic [Callable](Callable.md)\<T\>! | [privilegedCallable](Executors.md))`(`callable:` ` [Callable](Callable.md)<T>!`)` Legacy security code; do not use. |
| --- | --- |
| openstatic [Callable](Callable.md)\<T\>! | [privilegedCallableUsingCurrentClassLoader](Executors.md))`(`callable:` ` [Callable](Callable.md)<T>!`)` Legacy security code; do not use. |
| openstatic [ThreadFactory](ThreadFactory.md)! | [privilegedThreadFactory](Executors.md))`()` Legacy security code; do not use. |
| openstatic [ExecutorService](ExecutorService.md)! | [unconfigurableExecutorService](Executors.md))`(`executor:` ` [ExecutorService](ExecutorService.md)!`)` Returns an object that delegates all defined [ExecutorService](ExecutorService.md) methods to the given executor, but not any other methods that might otherwise be accessible using casts. |
| --- | --- |
| openstatic [ScheduledExecutorService](ScheduledExecutorService.md)! | [unconfigurableScheduledExecutorService](Executors.md))`(`executor:` ` [ScheduledExecutorService](ScheduledExecutorService.md)!`)` Returns an object that delegates all defined [ScheduledExecutorService](ScheduledExecutorService.md) methods to the given executor, but not any other methods that might otherwise be accessible using casts. |

## Public methods

### callable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun callable(task: Runnable!): Callable<Any!>!
```

Returns a [Callable](Callable.md) object that, when called, runs the given task and returns`null`.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------|
| `task` | [Runnable](../java.lang/Runnable.md)!:the task to run |

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|
| [Callable](Callable.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>! | a callable object |

| Exceptions ||
|----------------------------------|--------------|
| `java.lang.NullPointerException` | if task null |

### callable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> callable(
    task: Runnable!, 
    result: T
): Callable<T>!
```

Returns a [Callable](Callable.md) object that, when called, runs the given task and returns the given result. This can be useful when applying methods requiring a`Callable`to an otherwise resultless action.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------|
| `task` | [Runnable](../java.lang/Runnable.md)!:the task to run |
| `result` | T:the result to return |
| `<T>` | the type of the result |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------------|-------------------|
| [Callable](Callable.md)<T>! | a callable object |

| Exceptions ||
|----------------------------------|--------------|
| `java.lang.NullPointerException` | if task null |

### callable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun callable(action: PrivilegedAction<*>!): Callable<Any!>!
```

Returns a [Callable](Callable.md) object that, when called, runs the given privileged action and returns its result.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [PrivilegedAction](../java.security/PrivilegedAction.md)\<\*\>!:the privileged action to run |

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|
| [Callable](Callable.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>! | a callable object |

| Exceptions ||
|----------------------------------|----------------|
| `java.lang.NullPointerException` | if action null |

### callable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun callable(action: PrivilegedExceptionAction<*>!): Callable<Any!>!
```

Returns a [Callable](Callable.md) object that, when called, runs the given privileged exception action and returns its result.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [PrivilegedExceptionAction](../java.security/PrivilegedExceptionAction.md)\<\*\>!:the privileged exception action to run |

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|
| [Callable](Callable.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>! | a callable object |

| Exceptions ||
|----------------------------------|----------------|
| `java.lang.NullPointerException` | if action null |

### defaultThreadFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun defaultThreadFactory(): ThreadFactory!
```

Returns a default thread factory used to create new threads. This factory creates all new threads used by an Executor in the same [ThreadGroup](../java.lang/ThreadGroup.md). Each new thread is created as a non-daemon thread with priority set to the smaller of`Thread.NORM_PRIORITY`and the maximum priority permitted in the thread group. New threads have names accessible via [Thread.getName](../java.lang/Thread.md))of*pool-N-thread-M* , where*N* is the sequence number of this factory, and*M*is the sequence number of the thread created by this factory.

| Return ||
|-----------------------------------------------------------------------------------------------------|------------------|
| [ThreadFactory](ThreadFactory.md)! | a thread factory |

### newCachedThreadPool

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newCachedThreadPool(): ExecutorService!
```

Creates a thread pool that creates new threads as needed, but will reuse previously constructed threads when they are available. These pools will typically improve the performance of programs that execute many short-lived asynchronous tasks. Calls to`execute`will reuse previously constructed threads if available. If no existing thread is available, a new thread will be created and added to the pool. Threads that have not been used for sixty seconds are terminated and removed from the cache. Thus, a pool that remains idle for long enough will not consume any resources. Note that pools with similar properties but different details (for example, timeout parameters) may be created using [ThreadPoolExecutor](ThreadPoolExecutor.md) constructors.

| Return ||
|---------------------------------------------------------------------------------------------------------|-------------------------------|
| [ExecutorService](ExecutorService.md)! | the newly created thread pool |

### newCachedThreadPool

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newCachedThreadPool(threadFactory: ThreadFactory!): ExecutorService!
```

Creates a thread pool that creates new threads as needed, but will reuse previously constructed threads when they are available, and uses the provided ThreadFactory to create new threads when needed.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `threadFactory` | [ThreadFactory](ThreadFactory.md)!:the factory to use when creating new threads |

| Return ||
|---------------------------------------------------------------------------------------------------------|-------------------------------|
| [ExecutorService](ExecutorService.md)! | the newly created thread pool |

| Exceptions ||
|----------------------------------|--------------------------|
| `java.lang.NullPointerException` | if threadFactory is null |

### newFixedThreadPool

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newFixedThreadPool(nThreads: Int): ExecutorService!
```

Creates a thread pool that reuses a fixed number of threads operating off a shared unbounded queue. At any point, at most`nThreads`threads will be active processing tasks. If additional tasks are submitted when all threads are active, they will wait in the queue until a thread is available. If any thread terminates due to a failure during execution prior to shutdown, a new one will take its place if needed to execute subsequent tasks. The threads in the pool will exist until it is explicitly [shutdown](ExecutorService.md)).

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------|
| `nThreads` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of threads in the pool |

| Return ||
|---------------------------------------------------------------------------------------------------------|-------------------------------|
| [ExecutorService](ExecutorService.md)! | the newly created thread pool |

| Exceptions ||
|--------------------------------------|-------------------|
| `java.lang.IllegalArgumentException` | if`nThreads <= 0` |

### newFixedThreadPool

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newFixedThreadPool(
    nThreads: Int, 
    threadFactory: ThreadFactory!
): ExecutorService!
```

Creates a thread pool that reuses a fixed number of threads operating off a shared unbounded queue, using the provided ThreadFactory to create new threads when needed. At any point, at most`nThreads`threads will be active processing tasks. If additional tasks are submitted when all threads are active, they will wait in the queue until a thread is available. If any thread terminates due to a failure during execution prior to shutdown, a new one will take its place if needed to execute subsequent tasks. The threads in the pool will exist until it is explicitly [shutdown](ExecutorService.md)).

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `nThreads` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of threads in the pool |
| `threadFactory` | [ThreadFactory](ThreadFactory.md)!:the factory to use when creating new threads |

| Return ||
|---------------------------------------------------------------------------------------------------------|-------------------------------|
| [ExecutorService](ExecutorService.md)! | the newly created thread pool |

| Exceptions ||
|--------------------------------------|--------------------------|
| `java.lang.NullPointerException` | if threadFactory is null |
| `java.lang.IllegalArgumentException` | if`nThreads <= 0` |

### newScheduledThreadPool

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newScheduledThreadPool(corePoolSize: Int): ScheduledExecutorService!
```

Creates a thread pool that can schedule commands to run after a given delay, or to execute periodically.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `corePoolSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of threads to keep in the pool, even if they are idle |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [ScheduledExecutorService](ScheduledExecutorService.md)! | the newly created scheduled thread pool |

| Exceptions ||
|--------------------------------------|----------------------|
| `java.lang.IllegalArgumentException` | if`corePoolSize < 0` |

### newScheduledThreadPool

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newScheduledThreadPool(
    corePoolSize: Int, 
    threadFactory: ThreadFactory!
): ScheduledExecutorService!
```

Creates a thread pool that can schedule commands to run after a given delay, or to execute periodically.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `corePoolSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of threads to keep in the pool, even if they are idle |
| `threadFactory` | [ThreadFactory](ThreadFactory.md)!:the factory to use when the executor creates a new thread |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [ScheduledExecutorService](ScheduledExecutorService.md)! | the newly created scheduled thread pool |

| Exceptions ||
|--------------------------------------|--------------------------|
| `java.lang.IllegalArgumentException` | if`corePoolSize < 0` |
| `java.lang.NullPointerException` | if threadFactory is null |

### newSingleThreadExecutor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newSingleThreadExecutor(): ExecutorService!
```

Creates an Executor that uses a single worker thread operating off an unbounded queue. (Note however that if this single thread terminates due to a failure during execution prior to shutdown, a new one will take its place if needed to execute subsequent tasks.) Tasks are guaranteed to execute sequentially, and no more than one task will be active at any given time. Unlike the otherwise equivalent`newFixedThreadPool(1)`the returned executor is guaranteed not to be reconfigurable to use additional threads.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [ExecutorService](ExecutorService.md)! | the newly created single-threaded Executor |

### newSingleThreadExecutor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newSingleThreadExecutor(threadFactory: ThreadFactory!): ExecutorService!
```

Creates an Executor that uses a single worker thread operating off an unbounded queue, and uses the provided ThreadFactory to create a new thread when needed. Unlike the otherwise equivalent`newFixedThreadPool(1, threadFactory)`the returned executor is guaranteed not to be reconfigurable to use additional threads.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `threadFactory` | [ThreadFactory](ThreadFactory.md)!:the factory to use when creating new threads |

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [ExecutorService](ExecutorService.md)! | the newly created single-threaded Executor |

| Exceptions ||
|----------------------------------|--------------------------|
| `java.lang.NullPointerException` | if threadFactory is null |

### newSingleThreadScheduledExecutor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newSingleThreadScheduledExecutor(): ScheduledExecutorService!
```

Creates a single-threaded executor that can schedule commands to run after a given delay, or to execute periodically. (Note however that if this single thread terminates due to a failure during execution prior to shutdown, a new one will take its place if needed to execute subsequent tasks.) Tasks are guaranteed to execute sequentially, and no more than one task will be active at any given time. Unlike the otherwise equivalent`newScheduledThreadPool(1)`the returned executor is guaranteed not to be reconfigurable to use additional threads.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| [ScheduledExecutorService](ScheduledExecutorService.md)! | the newly created scheduled executor |

### newSingleThreadScheduledExecutor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newSingleThreadScheduledExecutor(threadFactory: ThreadFactory!): ScheduledExecutorService!
```

Creates a single-threaded executor that can schedule commands to run after a given delay, or to execute periodically. (Note however that if this single thread terminates due to a failure during execution prior to shutdown, a new one will take its place if needed to execute subsequent tasks.) Tasks are guaranteed to execute sequentially, and no more than one task will be active at any given time. Unlike the otherwise equivalent`newScheduledThreadPool(1, threadFactory)`the returned executor is guaranteed not to be reconfigurable to use additional threads.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `threadFactory` | [ThreadFactory](ThreadFactory.md)!:the factory to use when creating new threads |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| [ScheduledExecutorService](ScheduledExecutorService.md)! | the newly created scheduled executor |

| Exceptions ||
|----------------------------------|--------------------------|
| `java.lang.NullPointerException` | if threadFactory is null |

### newWorkStealingPool

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newWorkStealingPool(): ExecutorService!
```

Creates a work-stealing thread pool using the number of [available processors](../java.lang/Runtime.md))as its target parallelism level.

| Return ||
|---------------------------------------------------------------------------------------------------------|-------------------------------|
| [ExecutorService](ExecutorService.md)! | the newly created thread pool |

**See Also**

- [#newWorkStealingPool(int)](Executors.md)) 

### newWorkStealingPool

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newWorkStealingPool(parallelism: Int): ExecutorService!
```

Creates a thread pool that maintains enough threads to support the given parallelism level, and may use multiple queues to reduce contention. The parallelism level corresponds to the maximum number of threads actively engaged in, or available to engage in, task processing. The actual number of threads may grow and shrink dynamically. A work-stealing pool makes no guarantees about the order in which submitted tasks are executed.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------|
| `parallelism` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the targeted parallelism level |

| Return ||
|---------------------------------------------------------------------------------------------------------|-------------------------------|
| [ExecutorService](ExecutorService.md)! | the newly created thread pool |

| Exceptions ||
|--------------------------------------|----------------------|
| `java.lang.IllegalArgumentException` | if`parallelism <= 0` |

### privilegedCallable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> privilegedCallable(callable: Callable<T>!): Callable<T>!
```

**Deprecated:** *This method is only useful in conjunction with [the Security Manager](../java.lang/SecurityManager.md), which is deprecated and subject to removal in a future release. Consequently, this method is also deprecated and subject to removal. There is no replacement for the Security Manager or this method.*

Legacy security code; do not use. 

### privilegedCallableUsingCurrentClassLoader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> privilegedCallableUsingCurrentClassLoader(callable: Callable<T>!): Callable<T>!
```

**Deprecated:** *This method is only useful in conjunction with [the Security Manager](../java.lang/SecurityManager.md), which is deprecated and subject to removal in a future release. Consequently, this method is also deprecated and subject to removal. There is no replacement for the Security Manager or this method.*

Legacy security code; do not use. 

### privilegedThreadFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun privilegedThreadFactory(): ThreadFactory!
```

**Deprecated:** *This method is only useful in conjunction with [the Security Manager](../java.lang/SecurityManager.md), which is deprecated and subject to removal in a future release. Consequently, this method is also deprecated and subject to removal. There is no replacement for the Security Manager or this method.*

Legacy security code; do not use. 

### unconfigurableExecutorService

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun unconfigurableExecutorService(executor: ExecutorService!): ExecutorService!
```

Returns an object that delegates all defined [ExecutorService](ExecutorService.md) methods to the given executor, but not any other methods that might otherwise be accessible using casts. This provides a way to safely "freeze" configuration and disallow tuning of a given concrete implementation.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [ExecutorService](ExecutorService.md)!:the underlying implementation |

| Return ||
|---------------------------------------------------------------------------------------------------------|-----------------------------|
| [ExecutorService](ExecutorService.md)! | an`ExecutorService`instance |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if executor null |

### unconfigurableScheduledExecutorService

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun unconfigurableScheduledExecutorService(executor: ScheduledExecutorService!): ScheduledExecutorService!
```

Returns an object that delegates all defined [ScheduledExecutorService](ScheduledExecutorService.md) methods to the given executor, but not any other methods that might otherwise be accessible using casts. This provides a way to safely "freeze" configuration and disallow tuning of a given concrete implementation.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [ScheduledExecutorService](ScheduledExecutorService.md)!:the underlying implementation |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| [ScheduledExecutorService](ScheduledExecutorService.md)! | a`ScheduledExecutorService`instance |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if executor null |
