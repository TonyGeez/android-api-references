# SocketChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SocketChannel

```
abstract class SocketChannel : AbstractSelectableChannel, ByteChannel, GatheringByteChannel, NetworkChannel, ScatteringByteChannel
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [java.nio.channels.spi.AbstractInterruptibleChannel](../java/nio/channels/spi/AbstractInterruptibleChannel.md) ||||
| | ↳ | [java.nio.channels.SelectableChannel](../java/nio/channels/SelectableChannel.md) |||
| | | ↳ | [java.nio.channels.spi.AbstractSelectableChannel](../java/nio/channels/spi/AbstractSelectableChannel.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.nio.channels.SocketChannel](../java/nio/channels/SocketChannel.md) |

A selectable channel for stream-oriented connecting sockets.

A socket channel is created by invoking one of the #open methods of this class. It is not possible to create a channel for an arbitrary, pre-existing socket. A newly-created socket channel is open but not yet connected. An attempt to invoke an I/O operation upon an unconnected channel will cause a [NotYetConnectedException](../java/nio/channels/NotYetConnectedException.md) to be thrown. A socket channel can be connected by invoking its [connect](../java/nio/channels/SocketChannel.md))method; once connected, a socket channel remains connected until it is closed. Whether or not a socket channel is connected may be determined by invoking its [isConnected](../java/nio/channels/SocketChannel.md))method.

Socket channels support*non-blocking connection:* A socket channel may be created and the process of establishing the link to the remote socket may be initiated via the [connect](../java/nio/channels/SocketChannel.md))method for later completion by the [finishConnect](../java/nio/channels/SocketChannel.md))method. Whether or not a connection operation is in progress may be determined by invoking the [isConnectionPending](../java/nio/channels/SocketChannel.md))method.

Socket channels support*asynchronous shutdown,* which is similar to the asynchronous close operation specified in the [Channel](../java/nio/channels/Channel.md) class. If the input side of a socket is shut down by one thread while another thread is blocked in a read operation on the socket's channel, then the read operation in the blocked thread will complete without reading any bytes and will return`-1`. If the output side of a socket is shut down by one thread while another thread is blocked in a write operation on the socket's channel, then the blocked thread will receive an [AsynchronousCloseException](../java/nio/channels/AsynchronousCloseException.md).

Socket options are configured using the [setOption](../java/nio/channels/SocketChannel.md))method. Socket channels support the following options:

| Option Name | Description |
| --- | --- |
| [SO_SNDBUF](../java/net/StandardSocketOptions.md) | The size of the socket send buffer |
| [SO_RCVBUF](../java/net/StandardSocketOptions.md) | The size of the socket receive buffer |
| [SO_KEEPALIVE](../java/net/StandardSocketOptions.md) | Keep connection alive |
| --- | --- |
| [SO_REUSEADDR](../java/net/StandardSocketOptions.md) | Re-use address |
| [SO_LINGER](../java/net/StandardSocketOptions.md) | Linger on close if data is present (when configured in blocking mode only) |
| [TCP_NODELAY](../java/net/StandardSocketOptions.md) | Disable the Nagle algorithm |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|

Additional (implementation specific) options may also be supported.

Socket channels are safe for use by multiple concurrent threads. They support concurrent reading and writing, though at most one thread may be reading and at most one thread may be writing at any given time. The [connect](../java/nio/channels/SocketChannel.md))and [finishConnect](../java/nio/channels/SocketChannel.md))methods are mutually synchronized against each other, and an attempt to initiate a read or write operation while an invocation of one of these methods is in progress will block until that invocation is complete.

## Summary

| Protected constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SocketChannel](../java/nio/channels/SocketChannel.md))`(`provider:` ` [SelectorProvider](../java/nio/channels/spi/SelectorProvider.md)!`)` Initializes a new instance of this class. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [SocketChannel](../java/nio/channels/SocketChannel.md)! | [bind](../java/nio/channels/SocketChannel.md))`(`local:` ` [SocketAddress](../java/net/SocketAddress.md)!`)` <br /> |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [connect](../java/nio/channels/SocketChannel.md))`(`remote:` ` [SocketAddress](../java/net/SocketAddress.md)!`)` Connects this channel's socket. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [finishConnect](../java/nio/channels/SocketChannel.md))`()` Finishes the process of connecting a socket channel. |
| --- | --- |
| abstract [SocketAddress](../java/net/SocketAddress.md)! | [getLocalAddress](../java/nio/channels/SocketChannel.md))`()` Returns the socket address that this channel's socket is bound to. |
| abstract [SocketAddress](../java/net/SocketAddress.md)! | [getRemoteAddress](../java/nio/channels/SocketChannel.md))`()` Returns the remote address to which this channel's socket is connected. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnected](../java/nio/channels/SocketChannel.md))`()` Tells whether or not this channel's network socket is connected. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnectionPending](../java/nio/channels/SocketChannel.md))`()` Tells whether or not a connection operation is in progress on this channel. |
| openstatic [SocketChannel](../java/nio/channels/SocketChannel.md)! | [open](../java/nio/channels/SocketChannel.md))`()` Opens a socket channel. |
| openstatic [SocketChannel](../java/nio/channels/SocketChannel.md)! | [open](../java/nio/channels/SocketChannel.md))`(`remote:` ` [SocketAddress](../java/net/SocketAddress.md)!`)` Opens a socket channel and connects it to a remote address. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](../java/nio/channels/SocketChannel.md))`(`dst:` ` [ByteBuffer](../java/nio/ByteBuffer.md)!`)` <br /> |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [read](../java/nio/channels/SocketChannel.md))`(`dsts:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ByteBuffer](../java/nio/ByteBuffer.md)!>!`)` <br /> |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [read](../java/nio/channels/SocketChannel.md))`(`dsts:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ByteBuffer](../java/nio/ByteBuffer.md)!>!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| abstract [SocketChannel](../java/nio/channels/SocketChannel.md)! | [setOption](../java/nio/channels/SocketChannel.md))`(`name:` ` [SocketOption](../java/net/SocketOption.md)<T>!`, `value:` `T`)` <br /> |
| abstract [SocketChannel](../java/nio/channels/SocketChannel.md)! | [shutdownInput](../java/nio/channels/SocketChannel.md))`()` Shutdown the connection for reading without closing the channel. |
| abstract [SocketChannel](../java/nio/channels/SocketChannel.md)! | [shutdownOutput](../java/nio/channels/SocketChannel.md))`()` Shutdown the connection for writing without closing the channel. |
| --- | --- |
| abstract [Socket](../java/net/Socket.md)! | [socket](../java/nio/channels/SocketChannel.md))`()` Retrieves a socket associated with this channel. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [validOps](../java/nio/channels/SocketChannel.md))`()` Returns an operation set identifying this channel's supported operations. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [write](../java/nio/channels/SocketChannel.md))`(`src:` ` [ByteBuffer](../java/nio/ByteBuffer.md)!`)` <br /> |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [write](../java/nio/channels/SocketChannel.md))`(`srcs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ByteBuffer](../java/nio/ByteBuffer.md)!>!`)` <br /> |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [write](../java/nio/channels/SocketChannel.md))`(`srcs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ByteBuffer](../java/nio/ByteBuffer.md)!>!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Inherited functions ||
|---|---|
| From class [AbstractInterruptibleChannel](../java/nio/channels/spi/AbstractInterruptibleChannel.md) |------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [begin](../java/nio/channels/spi/AbstractInterruptibleChannel.md))`()` <br /> Marks the beginning of an I/O operation that might block indefinitely. This method should be invoked in tandem with the [end](../java/nio/channels/spi/AbstractInterruptibleChannel.md))method, using a`try`...`finally`block as shown [above](../java/nio/channels/spi/AbstractInterruptibleChannel.md), in order to implement asynchronous closing and interruption for this channel. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../java/nio/channels/spi/AbstractInterruptibleChannel.md))`()` <br /> Closes this channel. If the channel has already been closed then this method returns immediately. Otherwise it marks the channel as closed and then invokes the [implCloseChannel](../java/nio/channels/spi/AbstractInterruptibleChannel.md))method in order to complete the close operation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [end](../java/nio/channels/spi/AbstractInterruptibleChannel.md))`(`completed:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Marks the end of an I/O operation that might block indefinitely. This method should be invoked in tandem with the [begin](../java/nio/channels/spi/AbstractInterruptibleChannel.md))method, using a`try`...`finally`block as shown [above](../java/nio/channels/spi/AbstractInterruptibleChannel.md), in order to implement asynchronous closing and interruption for this channel. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [implCloseChannel](../java/nio/channels/spi/AbstractInterruptibleChannel.md))`()` <br /> Closes this channel. This method is invoked by the #close method in order to perform the actual work of closing the channel. This method is only invoked if the channel has not yet been closed, and it is never invoked more than once. An implementation of this method must arrange for any other thread that is blocked in an I/O operation upon this channel to return immediately, either by throwing an exception or by returning normally. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpen](../java/nio/channels/spi/AbstractInterruptibleChannel.md))`()` <br /> | ||
| From class [AbstractSelectableChannel](../java/nio/channels/spi/AbstractSelectableChannel.md) |------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [blockingLock](../java/nio/channels/spi/AbstractSelectableChannel.md))`()` <br /> | | [SelectableChannel](../java/nio/channels/SelectableChannel.md)! | [configureBlocking](../java/nio/channels/spi/AbstractSelectableChannel.md))`(`block:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Adjusts this channel's blocking mode. If the given blocking mode is different from the current blocking mode then this method invokes the [implConfigureBlocking](../java/nio/channels/spi/AbstractSelectableChannel.md))method, while holding the appropriate locks, in order to change the mode. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [implCloseChannel](../java/nio/channels/spi/AbstractSelectableChannel.md))`()` <br /> Closes this channel. This method, which is specified in the [AbstractInterruptibleChannel](../java/nio/channels/spi/AbstractInterruptibleChannel.md) class and is invoked by the java.nio.channels.Channel#close method, in turn invokes the [implCloseSelectableChannel](../java/nio/channels/spi/AbstractSelectableChannel.md))method in order to perform the actual work of closing this channel. It then cancels all of this channel's keys. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [implCloseSelectableChannel](../java/nio/channels/spi/AbstractSelectableChannel.md))`()` <br /> Closes this selectable channel. This method is invoked by the java.nio.channels.Channel#close method in order to perform the actual work of closing the channel. This method is only invoked if the channel has not yet been closed, and it is never invoked more than once. An implementation of this method must arrange for any other thread that is blocked in an I/O operation upon this channel to return immediately, either by throwing an exception or by returning normally. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [implConfigureBlocking](../java/nio/channels/spi/AbstractSelectableChannel.md))`(`block:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Adjusts this channel's blocking mode. This method is invoked by the [configureBlocking](../java/nio/channels/spi/AbstractSelectableChannel.md))method in order to perform the actual work of changing the blocking mode. This method is only invoked if the new mode is different from the current mode. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBlocking](../java/nio/channels/spi/AbstractSelectableChannel.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRegistered](../java/nio/channels/spi/AbstractSelectableChannel.md))`()` <br /> | | [SelectionKey](../java/nio/channels/SelectionKey.md)! | [keyFor](../java/nio/channels/spi/AbstractSelectableChannel.md))`(`sel:` ` [Selector](../java/nio/channels/Selector.md)!`)` <br /> | | [SelectorProvider](../java/nio/channels/spi/SelectorProvider.md)! | [provider](../java/nio/channels/spi/AbstractSelectableChannel.md))`()` <br /> Returns the provider that created this channel. <br /> | | [SelectionKey](../java/nio/channels/SelectionKey.md)! | [register](../java/nio/channels/spi/AbstractSelectableChannel.md))`(`sel:` ` [Selector](../java/nio/channels/Selector.md)!`, `ops:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `att:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Registers this channel with the given selector, returning a selection key. This method first verifies that this channel is open and that the given initial interest set is valid. If this channel is already registered with the given selector then the selection key representing that registration is returned after setting its interest set to the given value. Otherwise this channel has not yet been registered with the given selector, so the [register](../java/nio/channels/spi/AbstractSelector.md))method of the selector is invoked while holding the appropriate locks. The resulting key is added to this channel's key set before being returned. <br /> | ||
| From class [Channel](../java/nio/channels/Channel.md) |------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../java/nio/channels/Channel.md))`()` <br /> Closes this channel. After a channel is closed, any further attempt to invoke I/O operations upon it will cause a [ClosedChannelException](../java/nio/channels/ClosedChannelException.md) to be thrown. If this channel is already closed then invoking this method has no effect. This method may be invoked at any time. If some other thread has already invoked it, however, then another invocation will block until the first invocation is complete, after which it will return without effect. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpen](../java/nio/channels/Channel.md))`()` <br /> Tells whether or not this channel is open. <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| From class [NetworkChannel](../java/nio/channels/NetworkChannel.md) |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | T | [getOption](../java/nio/channels/NetworkChannel.md))`(`name:` ` [SocketOption](../java/net/SocketOption.md)<T>!`)` <br /> Returns the value of a socket option. <br /> | | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [SocketOption](../java/net/SocketOption.md)<*>!>! | [supportedOptions](../java/nio/channels/NetworkChannel.md))`()` <br /> Returns a set of the socket options supported by this channel. This method will continue to return the set of options even after the channel has been closed. <br /> | ||
| From class [SelectableChannel](../java/nio/channels/SelectableChannel.md) |------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [SelectionKey](../java/nio/channels/SelectionKey.md)! | [register](../java/nio/channels/SelectableChannel.md))`(`sel:` ` [Selector](../java/nio/channels/Selector.md)!`, `ops:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Registers this channel with the given selector, returning a selection key. An invocation of this convenience method of the form `sc.register(sel, ops)`behaves in exactly the same way as the invocation`sc.` [register(sel, ops, null)](../java/nio/channels/SelectableChannel.md)) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [validOps](../java/nio/channels/SelectableChannel.md))`()` <br /> Returns an [operation set](../java/nio/channels/SelectionKey.md) identifying this channel's supported operations. The bits that are set in this integer value denote exactly the operations that are valid for this channel. This method always returns the same value for a given concrete channel class. <br /> | ||

## Protected constructors

### SocketChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected SocketChannel(provider: SelectorProvider!)
```

Initializes a new instance of this class.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [SelectorProvider](../java/nio/channels/spi/SelectorProvider.md)!:The provider that created this channel |

## Public methods

### bind

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun bind(local: SocketAddress!): SocketChannel!
```

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `local` | [SocketAddress](../java/net/SocketAddress.md)!:The address to bind the socket, or`null`to bind the socket to an automatically assigned socket address |

| Return ||
|---------------------------------------------------------------------------------------------------|--------------|
| [SocketChannel](../java/nio/channels/SocketChannel.md)! | This channel |

| Exceptions ||
|-----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.AlreadyBoundException` | If the socket is already bound |
| `java.nio.channels.UnsupportedAddressTypeException` | If the type of the given address is not supported |
| `java.nio.channels.ClosedChannelException` | If the channel is closed |
| --- | --- |
| `java.io.IOException` | If some other I/O error occurs |
| `java.lang.SecurityException` | If a security manager has been installed and its [checkListen](../java/lang/SecurityManager.md))method denies the operation |
| `java.nio.channels.ConnectionPendingException` | If a non-blocking connect operation is already in progress on this channel |
| --- | --- |

### connect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun connect(remote: SocketAddress!): Boolean
```

Connects this channel's socket.

If this channel is in non-blocking mode then an invocation of this method initiates a non-blocking connection operation. If the connection is established immediately, as can happen with a local connection, then this method returns`true`. Otherwise this method returns`false`and the connection operation must later be completed by invoking the [finishConnect](../java/nio/channels/SocketChannel.md))method.

If this channel is in blocking mode then an invocation of this method will block until the connection is established or an I/O error occurs.

This method performs exactly the same security checks as the class. That is, if a security manager has been installed then this method verifies that its java.lang.SecurityManager#checkConnect method permits connecting to the address and port number of the given remote endpoint.

This method may be invoked at any time. If a read or write operation upon this channel is invoked while an invocation of this method is in progress then that operation will first block until this invocation is complete. If a connection attempt is initiated but fails, that is, if an invocation of this method throws a checked exception, then the channel will be closed.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `remote` | [SocketAddress](../java/net/SocketAddress.md)!:The remote address to which this channel is to be connected |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if a connection was established,`false`if this channel is in non-blocking mode and the connection operation is in progress |

| Exceptions ||
|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.AlreadyConnectedException` | If this channel is already connected |
| `java.nio.channels.ConnectionPendingException` | If a non-blocking connection operation is already in progress on this channel |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| --- | --- |
| `java.nio.channels.AsynchronousCloseException` | If another thread closes this channel while the connect operation is in progress |
| `java.nio.channels.ClosedByInterruptException` | If another thread interrupts the current thread while the connect operation is in progress, thereby closing the channel and setting the current thread's interrupt status |
| `java.nio.channels.UnresolvedAddressException` | If the given remote address is not fully resolved |
| --- | --- |
| `java.nio.channels.UnsupportedAddressTypeException` | If the type of the given remote address is not supported |
| `java.lang.SecurityException` | If a security manager has been installed and it does not permit access to the given remote endpoint |
| `java.io.IOException` | If some other I/O error occurs |
| --- | --- |

### finishConnect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun finishConnect(): Boolean
```

Finishes the process of connecting a socket channel.

A non-blocking connection operation is initiated by placing a socket channel in non-blocking mode and then invoking its [connect](../java/nio/channels/SocketChannel.md))method. Once the connection is established, or the attempt has failed, the socket channel will become connectable and this method may be invoked to complete the connection sequence. If the connection operation failed then invoking this method will cause an appropriate [java.io.IOException](../java/io/IOException.md) to be thrown.

If this channel is already connected then this method will not block and will immediately return`true`. If this channel is in non-blocking mode then this method will return`false`if the connection process is not yet complete. If this channel is in blocking mode then this method will block until the connection either completes or fails, and will always either return`true`or throw a checked exception describing the failure.

This method may be invoked at any time. If a read or write operation upon this channel is invoked while an invocation of this method is in progress then that operation will first block until this invocation is complete. If a connection attempt fails, that is, if an invocation of this method throws a checked exception, then the channel will be closed.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, this channel's socket is now connected |

| Exceptions ||
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.NoConnectionPendingException` | If this channel is not connected and a connection operation has not been initiated |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.AsynchronousCloseException` | If another thread closes this channel while the connect operation is in progress |
| --- | --- |
| `java.nio.channels.ClosedByInterruptException` | If another thread interrupts the current thread while the connect operation is in progress, thereby closing the channel and setting the current thread's interrupt status |
| `java.io.IOException` | If some other I/O error occurs |

### getLocalAddress

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLocalAddress(): SocketAddress!
```

Returns the socket address that this channel's socket is bound to.

Where the channel is [bound](../java/nio/channels/NetworkChannel.md))to an Internet Protocol socket address then the return value from this method is of type .

If there is a security manager set, its`checkConnect`method is called with the local address and`-1`as its arguments to see if the operation is allowed. If the operation is not allowed, a`SocketAddress`representing the [loopback](../java/net/InetAddress.md))address and the local port of the channel's socket is returned.

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SocketAddress](../java/net/SocketAddress.md)! | The`SocketAddress`that the socket is bound to, or the`SocketAddress`representing the loopback address if denied by the security manager, or`null`if the channel's socket is not bound |

| Exceptions ||
|--------------------------------------------|--------------------------|
| `java.nio.channels.ClosedChannelException` | If the channel is closed |
| `java.io.IOException` | If an I/O error occurs |

### getRemoteAddress

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getRemoteAddress(): SocketAddress!
```

Returns the remote address to which this channel's socket is connected.

Where the channel is bound and connected to an Internet Protocol socket address then the return value from this method is of type .

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [SocketAddress](../java/net/SocketAddress.md)! | The remote address;`null`if the channel's socket is not connected |

| Exceptions ||
|--------------------------------------------|--------------------------|
| `java.nio.channels.ClosedChannelException` | If the channel is closed |
| `java.io.IOException` | If an I/O error occurs |

### isConnected

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isConnected(): Boolean
```

Tells whether or not this channel's network socket is connected.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, this channel's network socket is [open](../java/nio/channels/spi/AbstractInterruptibleChannel.md))and connected |

### isConnectionPending

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isConnectionPending(): Boolean
```

Tells whether or not a connection operation is in progress on this channel.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, a connection operation has been initiated on this channel but not yet completed by invoking the [finishConnect](../java/nio/channels/SocketChannel.md))method |

### open

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun open(): SocketChannel!
```

Opens a socket channel.

The new channel is created by invoking the [openSocketChannel](../java/nio/channels/spi/SelectorProvider.md))method of the system-wide default object.

| Return ||
|---------------------------------------------------------------------------------------------------|----------------------|
| [SocketChannel](../java/nio/channels/SocketChannel.md)! | A new socket channel |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |

### open

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun open(remote: SocketAddress!): SocketChannel!
```

Opens a socket channel and connects it to a remote address.

This convenience method works as if by invoking the [open()](../java/nio/channels/SocketChannel.md))method, invoking the [connect](../java/nio/channels/SocketChannel.md))method upon the resulting socket channel, passing it`remote`, and then returning that channel.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `remote` | [SocketAddress](../java/net/SocketAddress.md)!:The remote address to which the new channel is to be connected |

| Return ||
|---------------------------------------------------------------------------------------------------|--------------------------------------|
| [SocketChannel](../java/nio/channels/SocketChannel.md)! | A new, and connected, socket channel |

| Exceptions ||
|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.AsynchronousCloseException` | If another thread closes this channel while the connect operation is in progress |
| `java.nio.channels.ClosedByInterruptException` | If another thread interrupts the current thread while the connect operation is in progress, thereby closing the channel and setting the current thread's interrupt status |
| `java.nio.channels.UnresolvedAddressException` | If the given remote address is not fully resolved |
| --- | --- |
| `java.nio.channels.UnsupportedAddressTypeException` | If the type of the given remote address is not supported |
| `java.lang.SecurityException` | If a security manager has been installed and it does not permit access to the given remote endpoint |
| `java.io.IOException` | If some other I/O error occurs |
| --- | --- |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun read(dst: ByteBuffer!): Int
```

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `dst` | [ByteBuffer](../java/nio/ByteBuffer.md)!:The buffer into which bytes are to be transferred |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of bytes read, possibly zero, or`-1`if the channel has reached end-of-stream |

| Exceptions ||
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.NonReadableChannelException` | If this channel was not opened for reading |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.AsynchronousCloseException` | If another thread closes this channel while the read operation is in progress |
| --- | --- |
| `java.nio.channels.ClosedByInterruptException` | If another thread interrupts the current thread while the read operation is in progress, thereby closing the channel and setting the current thread's interrupt status |
| `java.io.IOException` | If some other I/O error occurs |
| `java.nio.channels.NotYetConnectedException` | If this channel is not yet connected |
| --- | --- |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun read(dsts: Array<ByteBuffer!>!): Long
```

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dsts` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ByteBuffer](../java/nio/ByteBuffer.md)!\>!:The buffers into which bytes are to be transferred |

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The number of bytes read, possibly zero, or`-1`if the channel has reached end-of-stream |

| Exceptions ||
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.NonReadableChannelException` | If this channel was not opened for reading |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.AsynchronousCloseException` | If another thread closes this channel while the read operation is in progress |
| --- | --- |
| `java.nio.channels.ClosedByInterruptException` | If another thread interrupts the current thread while the read operation is in progress, thereby closing the channel and setting the current thread's interrupt status |
| `java.io.IOException` | If some other I/O error occurs |
| `java.nio.channels.NotYetConnectedException` | If this channel is not yet connected |
| --- | --- |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun read(
    dsts: Array<ByteBuffer!>!, 
    offset: Int, 
    length: Int
): Long
```

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dsts` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ByteBuffer](../java/nio/ByteBuffer.md)!\>!:The buffers into which bytes are to be transferred |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The offset within the buffer array of the first buffer into which bytes are to be transferred; must be non-negative and no larger than`dsts.length` |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The maximum number of buffers to be accessed; must be non-negative and no larger than`dsts.length`-`offset` |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The number of bytes read, possibly zero, or`-1`if the channel has reached end-of-stream |

| Exceptions ||
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If the preconditions on the`offset`and`length`parameters do not hold |
| `java.nio.channels.NonReadableChannelException` | If this channel was not opened for reading |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| --- | --- |
| `java.nio.channels.AsynchronousCloseException` | If another thread closes this channel while the read operation is in progress |
| `java.nio.channels.ClosedByInterruptException` | If another thread interrupts the current thread while the read operation is in progress, thereby closing the channel and setting the current thread's interrupt status |
| `java.io.IOException` | If some other I/O error occurs |
| --- | --- |
| `java.nio.channels.NotYetConnectedException` | If this channel is not yet connected |

### setOption

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <T : Any!> setOption(
    name: SocketOption<T>!, 
    value: T
): SocketChannel!
```

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------|
| `<T>` | The type of the socket option value |
| `name` | [SocketOption](../java/net/SocketOption.md)\<T\>!:The socket option |
| `value` | T:The value of the socket option. A value of`null`may be a valid value for some socket options. |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------------------------|--------------|
| [SocketChannel](../java/nio/channels/SocketChannel.md)! | This channel |

| Exceptions ||
|--------------------------------------------|----------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | If the socket option is not supported by this channel |
| `java.lang.IllegalArgumentException` | If the value is not a valid value for this socket option |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| --- | --- |
| `java.io.IOException` | If an I/O error occurs |

### shutdownInput

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun shutdownInput(): SocketChannel!
```

Shutdown the connection for reading without closing the channel.

Once shutdown for reading then further reads on the channel will return`-1`, the end-of-stream indication. If the input side of the connection is already shutdown then invoking this method has no effect.

| Return ||
|---------------------------------------------------------------------------------------------------|-------------|
| [SocketChannel](../java/nio/channels/SocketChannel.md)! | The channel |

| Exceptions ||
|----------------------------------------------|--------------------------------------|
| `java.nio.channels.NotYetConnectedException` | If this channel is not yet connected |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.io.IOException` | If some other I/O error occurs |
| --- | --- |

### shutdownOutput

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun shutdownOutput(): SocketChannel!
```

Shutdown the connection for writing without closing the channel.

Once shutdown for writing then further attempts to write to the channel will throw [ClosedChannelException](../java/nio/channels/ClosedChannelException.md). If the output side of the connection is already shutdown then invoking this method has no effect.

| Return ||
|---------------------------------------------------------------------------------------------------|-------------|
| [SocketChannel](../java/nio/channels/SocketChannel.md)! | The channel |

| Exceptions ||
|----------------------------------------------|--------------------------------------|
| `java.nio.channels.NotYetConnectedException` | If this channel is not yet connected |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.io.IOException` | If some other I/O error occurs |
| --- | --- |

### socket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun socket(): Socket!
```

Retrieves a socket associated with this channel.

The returned object will not declare any public methods that are not declared in the [java.net.Socket](../java/net/Socket.md) class.

| Return ||
|---------------------------------------------------------------------------------|---------------------------------------|
| [Socket](../java/net/Socket.md)! | A socket associated with this channel |

### validOps

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun validOps(): Int
```

Returns an operation set identifying this channel's supported operations.

Socket channels support connecting, reading, and writing, so this method returns`(` [SelectionKey.OP_CONNECT](../java/nio/channels/SelectionKey.md)`|` [SelectionKey.OP_READ](../java/nio/channels/SelectionKey.md)`|` [java.nio.channels.SelectionKey#OP_WRITE](../java/nio/channels/SelectionKey.md)`)`.
| --- | --- | --- |

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The valid-operation set |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun write(src: ByteBuffer!): Int
```

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `src` | [ByteBuffer](../java/nio/ByteBuffer.md)!:The buffer from which bytes are to be retrieved |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of bytes written, possibly zero |

| Exceptions ||
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.NonWritableChannelException` | If this channel was not opened for writing |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.AsynchronousCloseException` | If another thread closes this channel while the write operation is in progress |
| --- | --- |
| `java.nio.channels.ClosedByInterruptException` | If another thread interrupts the current thread while the write operation is in progress, thereby closing the channel and setting the current thread's interrupt status |
| `java.io.IOException` | If some other I/O error occurs |
| `java.nio.channels.NotYetConnectedException` | If this channel is not yet connected |
| --- | --- |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun write(srcs: Array<ByteBuffer!>!): Long
```

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `srcs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ByteBuffer](../java/nio/ByteBuffer.md)!\>!:The buffers from which bytes are to be retrieved |

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The number of bytes written, possibly zero |

| Exceptions ||
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.NonWritableChannelException` | If this channel was not opened for writing |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.AsynchronousCloseException` | If another thread closes this channel while the write operation is in progress |
| --- | --- |
| `java.nio.channels.ClosedByInterruptException` | If another thread interrupts the current thread while the write operation is in progress, thereby closing the channel and setting the current thread's interrupt status |
| `java.io.IOException` | If some other I/O error occurs |
| `java.nio.channels.NotYetConnectedException` | If this channel is not yet connected |
| --- | --- |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun write(
    srcs: Array<ByteBuffer!>!, 
    offset: Int, 
    length: Int
): Long
```

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `srcs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ByteBuffer](../java/nio/ByteBuffer.md)!\>!:The buffers from which bytes are to be retrieved |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The offset within the buffer array of the first buffer from which bytes are to be retrieved; must be non-negative and no larger than`srcs.length` |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The maximum number of buffers to be accessed; must be non-negative and no larger than`srcs.length`-`offset` |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The number of bytes written, possibly zero |

| Exceptions ||
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If the preconditions on the`offset`and`length`parameters do not hold |
| `java.nio.channels.NonWritableChannelException` | If this channel was not opened for writing |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| --- | --- |
| `java.nio.channels.AsynchronousCloseException` | If another thread closes this channel while the write operation is in progress |
| `java.nio.channels.ClosedByInterruptException` | If another thread interrupts the current thread while the write operation is in progress, thereby closing the channel and setting the current thread's interrupt status |
| `java.io.IOException` | If some other I/O error occurs |
| --- | --- |
| `java.nio.channels.NotYetConnectedException` | If this channel is not yet connected |
