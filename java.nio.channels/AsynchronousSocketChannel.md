Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AsynchronousSocketChannel

```
abstract class AsynchronousSocketChannel : AsynchronousByteChannel, NetworkChannel
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.nio.channels.AsynchronousSocketChannel](../java/nio/channels/AsynchronousSocketChannel.md) |

An asynchronous channel for stream-oriented connecting sockets.

Asynchronous socket channels are created in one of two ways. A newly-created `AsynchronousSocketChannel` is created by invoking one of the #open methods defined by this class. A newly-created channel is open but not yet connected. A connected `AsynchronousSocketChannel` is created when a connection is made to the socket of an `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousServerSocketChannel`. It is not possible to create an asynchronous socket channel for an arbitrary, pre-existing `https://developer.android.com/reference/kotlin/java/net/Socket.html#`.

A newly-created channel is connected by invoking its #connect method; once connected, a channel remains connected until it is closed. Whether or not a socket channel is connected may be determined by invoking its `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel#getRemoteAddress()` method. An attempt to invoke an I/O operation upon an unconnected channel will cause a `https://developer.android.com/reference/kotlin/java/nio/channels/NotYetConnectedException` to be thrown.

Channels of this type are safe for use by multiple concurrent threads. They support concurrent reading and writing, though at most one read operation and one write operation can be outstanding at any time. If a thread initiates a read operation before a previous read operation has completed then a `https://developer.android.com/reference/kotlin/java/nio/channels/ReadPendingException` will be thrown. Similarly, an attempt to initiate a write operation before a previous write has completed will throw a `https://developer.android.com/reference/kotlin/java/nio/channels/WritePendingException`.

Socket options are configured using the `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel#setOption(java.net.SocketOption,%20java.nio.channels.AsynchronousSocketChannel.setOption.T)` method. Asynchronous socket channels support the following options:

| Option Name | Description |
| --- | --- |
| `https://developer.android.com/reference/kotlin/java/net/StandardSocketOptions.html#SO_SNDBUF:java.net.SocketOption` | The size of the socket send buffer |
| `https://developer.android.com/reference/kotlin/java/net/StandardSocketOptions.html#SO_RCVBUF:java.net.SocketOption` | The size of the socket receive buffer |
| `https://developer.android.com/reference/kotlin/java/net/StandardSocketOptions.html#SO_KEEPALIVE:java.net.SocketOption` | Keep connection alive |
| --- | --- |
| `https://developer.android.com/reference/kotlin/java/net/StandardSocketOptions.html#SO_REUSEADDR:java.net.SocketOption` | Re-use address |
| `https://developer.android.com/reference/kotlin/java/net/StandardSocketOptions.html#TCP_NODELAY:java.net.SocketOption` | Disable the Nagle algorithm |
|---|---|

Additional (implementation specific) options may also be supported.

## Timeouts

The `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel#read(java.nio.ByteBuffer,%20kotlin.Long,%20java.util.concurrent.TimeUnit,%20java.nio.channels.AsynchronousSocketChannel.read.A,%20java.nio.channels.CompletionHandler)` and `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel#write(java.nio.ByteBuffer,%20kotlin.Long,%20java.util.concurrent.TimeUnit,%20java.nio.channels.AsynchronousSocketChannel.write.A,%20java.nio.channels.CompletionHandler)` methods defined by this class allow a timeout to be specified when initiating a read or write operation. If the timeout elapses before an operation completes then the operation completes with the exception `https://developer.android.com/reference/kotlin/java/nio/channels/InterruptedByTimeoutException`. A timeout may leave the channel, or the underlying connection, in an inconsistent state. Where the implementation cannot guarantee that bytes have not been read from the channel then it puts the channel into an implementation specific *error state* . A subsequent attempt to initiate a `read` operation causes an unspecified runtime exception to be thrown. Similarly if a `write` operation times out and the implementation cannot guarantee bytes have not been written to the channel then further attempts to `write` to the channel cause an unspecified runtime exception to be thrown. When a timeout elapses then the state of the `https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#`, or the sequence of buffers, for the I/O operation is not defined. Buffers should be discarded or at least care must be taken to ensure that the buffers are not accessed while the channel remains open. All methods that accept timeout parameters treat values less than or equal to zero to mean that the I/O operation does not timeout.

## Summary

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel#AsynchronousSocketChannel(java.nio.channels.spi.AsynchronousChannelProvider)(provider: https://developer.android.com/reference/kotlin/java/nio/channels/spi/AsynchronousChannelProvider!)` Initializes a new instance of this class. |

| Public methods ||
|---|---|
| abstract [AsynchronousSocketChannel](../java/nio/channels/AsynchronousSocketChannel.md)! | `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel#bind(java.net.SocketAddress)(local: https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#!)` <br /> |
| abstract [Future](../java/util/concurrent/Future.md)\< [Void](../java/lang/Void.md)!\>! | `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel#connect(java.net.SocketAddress)(remote: https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#!)` Connects this channel. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel#connect(java.net.SocketAddress,%20java.nio.channels.AsynchronousSocketChannel.connect.A,%20java.nio.channels.CompletionHandler)(remote: https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#!, attachment: A, handler: https://developer.android.com/reference/kotlin/java/nio/channels/CompletionHandler<https://developer.android.com/reference/kotlin/java/lang/Void.html#!, in A>!)` Connects this channel. |
| --- | --- |
| abstract [SocketAddress](../java/net/SocketAddress.md)! | `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel#getLocalAddress()()` Returns the socket address that this channel's socket is bound to. |
| abstract [SocketAddress](../java/net/SocketAddress.md)! | `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel#getRemoteAddress()()` Returns the remote address to which this channel's socket is connected. |
| open static [AsynchronousSocketChannel](../java/nio/channels/AsynchronousSocketChannel.md)! | `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel#open()()` Opens an asynchronous socket channel. |
| --- | --- |
| open static [AsynchronousSocketChannel](../java/nio/channels/AsynchronousSocketChannel.md)! | `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel#open(java.nio.channels.AsynchronousChannelGroup)(group: https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup!)` Opens an asynchronous socket channel. |
| [AsynchronousChannelProvider](../java/nio/channels/spi/AsynchronousChannelProvider.md)! | `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel#provider()()` Returns the provider that created this channel. |
| abstract [Future](../java/util/concurrent/Future.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>! | `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel#read(java.nio.ByteBuffer)(dst: https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#!)` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel#read(java.nio.ByteBuffer,%20java.nio.channels.AsynchronousSocketChannel.read.A,%20java.nio.channels.CompletionHandler)(dst: https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#!, attachment: A, handler: https://developer.android.com/reference/kotlin/java/nio/channels/CompletionHandler<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!, in A>!)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel#read(java.nio.ByteBuffer,%20kotlin.Long,%20java.util.concurrent.TimeUnit,%20java.nio.channels.AsynchronousSocketChannel.read.A,%20java.nio.channels.CompletionHandler)(dst: https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#!, timeout: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, unit: https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit.html#!, attachment: A, handler: https://developer.android.com/reference/kotlin/java/nio/channels/CompletionHandler<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!, in A>!)` Reads a sequence of bytes from this channel into the given buffer. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel#read(kotlin.Array,%20kotlin.Int,%20kotlin.Int,%20kotlin.Long,%20java.util.concurrent.TimeUnit,%20java.nio.channels.AsynchronousSocketChannel.read.A,%20java.nio.channels.CompletionHandler)(dsts: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#!>!, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, length: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, timeout: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, unit: https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit.html#!, attachment: A, handler: https://developer.android.com/reference/kotlin/java/nio/channels/CompletionHandler<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html!, in A>!)` Reads a sequence of bytes from this channel into a subsequence of the given buffers. |
| --- | --- |
| abstract [AsynchronousSocketChannel](../java/nio/channels/AsynchronousSocketChannel.md)! | `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel#setOption(java.net.SocketOption,%20java.nio.channels.AsynchronousSocketChannel.setOption.T)(name: https://developer.android.com/reference/kotlin/java/net/SocketOption.html#<T>!, value: T)` <br /> |
| abstract [AsynchronousSocketChannel](../java/nio/channels/AsynchronousSocketChannel.md)! | `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel#shutdownInput()()` Shutdown the connection for reading without closing the channel. |
| abstract [AsynchronousSocketChannel](../java/nio/channels/AsynchronousSocketChannel.md)! | `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel#shutdownOutput()()` Shutdown the connection for writing without closing the channel. |
| --- | --- |
| abstract [Future](../java/util/concurrent/Future.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>! | `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel#write(java.nio.ByteBuffer)(src: https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#!)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel#write(java.nio.ByteBuffer,%20java.nio.channels.AsynchronousSocketChannel.write.A,%20java.nio.channels.CompletionHandler)(src: https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#!, attachment: A, handler: https://developer.android.com/reference/kotlin/java/nio/channels/CompletionHandler<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!, in A>!)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel#write(java.nio.ByteBuffer,%20kotlin.Long,%20java.util.concurrent.TimeUnit,%20java.nio.channels.AsynchronousSocketChannel.write.A,%20java.nio.channels.CompletionHandler)(src: https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#!, timeout: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, unit: https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit.html#!, attachment: A, handler: https://developer.android.com/reference/kotlin/java/nio/channels/CompletionHandler<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!, in A>!)` Writes a sequence of bytes to this channel from the given buffer. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel#write(kotlin.Array,%20kotlin.Int,%20kotlin.Int,%20kotlin.Long,%20java.util.concurrent.TimeUnit,%20java.nio.channels.AsynchronousSocketChannel.write.A,%20java.nio.channels.CompletionHandler)(srcs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#!>!, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, length: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, timeout: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, unit: https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit.html#!, attachment: A, handler: https://developer.android.com/reference/kotlin/java/nio/channels/CompletionHandler<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html!, in A>!)` Writes a sequence of bytes to this channel from a subsequence of the given buffers. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/nio/channels/Channel` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/nio/channels/Channel#close()()` Closes this channel. After a channel is closed, any further attempt to invoke I/O operations upon it will cause a `https://developer.android.com/reference/kotlin/java/nio/channels/ClosedChannelException` to be thrown. If this channel is already closed then invoking this method has no effect. This method may be invoked at any time. If some other thread has already invoked it, however, then another invocation will block until the first invocation is complete, after which it will return without effect. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/nio/channels/Channel#isOpen()()` Tells whether or not this channel is open. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel` |---|---| | `T` | `https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel#getOption(java.net.SocketOption)(name: https://developer.android.com/reference/kotlin/java/net/SocketOption.html#<T>!)` Returns the value of a socket option. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/java/net/SocketOption.html#<*>!>!` | `https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel#supportedOptions()()` Returns a set of the socket options supported by this channel. This method will continue to return the set of options even after the channel has been closed. <br /> | ||

## Protected constructors

### AsynchronousSocketChannel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected AsynchronousSocketChannel(provider: AsynchronousChannelProvider!)
```

Initializes a new instance of this class.

| Parameters ||
|---|---|
| `provider` | [AsynchronousChannelProvider](../java/nio/channels/spi/AsynchronousChannelProvider.md)!: The provider that created this channel |

## Public methods

### bind

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun bind(local: SocketAddress!): AsynchronousSocketChannel!
```

| Parameters ||
|---|---|
| `local` | [SocketAddress](../java/net/SocketAddress.md)!: The address to bind the socket, or `null` to bind the socket to an automatically assigned socket address |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel#!` | This channel |

| Exceptions ||
|---|---|
| `java.io.IOException` | If some other I/O error occurs |
| `java.lang.SecurityException` | If a security manager has been installed and its `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkListen(kotlin.Int)` method denies the operation |
| `java.nio.channels.AlreadyBoundException` | If the socket is already bound |
| --- | --- |
| `java.nio.channels.ClosedChannelException` | If the channel is closed |
| `java.nio.channels.UnsupportedAddressTypeException` | If the type of the given address is not supported |
| `java.nio.channels.ConnectionPendingException` | If a connection operation is already in progress on this channel |
| --- | --- |

### connect

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun connect(remote: SocketAddress!): Future<Void!>!
```

Connects this channel.

This method initiates an operation to connect this channel. This method behaves in exactly the same manner as the `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel#connect(java.net.SocketAddress,%20java.nio.channels.AsynchronousSocketChannel.connect.A,%20java.nio.channels.CompletionHandler)` method except that instead of specifying a completion handler, this method returns a `Future` representing the pending result. The `Future`'s `https://developer.android.com/reference/kotlin/java/util/concurrent/Future.html#get()` method returns `null` on successful completion.

| Parameters ||
|---|---|
| `remote` | [SocketAddress](../java/net/SocketAddress.md)!: The remote address to which this channel is to be connected |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/Future.html#<https://developer.android.com/reference/kotlin/java/lang/Void.html#!>!` | A `Future` object representing the pending result |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager has been installed and it does not permit access to the given remote endpoint |
| `java.nio.channels.AlreadyConnectedException` | If this channel is already connected |
| `java.nio.channels.ConnectionPendingException` | If a connection operation is already in progress on this channel |
| --- | --- |
| `java.nio.channels.UnresolvedAddressException` | If the given remote address is not fully resolved |
| `java.nio.channels.UnsupportedAddressTypeException` | If the type of the given remote address is not supported |

### connect

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun <A : Any!> connect(
    remote: SocketAddress!, 
    attachment: A, 
    handler: CompletionHandler<Void!, in A>!
): Unit
```

Connects this channel.

This method initiates an operation to connect this channel. The `handler` parameter is a completion handler that is invoked when the connection is successfully established or connection cannot be established. If the connection cannot be established then the channel is closed.

This method performs exactly the same security checks as the `https://developer.android.com/reference/kotlin/java/net/Socket.html#` class. That is, if a security manager has been installed then this method verifies that its java.lang.SecurityManager#checkConnect method permits connecting to the address and port number of the given remote endpoint.

| Parameters ||
|---|---|
| `<A>` | The type of the attachment |
| `remote` | [SocketAddress](../java/net/SocketAddress.md)!: The remote address to which this channel is to be connected |
| `attachment` | A: The object to attach to the I/O operation; can be `null` |
| --- | --- |
| `handler` | [CompletionHandler](../java/nio/channels/CompletionHandler.md)\< [Void](../java/lang/Void.md)!, in A\>!: The handler for consuming the result |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager has been installed and it does not permit access to the given remote endpoint |
| `java.nio.channels.AlreadyConnectedException` | If this channel is already connected |
| `java.nio.channels.ConnectionPendingException` | If a connection operation is already in progress on this channel |
| --- | --- |
| `java.nio.channels.ShutdownChannelGroupException` | If the channel group has terminated |
| `java.nio.channels.UnresolvedAddressException` | If the given remote address is not fully resolved |
| `java.nio.channels.UnsupportedAddressTypeException` | If the type of the given remote address is not supported |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel#getRemoteAddress()`

### getLocalAddress

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getLocalAddress(): SocketAddress!
```

Returns the socket address that this channel's socket is bound to.

Where the channel is `https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel#bind(java.net.SocketAddress)` to an Internet Protocol socket address then the return value from this method is of type `https://developer.android.com/reference/kotlin/java/net/InetSocketAddress.html#`.

If there is a security manager set, its `checkConnect` method is called with the local address and `-1` as its arguments to see if the operation is allowed. If the operation is not allowed, a `SocketAddress` representing the `https://developer.android.com/reference/kotlin/java/net/InetAddress.html#getLoopbackAddress()` address and the local port of the channel's socket is returned.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#!` | The `SocketAddress` that the socket is bound to, or the `SocketAddress` representing the loopback address if denied by the security manager, or `null` if the channel's socket is not bound |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |
| `java.nio.channels.ClosedChannelException` | If the channel is closed |

### getRemoteAddress

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getRemoteAddress(): SocketAddress!
```

Returns the remote address to which this channel's socket is connected.

Where the channel is bound and connected to an Internet Protocol socket address then the return value from this method is of type `https://developer.android.com/reference/kotlin/java/net/InetSocketAddress.html#`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#!` | The remote address; `null` if the channel's socket is not connected |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |
| `java.nio.channels.ClosedChannelException` | If the channel is closed |

### open

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun open(): AsynchronousSocketChannel!
```

Opens an asynchronous socket channel.

This method returns an asynchronous socket channel that is bound to the *default group*.This method is equivalent to evaluating the expression:

```kotlin
open((AsynchronousChannelGroup)null);
  
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel#!` | A new asynchronous socket channel |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |

### open

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun open(group: AsynchronousChannelGroup!): AsynchronousSocketChannel!
```

Opens an asynchronous socket channel.

The new channel is created by invoking the `https://developer.android.com/reference/kotlin/java/nio/channels/spi/AsynchronousChannelProvider#openAsynchronousSocketChannel(java.nio.channels.AsynchronousChannelGroup)` method on the `https://developer.android.com/reference/kotlin/java/nio/channels/spi/AsynchronousChannelProvider` that created the group. If the group parameter is `null` then the resulting channel is created by the system-wide default provider, and bound to the *default group*.

| Parameters ||
|---|---|
| `group` | [AsynchronousChannelGroup](../java/nio/channels/AsynchronousChannelGroup.md)!: The group to which the newly constructed channel should be bound, or `null` for the default group |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel#!` | A new asynchronous socket channel |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |
| `java.nio.channels.ShutdownChannelGroupException` | If the channel group is shutdown |

### provider

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun provider(): AsynchronousChannelProvider!
```

Returns the provider that created this channel.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/channels/spi/AsynchronousChannelProvider!` | The provider that created this channel |

### read

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun read(dst: ByteBuffer!): Future<Int!>!
```

| Parameters ||
|---|---|
| `dst` | [ByteBuffer](../java/nio/ByteBuffer.md)!: The buffer into which bytes are to be transferred |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/Future.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>!` | A Future representing the result of the operation |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the buffer is read-only |
| `java.nio.channels.ReadPendingException` | If the channel does not allow more than one read to be outstanding and a previous read has not completed |
| `java.nio.channels.NotYetConnectedException` | If this channel is not yet connected |
| --- | --- |

### read

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <A : Any!> read(
    dst: ByteBuffer!, 
    attachment: A, 
    handler: CompletionHandler<Int!, in A>!
): Unit
```

| Parameters ||
|---|---|
| `<A>` | The type of the attachment |
| `dst` | [ByteBuffer](../java/nio/ByteBuffer.md)!: The buffer into which bytes are to be transferred |
| `attachment` | A: The object to attach to the I/O operation; can be `null` |
| --- | --- |
| `handler` | [CompletionHandler](../java/nio/channels/CompletionHandler.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!, in A\>!: The completion handler |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the buffer is read-only |
| `java.nio.channels.ReadPendingException` | If the channel does not allow more than one read to be outstanding and a previous read has not completed |
| `java.nio.channels.ShutdownChannelGroupException` | If the channel group has terminated |
| --- | --- |
| `java.nio.channels.NotYetConnectedException` | If this channel is not yet connected |

### read

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun <A : Any!> read(
    dst: ByteBuffer!, 
    timeout: Long, 
    unit: TimeUnit!, 
    attachment: A, 
    handler: CompletionHandler<Int!, in A>!
): Unit
```

Reads a sequence of bytes from this channel into the given buffer.

This method initiates an asynchronous read operation to read a sequence of bytes from this channel into the given buffer. The `handler` parameter is a completion handler that is invoked when the read operation completes (or fails). The result passed to the completion handler is the number of bytes read or `-1` if no bytes could be read because the channel has reached end-of-stream.

If a timeout is specified and the timeout elapses before the operation completes then the operation completes with the exception `https://developer.android.com/reference/kotlin/java/nio/channels/InterruptedByTimeoutException`. Where a timeout occurs, and the implementation cannot guarantee that bytes have not been read, or will not be read from the channel into the given buffer, then further attempts to read from the channel will cause an unspecific runtime exception to be thrown.

Otherwise this method works in the same manner as the `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousByteChannel#read(java.nio.ByteBuffer,%20java.nio.channels.AsynchronousByteChannel.read.A,%20java.nio.channels.CompletionHandler)` method.

| Parameters ||
|---|---|
| `<A>` | The type of the attachment |
| `dst` | [ByteBuffer](../java/nio/ByteBuffer.md)!: The buffer into which bytes are to be transferred |
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The maximum time for the I/O operation to complete |
| --- | --- |
| `unit` | [TimeUnit](../java/util/concurrent/TimeUnit.md)!: The time unit of the `timeout` argument |
| `attachment` | A: The object to attach to the I/O operation; can be `null` |
| `handler` | [CompletionHandler](../java/nio/channels/CompletionHandler.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!, in A\>!: The handler for consuming the result |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the buffer is read-only |
| `java.nio.channels.NotYetConnectedException` | If this channel is not yet connected |
| `java.nio.channels.ReadPendingException` | If a read operation is already in progress on this channel |
| --- | --- |
| `java.nio.channels.ShutdownChannelGroupException` | If the channel group has terminated |

### read

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun <A : Any!> read(
    dsts: Array<ByteBuffer!>!, 
    offset: Int, 
    length: Int, 
    timeout: Long, 
    unit: TimeUnit!, 
    attachment: A, 
    handler: CompletionHandler<Long!, in A>!
): Unit
```

Reads a sequence of bytes from this channel into a subsequence of the given buffers. This operation, sometimes called a *scattering read* , is often useful when implementing network protocols that group data into segments consisting of one or more fixed-length headers followed by a variable-length body. The `handler` parameter is a completion handler that is invoked when the read operation completes (or fails). The result passed to the completion handler is the number of bytes read or `-1` if no bytes could be read because the channel has reached end-of-stream.

This method initiates a read of up to *r* bytes from this channel, where *r* is the total number of bytes remaining in the specified subsequence of the given buffer array, that is,

```kotlin
dsts[offset].remaining()
      + dsts[offset+1].remaining()
      + ... + dsts[offset+length-1].remaining()
```
at the moment that the read is attempted.

Suppose that a byte sequence of length *n* is read, where `0` `<` *n* `<=` *r* . Up to the first `dsts[offset].remaining()` bytes of this sequence are transferred into buffer `dsts[offset]`, up to the next `dsts[offset+1].remaining()` bytes are transferred into buffer `dsts[offset+1]`, and so forth, until the entire byte sequence is transferred into the given buffers. As many bytes as possible are transferred into each buffer, hence the final position of each updated buffer, except the last updated buffer, is guaranteed to be equal to that buffer's limit. The underlying operating system may impose a limit on the number of buffers that may be used in an I/O operation. Where the number of buffers (with bytes remaining), exceeds this limit, then the I/O operation is performed with the maximum number of buffers allowed by the operating system.

If a timeout is specified and the timeout elapses before the operation completes then it completes with the exception `https://developer.android.com/reference/kotlin/java/nio/channels/InterruptedByTimeoutException`. Where a timeout occurs, and the implementation cannot guarantee that bytes have not been read, or will not be read from the channel into the given buffers, then further attempts to read from the channel will cause an unspecific runtime exception to be thrown.

| Parameters ||
|---|---|
| `<A>` | The type of the attachment |
| `dsts` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ByteBuffer](../java/nio/ByteBuffer.md)!\>!: The buffers into which bytes are to be transferred |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset within the buffer array of the first buffer into which bytes are to be transferred; must be non-negative and no larger than `dsts.length` |
| --- | --- |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The maximum number of buffers to be accessed; must be non-negative and no larger than `dsts.length - offset` |
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The maximum time for the I/O operation to complete |
| `unit` | [TimeUnit](../java/util/concurrent/TimeUnit.md)!: The time unit of the `timeout` argument |
| --- | --- |
| `attachment` | A: The object to attach to the I/O operation; can be `null` |
| `handler` | [CompletionHandler](../java/nio/channels/CompletionHandler.md)\< [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!, in A\>!: The handler for consuming the result |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the buffer is read-only |
| `java.lang.IndexOutOfBoundsException` | If the pre-conditions for the `offset` and `length` parameter aren't met |
| `java.nio.channels.NotYetConnectedException` | If this channel is not yet connected |
| --- | --- |
| `java.nio.channels.ReadPendingException` | If a read operation is already in progress on this channel |
| `java.nio.channels.ShutdownChannelGroupException` | If the channel group has terminated |

### setOption

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun <T : Any!> setOption(
    name: SocketOption<T>!, 
    value: T
): AsynchronousSocketChannel!
```

| Parameters ||
|---|---|
| `<T>` | The type of the socket option value |
| `name` | [SocketOption](../java/net/SocketOption.md)\<T\>!: The socket option |
| `value` | T: The value of the socket option. A value of `null` may be a valid value for some socket options. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel#!` | This channel |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |
| `java.lang.IllegalArgumentException` | If the value is not a valid value for this socket option |
| `java.lang.UnsupportedOperationException` | If the socket option is not supported by this channel |
| --- | --- |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |

### shutdownInput

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun shutdownInput(): AsynchronousSocketChannel!
```

Shutdown the connection for reading without closing the channel.

Once shutdown for reading then further reads on the channel will return `-1`, the end-of-stream indication. If the input side of the connection is already shutdown then invoking this method has no effect. The effect on an outstanding read operation is system dependent and therefore not specified. The effect, if any, when there is data in the socket receive buffer that has not been read, or data arrives subsequently, is also system dependent.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel#!` | The channel |

| Exceptions ||
|---|---|
| `java.io.IOException` | If some other I/O error occurs |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.NotYetConnectedException` | If this channel is not yet connected |
| --- | --- |

### shutdownOutput

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun shutdownOutput(): AsynchronousSocketChannel!
```

Shutdown the connection for writing without closing the channel.

Once shutdown for writing then further attempts to write to the channel will throw `https://developer.android.com/reference/kotlin/java/nio/channels/ClosedChannelException`. If the output side of the connection is already shutdown then invoking this method has no effect. The effect on an outstanding write operation is system dependent and therefore not specified.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel#!` | The channel |

| Exceptions ||
|---|---|
| `java.io.IOException` | If some other I/O error occurs |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.NotYetConnectedException` | If this channel is not yet connected |
| --- | --- |

### write

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun write(src: ByteBuffer!): Future<Int!>!
```

| Parameters ||
|---|---|
| `src` | [ByteBuffer](../java/nio/ByteBuffer.md)!: The buffer from which bytes are to be retrieved |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/Future.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>!` | A Future representing the result of the operation |

| Exceptions ||
|---|---|
| `java.nio.channels.WritePendingException` | If the channel does not allow more than one write to be outstanding and a previous write has not completed |
| `java.nio.channels.NotYetConnectedException` | If this channel is not yet connected |

### write

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <A : Any!> write(
    src: ByteBuffer!, 
    attachment: A, 
    handler: CompletionHandler<Int!, in A>!
): Unit
```

| Parameters ||
|---|---|
| `<A>` | The type of the attachment |
| `src` | [ByteBuffer](../java/nio/ByteBuffer.md)!: The buffer from which bytes are to be retrieved |
| `attachment` | A: The object to attach to the I/O operation; can be `null` |
| --- | --- |
| `handler` | [CompletionHandler](../java/nio/channels/CompletionHandler.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!, in A\>!: The completion handler object |

| Exceptions ||
|---|---|
| `java.nio.channels.ShutdownChannelGroupException` | If the channel group has terminated |
| `java.nio.channels.WritePendingException` | If the channel does not allow more than one write to be outstanding and a previous write has not completed |
| `java.nio.channels.NotYetConnectedException` | If this channel is not yet connected |
| --- | --- |

### write

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun <A : Any!> write(
    src: ByteBuffer!, 
    timeout: Long, 
    unit: TimeUnit!, 
    attachment: A, 
    handler: CompletionHandler<Int!, in A>!
): Unit
```

Writes a sequence of bytes to this channel from the given buffer.

This method initiates an asynchronous write operation to write a sequence of bytes to this channel from the given buffer. The `handler` parameter is a completion handler that is invoked when the write operation completes (or fails). The result passed to the completion handler is the number of bytes written.

If a timeout is specified and the timeout elapses before the operation completes then it completes with the exception `https://developer.android.com/reference/kotlin/java/nio/channels/InterruptedByTimeoutException`. Where a timeout occurs, and the implementation cannot guarantee that bytes have not been written, or will not be written to the channel from the given buffer, then further attempts to write to the channel will cause an unspecific runtime exception to be thrown.

Otherwise this method works in the same manner as the `https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousByteChannel#write(java.nio.ByteBuffer,%20java.nio.channels.AsynchronousByteChannel.write.A,%20java.nio.channels.CompletionHandler)` method.

| Parameters ||
|---|---|
| `<A>` | The type of the attachment |
| `src` | [ByteBuffer](../java/nio/ByteBuffer.md)!: The buffer from which bytes are to be retrieved |
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The maximum time for the I/O operation to complete |
| --- | --- |
| `unit` | [TimeUnit](../java/util/concurrent/TimeUnit.md)!: The time unit of the `timeout` argument |
| `attachment` | A: The object to attach to the I/O operation; can be `null` |
| `handler` | [CompletionHandler](../java/nio/channels/CompletionHandler.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!, in A\>!: The handler for consuming the result |
| --- | --- |

| Exceptions ||
|---|---|
| `java.nio.channels.NotYetConnectedException` | If this channel is not yet connected |
| `java.nio.channels.ShutdownChannelGroupException` | If the channel group has terminated |
| `java.nio.channels.WritePendingException` | If a write operation is already in progress on this channel |
| --- | --- |

### write

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun <A : Any!> write(
    srcs: Array<ByteBuffer!>!, 
    offset: Int, 
    length: Int, 
    timeout: Long, 
    unit: TimeUnit!, 
    attachment: A, 
    handler: CompletionHandler<Long!, in A>!
): Unit
```

Writes a sequence of bytes to this channel from a subsequence of the given buffers. This operation, sometimes called a *gathering write* , is often useful when implementing network protocols that group data into segments consisting of one or more fixed-length headers followed by a variable-length body. The `handler` parameter is a completion handler that is invoked when the write operation completes (or fails). The result passed to the completion handler is the number of bytes written.

This method initiates a write of up to *r* bytes to this channel, where *r* is the total number of bytes remaining in the specified subsequence of the given buffer array, that is,

```kotlin
srcs[offset].remaining()
      + srcs[offset+1].remaining()
      + ... + srcs[offset+length-1].remaining()
```
at the moment that the write is attempted.

Suppose that a byte sequence of length *n* is written, where `0` `<` *n* `<=` *r* . Up to the first `srcs[offset].remaining()` bytes of this sequence are written from buffer `srcs[offset]`, up to the next `srcs[offset+1].remaining()` bytes are written from buffer `srcs[offset+1]`, and so forth, until the entire byte sequence is written. As many bytes as possible are written from each buffer, hence the final position of each updated buffer, except the last updated buffer, is guaranteed to be equal to that buffer's limit. The underlying operating system may impose a limit on the number of buffers that may be used in an I/O operation. Where the number of buffers (with bytes remaining), exceeds this limit, then the I/O operation is performed with the maximum number of buffers allowed by the operating system.

If a timeout is specified and the timeout elapses before the operation completes then it completes with the exception `https://developer.android.com/reference/kotlin/java/nio/channels/InterruptedByTimeoutException`. Where a timeout occurs, and the implementation cannot guarantee that bytes have not been written, or will not be written to the channel from the given buffers, then further attempts to write to the channel will cause an unspecific runtime exception to be thrown.

| Parameters ||
|---|---|
| `<A>` | The type of the attachment |
| `srcs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ByteBuffer](../java/nio/ByteBuffer.md)!\>!: The buffers from which bytes are to be retrieved |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset within the buffer array of the first buffer from which bytes are to be retrieved; must be non-negative and no larger than `srcs.length` |
| --- | --- |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The maximum number of buffers to be accessed; must be non-negative and no larger than `srcs.length - offset` |
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The maximum time for the I/O operation to complete |
| `unit` | [TimeUnit](../java/util/concurrent/TimeUnit.md)!: The time unit of the `timeout` argument |
| --- | --- |
| `attachment` | A: The object to attach to the I/O operation; can be `null` |
| `handler` | [CompletionHandler](../java/nio/channels/CompletionHandler.md)\< [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!, in A\>!: The handler for consuming the result |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | If the pre-conditions for the `offset` and `length` parameter aren't met |
| `java.nio.channels.NotYetConnectedException` | If this channel is not yet connected |
| `java.nio.channels.ShutdownChannelGroupException` | If the channel group has terminated |
| --- | --- |
| `java.nio.channels.WritePendingException` | If a write operation is already in progress on this channel |
