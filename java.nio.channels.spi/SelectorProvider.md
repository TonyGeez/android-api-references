Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SelectorProvider

```
abstract class SelectorProvider
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.nio.channels.spi.SelectorProvider](../java/nio/channels/spi/SelectorProvider.md) |

Service-provider class for selectors and selectable channels.

A selector provider is a concrete subclass of this class that has a zero-argument constructor and implements the abstract methods specified below. A given invocation of the Java virtual machine maintains a single system-wide default provider instance, which is returned by the `https://developer.android.com/reference/kotlin/java/nio/channels/spi/SelectorProvider#provider()` method. The first invocation of that method will locate the default provider as specified below.

The system-wide default provider is used by the static `open` methods of the java.nio.channels.DatagramChannel#open, `https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.html#open()`, `https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#open()`, `https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel.html#open()`, and java.nio.channels.SocketChannel#open classes. It is also used by the `https://developer.android.com/reference/kotlin/java/lang/System.html#inheritedChannel()` method. A program may make use of a provider other than the default provider by instantiating that provider and then directly invoking the `open` methods defined in this class.

All of the methods in this class are safe for use by multiple concurrent threads.

## Summary

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/channels/spi/SelectorProvider#SelectorProvider()()` Initializes a new instance of this class. |

| Public methods ||
|---|---|
| open [Channel](../java/nio/channels/Channel.md)! | `https://developer.android.com/reference/kotlin/java/nio/channels/spi/SelectorProvider#inheritedChannel()()` Returns the channel inherited from the entity that created this Java virtual machine. |
| abstract [DatagramChannel](../java/nio/channels/DatagramChannel.md)! | `https://developer.android.com/reference/kotlin/java/nio/channels/spi/SelectorProvider#openDatagramChannel()()` Opens a datagram channel. |
| abstract [DatagramChannel](../java/nio/channels/DatagramChannel.md)! | `https://developer.android.com/reference/kotlin/java/nio/channels/spi/SelectorProvider#openDatagramChannel(java.net.ProtocolFamily)(family: https://developer.android.com/reference/kotlin/java/net/ProtocolFamily.html#!)` Opens a datagram channel. |
| --- | --- |
| abstract [Pipe](../java/nio/channels/Pipe.md)! | `https://developer.android.com/reference/kotlin/java/nio/channels/spi/SelectorProvider#openPipe()()` Opens a pipe. |
| abstract [AbstractSelector](../java/nio/channels/spi/AbstractSelector.md)! | `https://developer.android.com/reference/kotlin/java/nio/channels/spi/SelectorProvider#openSelector()()` Opens a selector. |
| abstract [ServerSocketChannel](../java/nio/channels/ServerSocketChannel.md)! | `https://developer.android.com/reference/kotlin/java/nio/channels/spi/SelectorProvider#openServerSocketChannel()()` Opens a server-socket channel. |
| --- | --- |
| abstract [SocketChannel](../java/nio/channels/SocketChannel.md)! | `https://developer.android.com/reference/kotlin/java/nio/channels/spi/SelectorProvider#openSocketChannel()()` Opens a socket channel. |
| open static [SelectorProvider](../java/nio/channels/spi/SelectorProvider.md)! | `https://developer.android.com/reference/kotlin/java/nio/channels/spi/SelectorProvider#provider()()` Returns the system-wide default selector provider for this invocation of the Java virtual machine. |

## Protected constructors

### SelectorProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected SelectorProvider()
```

Initializes a new instance of this class.

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager has been installed and it denies `https://developer.android.com/reference/kotlin/java/lang/RuntimePermission.html#``("selectorProvider")` |

## Public methods

### inheritedChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun inheritedChannel(): Channel!
```

Returns the channel inherited from the entity that created this Java virtual machine.

On many operating systems a process, such as a Java virtual machine, can be started in a manner that allows the process to inherit a channel from the entity that created the process. The manner in which this is done is system dependent, as are the possible entities to which the channel may be connected. For example, on UNIX systems, the Internet services daemon (*inetd*) is used to start programs to service requests when a request arrives on an associated network port. In this example, the process that is started, inherits a channel representing a network socket.

In cases where the inherited channel represents a network socket then the `https://developer.android.com/reference/kotlin/java/nio/channels/Channel.html#` type returned by this method is determined as follows:

- If the inherited channel represents a stream-oriented connected socket then a `https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel.html#` is returned. The socket channel is, at least initially, in blocking mode, bound to a socket address, and connected to a peer.
- If the inherited channel represents a stream-oriented listening socket then a `https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel.html#` is returned. The server-socket channel is, at least initially, in blocking mode, and bound to a socket address.
- If the inherited channel is a datagram-oriented socket then a `https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel.html#` is returned. The datagram channel is, at least initially, in blocking mode, and bound to a socket address.

In addition to the network-oriented channels described, this method may return other kinds of channels in the future.

The first invocation of this method creates the channel that is returned. Subsequent invocations of this method return the same channel.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/channels/Channel.html#!` | The inherited channel, if any, otherwise `null`. |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |
| `java.lang.SecurityException` | If a security manager has been installed and it denies `https://developer.android.com/reference/kotlin/java/lang/RuntimePermission.html#``("inheritedChannel")` |

### openDatagramChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun openDatagramChannel(): DatagramChannel!
```

Opens a datagram channel.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel.html#!` | The new channel |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |

### openDatagramChannel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun openDatagramChannel(family: ProtocolFamily!): DatagramChannel!
```

Opens a datagram channel.

| Parameters ||
|---|---|
| `family` | [ProtocolFamily](../java/net/ProtocolFamily.md)!: The protocol family |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel.html#!` | A new datagram channel |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |
| `java.lang.UnsupportedOperationException` | If the specified protocol family is not supported |

### openPipe

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun openPipe(): Pipe!
```

Opens a pipe.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.html#!` | The new pipe |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |

### openSelector

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun openSelector(): AbstractSelector!
```

Opens a selector.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelector!` | The new selector |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |

### openServerSocketChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun openServerSocketChannel(): ServerSocketChannel!
```

Opens a server-socket channel.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel.html#!` | The new channel |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |

### openSocketChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun openSocketChannel(): SocketChannel!
```

Opens a socket channel.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel.html#!` | The new channel |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |

### provider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun provider(): SelectorProvider!
```

Returns the system-wide default selector provider for this invocation of the Java virtual machine.

The first invocation of this method locates the default provider object as follows:

1. If the system property `java.nio.channels.spi.SelectorProvider` is defined then it is taken to be the fully-qualified name of a concrete provider class. The class is loaded and instantiated; if this process fails then an unspecified error is thrown.
2. If a provider class has been installed in a jar file that is visible to the system class loader, and that jar file contains a provider-configuration file named `java.nio.channels.spi.SelectorProvider` in the resource directory `META-INF/services`, then the first class name specified in that file is taken. The class is loaded and instantiated; if this process fails then an unspecified error is thrown.
3. Finally, if no provider has been specified by any of the above means then the system-default provider class is instantiated and the result is returned.

Subsequent invocations of this method return the provider that was returned by the first invocation.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/channels/spi/SelectorProvider#!` | The system-wide default selector provider |
