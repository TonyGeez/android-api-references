# AsynchronousChannelGroup

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AsynchronousChannelGroup

```
abstract class AsynchronousChannelGroup
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.nio.channels.AsynchronousChannelGroup](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup#) |

A grouping of asynchronous channels for the purpose of resource sharing.

An asynchronous channel group encapsulates the mechanics required to handle the completion of I/O operations initiated by [asynchronous channels](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannel) that are bound to the group. A group has an associated thread pool to which tasks are submitted to handle I/O events and dispatch to [completion-handlers](https://developer.android.com/reference/kotlin/java/nio/channels/CompletionHandler) that consume the result of asynchronous operations performed on channels in the group. In addition to handling I/O events, the pooled threads may also execute other tasks required to support the execution of asynchronous I/O operations.

An asynchronous channel group is created by invoking the [withFixedThreadPool](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup#withFixedThreadPool(kotlin.Int,%20java.util.concurrent.ThreadFactory))or [withCachedThreadPool](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup#withCachedThreadPool(java.util.concurrent.ExecutorService,%20kotlin.Int))methods defined here. Channels are bound to a group by specifying the group when constructing the channel. The associated thread pool is*owned*by the group; termination of the group results in the shutdown of the associated thread pool.

In addition to groups created explicitly, the Java virtual machine maintains a system-wide*default group* that is constructed automatically. Asynchronous channels that do not specify a group at construction time are bound to the default group. The default group has an associated thread pool that creates new threads as needed. The default group may be configured by means of system properties defined in the table below. Where the [ThreadFactory](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadFactory.html#) for the default group is not configured then the pooled threads of the default group are [daemon](https://developer.android.com/reference/kotlin/java/lang/Thread.html#isDaemon())threads.

| System property | Description |
| `java.nio.channels.DefaultThreadPool.threadFactory` | The value of this property is taken to be the fully-qualified name of a concrete [ThreadFactory](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadFactory.html#) class. The class is loaded using the system class loader and instantiated. The factory's [newThread](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadFactory.html#newThread(java.lang.Runnable))method is invoked to create each thread for the default group's thread pool. If the process to load and instantiate the value of the property fails then an unspecified error is thrown during the construction of the default group. |
| `java.nio.channels.DefaultThreadPool.initialSize` | The value of the`initialSize`parameter for the default group (see [withCachedThreadPool](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup#withCachedThreadPool(java.util.concurrent.ExecutorService,%20kotlin.Int))). The value of the property is taken to be the`String`representation of an`Integer`that is the initial size parameter. If the value cannot be parsed as an`Integer`it causes an unspecified error to be thrown during the construction of the default group. |
|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|

## Threading

The completion handler for an I/O operation initiated on a channel bound to a group is guaranteed to be invoked by one of the pooled threads in the group. This ensures that the completion handler is run by a thread with the expected*identity*.

Where an I/O operation completes immediately, and the initiating thread is one of the pooled threads in the group then the completion handler may be invoked directly by the initiating thread. To avoid stack overflow, an implementation may impose a limit as to the number of activations on the thread stack. Some I/O operations may prohibit invoking the completion handler directly by the initiating thread (see [accept](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousServerSocketChannel#accept(java.nio.channels.AsynchronousServerSocketChannel.accept.A,%20java.nio.channels.CompletionHandler))).

## Shutdown and Termination

The [shutdown](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup#shutdown())method is used to initiate an*orderly shutdown* of a group. An orderly shutdown marks the group as shutdown; further attempts to construct a channel that binds to the group will throw [ShutdownChannelGroupException](https://developer.android.com/reference/kotlin/java/nio/channels/ShutdownChannelGroupException). Whether or not a group is shutdown can be tested using the [isShutdown](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup#isShutdown())method. Once shutdown, the group*terminates* when all asynchronous channels that are bound to the group are closed, all actively executing completion handlers have run to completion, and resources used by the group are released. No attempt is made to stop or interrupt threads that are executing completion handlers. The [isTerminated](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup#isTerminated())method is used to test if the group has terminated, and the [awaitTermination](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup#awaitTermination(kotlin.Long,%20java.util.concurrent.TimeUnit))method can be used to block until the group has terminated.

The [shutdownNow](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup#shutdownNow())method can be used to initiate a*forceful shutdown* of the group. In addition to the actions performed by an orderly shutdown, the`shutdownNow`method closes all open channels in the group as if by invoking the java.nio.channels.AsynchronousChannel#close method.

## Summary

| Protected constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AsynchronousChannelGroup](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup#AsynchronousChannelGroup(java.nio.channels.spi.AsynchronousChannelProvider))`(`provider:` ` [AsynchronousChannelProvider](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AsynchronousChannelProvider)!`)` Initialize a new instance of this class. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [awaitTermination](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup#awaitTermination(kotlin.Long,%20java.util.concurrent.TimeUnit))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit.html#)!`)` Awaits termination of the group. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isShutdown](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup#isShutdown())`()` Tells whether or not this asynchronous channel group is shutdown. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTerminated](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup#isTerminated())`()` Tells whether or not this group has terminated. |
| [AsynchronousChannelProvider](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AsynchronousChannelProvider)! | [provider](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup#provider())`()` Returns the provider that created this channel group. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [shutdown](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup#shutdown())`()` Initiates an orderly shutdown of the group. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [shutdownNow](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup#shutdownNow())`()` Shuts down the group and closes all open channels in the group. |
| openstatic [AsynchronousChannelGroup](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup#)! | [withCachedThreadPool](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup#withCachedThreadPool(java.util.concurrent.ExecutorService,%20kotlin.Int))`(`executor:` ` [ExecutorService](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService.html#)!`, `initialSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates an asynchronous channel group with a given thread pool that creates new threads as needed. |
| openstatic [AsynchronousChannelGroup](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup#)! | [withFixedThreadPool](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup#withFixedThreadPool(kotlin.Int,%20java.util.concurrent.ThreadFactory))`(`nThreads:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `threadFactory:` ` [ThreadFactory](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadFactory.html#)!`)` Creates an asynchronous channel group with a fixed thread pool. |
| openstatic [AsynchronousChannelGroup](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup#)! | [withThreadPool](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup#withThreadPool(java.util.concurrent.ExecutorService))`(`executor:` ` [ExecutorService](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService.html#)!`)` Creates an asynchronous channel group with a given thread pool. |

## Protected constructors

### AsynchronousChannelGroup

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected AsynchronousChannelGroup(provider: AsynchronousChannelProvider!)
```

Initialize a new instance of this class.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [AsynchronousChannelProvider](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AsynchronousChannelProvider)!:The asynchronous channel provider for this group |

## Public methods

### awaitTermination

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun awaitTermination(
    timeout: Long, 
    unit: TimeUnit!
): Boolean
```

Awaits termination of the group.

This method blocks until the group has terminated, or the timeout occurs, or the current thread is interrupted, whichever happens first.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The maximum time to wait, or zero or less to not wait |
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit.html#)!:The time unit of the timeout argument |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the group has terminated;`false`if the timeout elapsed before termination |

| Exceptions ||
|----------------------------------|------------------------------|
| `java.lang.InterruptedException` | If interrupted while waiting |

### isShutdown

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isShutdown(): Boolean
```

Tells whether or not this asynchronous channel group is shutdown.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this asynchronous channel group is shutdown or has been marked for shutdown. |

### isTerminated

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isTerminated(): Boolean
```

Tells whether or not this group has terminated.

Where this method returns`true`, then the associated thread pool has also [terminated](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService.html#isTerminated()).

| Return ||
|------------------------------------------------------------------------------------|------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this group has terminated |

### provider

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun provider(): AsynchronousChannelProvider!
```

Returns the provider that created this channel group.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| [AsynchronousChannelProvider](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AsynchronousChannelProvider)! | The provider that created this channel group |

### shutdown

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun shutdown(): Unit
```

Initiates an orderly shutdown of the group.

This method marks the group as shutdown. Further attempts to construct channel that binds to this group will throw [ShutdownChannelGroupException](https://developer.android.com/reference/kotlin/java/nio/channels/ShutdownChannelGroupException). The group terminates when all asynchronous channels in the group are closed, all actively executing completion handlers have run to completion, and all resources have been released. This method has no effect if the group is already shutdown. 

### shutdownNow

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun shutdownNow(): Unit
```

Shuts down the group and closes all open channels in the group.

In addition to the actions performed by the [shutdown](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup#shutdown())method, this method invokes the java.nio.channels.AsynchronousChannel#close method on all open channels in the group. This method does not attempt to stop or interrupt threads that are executing completion handlers. The group terminates when all actively executing completion handlers have run to completion and all resources have been released. This method may be invoked at any time. If some other thread has already invoked it, then another invocation will block until the first invocation is complete, after which it will return without effect.

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |

### withCachedThreadPool

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun withCachedThreadPool(
    executor: ExecutorService!, 
    initialSize: Int
): AsynchronousChannelGroup!
```

Creates an asynchronous channel group with a given thread pool that creates new threads as needed.

The`executor`parameter is an`ExecutorService`that creates new threads as needed to execute tasks that are submitted to handle I/O events and dispatch completion results for operations initiated on asynchronous channels in the group. It may reuse previously constructed threads when they are available.

The`initialSize`parameter may be used by the implementation as a*hint*as to the initial number of tasks it may submit. For example, it may be used to indicate the initial number of threads that wait on I/O events.

The executor is intended to be used exclusively by the resulting asynchronous channel group. Termination of the group results in the orderly [shutdown](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService.html#shutdown())of the executor service. Shutting down the executor service by other means results in unspecified behavior.

The group is created by invoking the [openAsynchronousChannelGroup(ExecutorService,int)](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AsynchronousChannelProvider#openAsynchronousChannelGroup(java.util.concurrent.ExecutorService,%20kotlin.Int))method of the system-wide default [AsynchronousChannelProvider](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AsynchronousChannelProvider) object.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [ExecutorService](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService.html#)!:The thread pool for the resulting group |
| `initialSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A value`>=0`or a negative value for implementation specific default |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| [AsynchronousChannelGroup](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup#)! | A new asynchronous channel group |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |

**See Also**

### withFixedThreadPool

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun withFixedThreadPool(
    nThreads: Int, 
    threadFactory: ThreadFactory!
): AsynchronousChannelGroup!
```

Creates an asynchronous channel group with a fixed thread pool.

The resulting asynchronous channel group reuses a fixed number of threads. At any point, at most`nThreads`threads will be active processing tasks that are submitted to handle I/O events and dispatch completion results for operations initiated on asynchronous channels in the group.

The group is created by invoking the [openAsynchronousChannelGroup(int,ThreadFactory)](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AsynchronousChannelProvider#openAsynchronousChannelGroup(kotlin.Int,%20java.util.concurrent.ThreadFactory))method of the system-wide default [AsynchronousChannelProvider](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AsynchronousChannelProvider) object.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `nThreads` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of threads in the pool |
| `threadFactory` | [ThreadFactory](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadFactory.html#)!:The factory to use when creating new threads |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| [AsynchronousChannelGroup](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup#)! | A new asynchronous channel group |

| Exceptions ||
|--------------------------------------|------------------------|
| `java.lang.IllegalArgumentException` | If`nThreads <= 0` |
| `java.io.IOException` | If an I/O error occurs |

### withThreadPool

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun withThreadPool(executor: ExecutorService!): AsynchronousChannelGroup!
```

Creates an asynchronous channel group with a given thread pool.

The`executor`parameter is an`ExecutorService`that executes tasks submitted to dispatch completion results for operations initiated on asynchronous channels in the group.

Care should be taken when configuring the executor service. It should support*direct handoff* or*unbounded queuing* of submitted tasks, and the thread that invokes the [execute](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#execute(java.lang.Runnable))method should never invoke the task directly. An implementation may mandate additional constraints.

The executor is intended to be used exclusively by the resulting asynchronous channel group. Termination of the group results in the orderly [shutdown](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService.html#shutdown())of the executor service. Shutting down the executor service by other means results in unspecified behavior.

The group is created by invoking the [openAsynchronousChannelGroup(ExecutorService,int)](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AsynchronousChannelProvider#openAsynchronousChannelGroup(java.util.concurrent.ExecutorService,%20kotlin.Int))method of the system-wide default [AsynchronousChannelProvider](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AsynchronousChannelProvider) object with an`initialSize`of`0`.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [ExecutorService](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService.html#)!:The thread pool for the resulting group |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| [AsynchronousChannelGroup](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup#)! | A new asynchronous channel group |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |
