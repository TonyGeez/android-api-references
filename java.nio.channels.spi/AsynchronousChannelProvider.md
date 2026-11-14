Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AsynchronousChannelProvider

```
abstract class AsynchronousChannelProvider
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.nio.channels.spi.AsynchronousChannelProvider](../java/nio/channels/spi/AsynchronousChannelProvider.md) |

Service-provider class for asynchronous channels.

An asynchronous channel provider is a concrete subclass of this class that has a zero-argument constructor and implements the abstract methods specified below. A given invocation of the Java virtual machine maintains a single system-wide default provider instance, which is returned by the `https://developer.android.com/reference/kotlin/java/nio/channels/spi/AsynchronousChannelProvider#provider()` method. The first invocation of that method will locate the default provider as specified below.

All of the methods in this class are safe for use by multiple concurrent threads.

## Summary

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/channels/spi/AsynchronousChannelProvider#AsynchronousChannelProvider()()` Initializes a new instance of this class. |

| Public methods ||
|---|---|
| abstract [AsynchronousChannelGroup](../java/nio/channels/AsynchronousChannelGroup.md)! | `https://developer.android.com/reference/kotlin/java/nio/channels/spi/AsynchronousChannelProvider#openAsynchronousChannelGroup(kotlin.Int,%20java.util.concurrent.ThreadFactory)(nThreads: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, threadFactory: https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadFactory.html#!)` Constructs a new asynchronous channel group with a fixed thread pool. |
| abstract [AsynchronousChannelGroup](../java/nio/channels/AsynchronousChannelGroup.md)! | `https://developer.android.com/reference/kotlin/java/nio/channels/spi/AsynchronousChannelProvider#openAsynchronousChannelGroup(java.util.concurrent.ExecutorService,%20kotlin.Int)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService.html#!, initialSize: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Constructs a new asynchronous channel group with the given thread pool. |
| abstract [AsynchronousServerSocketChannel](../java/nio/channels/AsynchronousServerSocketChannel.md)! | `https://developer.android.com/reference/kotlin/java/nio/channels/spi/AsynchronousChannelProvider#openAsynchronousServerSocketChannel(java.nio.channels.AsynchronousChannelGroup)(group: https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup.html#!)` Opens an asynchronous server-socket channel. |
| --- | --- |
| abstract [AsynchronousSocketChannel](../java/nio/channels/AsynchronousSocketChannel.md)! | `https://developer.android.com/reference/kotlin/java/nio/channels/spi/AsynchronousChannelProvider#openAsynchronousSocketChannel(java.nio.channels.AsynchronousChannelGroup)(group: https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup.html#!)` Opens an asynchronous socket channel. |
| open static [AsynchronousChannelProvider](../java/nio/channels/spi/AsynchronousChannelProvider.md)! | `https://developer.android.com/reference/kotlin/java/nio/channels/spi/AsynchronousChannelProvider#provider()()` Returns the system-wide default asynchronous channel provider for this invocation of the Java virtual machine. |

## Protected constructors

### AsynchronousChannelProvider

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected AsynchronousChannelProvider()
```

Initializes a new instance of this class.

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager has been installed and it denies `https://developer.android.com/reference/kotlin/java/lang/RuntimePermission.html#``("asynchronousChannelProvider")` |

## Public methods

### openAsynchronousChannelGroup

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun openAsynchronousChannelGroup(
    nThreads: Int, 
    threadFactory: ThreadFactory!
): AsynchronousChannelGroup!
```

Constructs a new asynchronous channel group with a fixed thread pool.

| Parameters ||
|---|---|
| `nThreads` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of threads in the pool |
| `threadFactory` | [ThreadFactory](../java/util/concurrent/ThreadFactory.md)!: The factory to use when creating new threads |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup.html#!` | A new asynchronous channel group |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |
| `java.lang.IllegalArgumentException` | If `nThreads <= 0` |

**See Also**

- `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup.html#withFixedThreadPool(kotlin.Int,%20java.util.concurrent.ThreadFactory)`

### openAsynchronousChannelGroup

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun openAsynchronousChannelGroup(
    executor: ExecutorService!, 
    initialSize: Int
): AsynchronousChannelGroup!
```

Constructs a new asynchronous channel group with the given thread pool.

| Parameters ||
|---|---|
| `executor` | [ExecutorService](../java/util/concurrent/ExecutorService.md)!: The thread pool |
| `initialSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A value `>=0` or a negative value for implementation specific default |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup.html#!` | A new asynchronous channel group |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |

**See Also**

- `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup.html#withCachedThreadPool(java.util.concurrent.ExecutorService,%20kotlin.Int)`

### openAsynchronousServerSocketChannel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun openAsynchronousServerSocketChannel(group: AsynchronousChannelGroup!): AsynchronousServerSocketChannel!
```

Opens an asynchronous server-socket channel.

| Parameters ||
|---|---|
| `group` | [AsynchronousChannelGroup](../java/nio/channels/AsynchronousChannelGroup.md)!: The group to which the channel is bound, or `null` to bind to the default group |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousServerSocketChannel.html#!` | The new channel |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |
| `java.nio.channels.IllegalChannelGroupException` | If the provider that created the group differs from this provider |
| `java.nio.channels.ShutdownChannelGroupException` | The group is shutdown |
| --- | --- |

### openAsynchronousSocketChannel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun openAsynchronousSocketChannel(group: AsynchronousChannelGroup!): AsynchronousSocketChannel!
```

Opens an asynchronous socket channel.

| Parameters ||
|---|---|
| `group` | [AsynchronousChannelGroup](../java/nio/channels/AsynchronousChannelGroup.md)!: The group to which the channel is bound, or `null` to bind to the default group |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel.html#!` | The new channel |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |
| `java.nio.channels.IllegalChannelGroupException` | If the provider that created the group differs from this provider |
| `java.nio.channels.ShutdownChannelGroupException` | The group is shutdown |
| --- | --- |

### provider

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun provider(): AsynchronousChannelProvider!
```

Returns the system-wide default asynchronous channel provider for this invocation of the Java virtual machine.

The first invocation of this method locates the default provider object as follows:

1. If the system property `java.nio.channels.spi.AsynchronousChannelProvider` is defined then it is taken to be the fully-qualified name of a concrete provider class. The class is loaded and instantiated; if this process fails then an unspecified error is thrown.
2. If a provider class has been installed in a jar file that is visible to the system class loader, and that jar file contains a provider-configuration file named `java.nio.channels.spi.AsynchronousChannelProvider` in the resource directory `META-INF/services`, then the first class name specified in that file is taken. The class is loaded and instantiated; if this process fails then an unspecified error is thrown.
3. Finally, if no provider has been specified by any of the above means then the system-default provider class is instantiated and the result is returned.

Subsequent invocations of this method return the provider that was returned by the first invocation.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/channels/spi/AsynchronousChannelProvider#!` | The system-wide default AsynchronousChannel provider |
