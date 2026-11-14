# ServerSocketChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ServerSocketChannel

```
abstract class ServerSocketChannel : AbstractSelectableChannel, NetworkChannel
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [java.nio.channels.spi.AbstractInterruptibleChannel](../java.nio.channels.spi/AbstractInterruptibleChannel.md) ||||
| | ↳ | [java.nio.channels.SelectableChannel](SelectableChannel.md) |||
| | | ↳ | [java.nio.channels.spi.AbstractSelectableChannel](../java.nio.channels.spi/AbstractSelectableChannel.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.nio.channels.ServerSocketChannel](ServerSocketChannel.md) |

A selectable channel for stream-oriented listening sockets.

A server-socket channel is created by invoking the [open](ServerSocketChannel.md))method of this class. It is not possible to create a channel for an arbitrary, pre-existing [ServerSocket](../java.net/ServerSocket.md). A newly-created server-socket channel is open but not yet bound. An attempt to invoke the [accept](ServerSocketChannel.md))method of an unbound server-socket channel will cause a [NotYetBoundException](NotYetBoundException.md) to be thrown. A server-socket channel can be bound by invoking one of the [bind](ServerSocketChannel.md))methods defined by this class.

Socket options are configured using the [setOption](ServerSocketChannel.md))method. Server-socket channels support the following options:

| Option Name | Description |
| --- | --- |
| [SO_RCVBUF](../java.net/StandardSocketOptions.md) | The size of the socket receive buffer |
| [SO_REUSEADDR](../java.net/StandardSocketOptions.md) | Re-use address |
|---------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|

Additional (implementation specific) options may also be supported.

Server-socket channels are safe for use by multiple concurrent threads.

## Summary

| Protected constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ServerSocketChannel](ServerSocketChannel.md))`(`provider:` ` [SelectorProvider](../java.nio.channels.spi/SelectorProvider.md)!`)` Initializes a new instance of this class. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [SocketChannel](SocketChannel.md)! | [accept](ServerSocketChannel.md))`()` Accepts a connection made to this channel's socket. |
| [ServerSocketChannel](ServerSocketChannel.md)! | [bind](ServerSocketChannel.md))`(`local:` ` [SocketAddress](../java.net/SocketAddress.md)!`)` Binds the channel's socket to a local address and configures the socket to listen for connections. |
| abstract [ServerSocketChannel](ServerSocketChannel.md)! | [bind](ServerSocketChannel.md))`(`local:` ` [SocketAddress](../java.net/SocketAddress.md)!`, `backlog:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Binds the channel's socket to a local address and configures the socket to listen for connections. |
| --- | --- |
| abstract [SocketAddress](../java.net/SocketAddress.md)! | [getLocalAddress](ServerSocketChannel.md))`()` Returns the socket address that this channel's socket is bound to. |
| openstatic [ServerSocketChannel](ServerSocketChannel.md)! | [open](ServerSocketChannel.md))`()` Opens a server-socket channel. |
| abstract [ServerSocketChannel](ServerSocketChannel.md)! | [setOption](ServerSocketChannel.md))`(`name:` ` [SocketOption](../java.net/SocketOption.md)<T>!`, `value:` `T`)` <br /> |
| --- | --- |
| abstract [ServerSocket](../java.net/ServerSocket.md)! | [socket](ServerSocketChannel.md))`()` Retrieves a server socket associated with this channel. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [validOps](ServerSocketChannel.md))`()` Returns an operation set identifying this channel's supported operations. |

| Inherited functions ||
|---|---|
| From class [AbstractInterruptibleChannel](../java.nio.channels.spi/AbstractInterruptibleChannel.md) |------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [begin](../java.nio.channels.spi/AbstractInterruptibleChannel.md))`()` <br /> Marks the beginning of an I/O operation that might block indefinitely. This method should be invoked in tandem with the [end](../java.nio.channels.spi/AbstractInterruptibleChannel.md))method, using a`try`...`finally`block as shown [above](../java.nio.channels.spi/AbstractInterruptibleChannel.md), in order to implement asynchronous closing and interruption for this channel. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../java.nio.channels.spi/AbstractInterruptibleChannel.md))`()` <br /> Closes this channel. If the channel has already been closed then this method returns immediately. Otherwise it marks the channel as closed and then invokes the [implCloseChannel](../java.nio.channels.spi/AbstractInterruptibleChannel.md))method in order to complete the close operation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [end](../java.nio.channels.spi/AbstractInterruptibleChannel.md))`(`completed:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Marks the end of an I/O operation that might block indefinitely. This method should be invoked in tandem with the [begin](../java.nio.channels.spi/AbstractInterruptibleChannel.md))method, using a`try`...`finally`block as shown [above](../java.nio.channels.spi/AbstractInterruptibleChannel.md), in order to implement asynchronous closing and interruption for this channel. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [implCloseChannel](../java.nio.channels.spi/AbstractInterruptibleChannel.md))`()` <br /> Closes this channel. This method is invoked by the #close method in order to perform the actual work of closing the channel. This method is only invoked if the channel has not yet been closed, and it is never invoked more than once. An implementation of this method must arrange for any other thread that is blocked in an I/O operation upon this channel to return immediately, either by throwing an exception or by returning normally. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpen](../java.nio.channels.spi/AbstractInterruptibleChannel.md))`()` <br /> | ||
| From class [AbstractSelectableChannel](../java.nio.channels.spi/AbstractSelectableChannel.md) |------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [blockingLock](../java.nio.channels.spi/AbstractSelectableChannel.md))`()` <br /> | | [SelectableChannel](SelectableChannel.md)! | [configureBlocking](../java.nio.channels.spi/AbstractSelectableChannel.md))`(`block:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Adjusts this channel's blocking mode. If the given blocking mode is different from the current blocking mode then this method invokes the [implConfigureBlocking](../java.nio.channels.spi/AbstractSelectableChannel.md))method, while holding the appropriate locks, in order to change the mode. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [implCloseChannel](../java.nio.channels.spi/AbstractSelectableChannel.md))`()` <br /> Closes this channel. This method, which is specified in the [AbstractInterruptibleChannel](../java.nio.channels.spi/AbstractInterruptibleChannel.md) class and is invoked by the java.nio.channels.Channel#close method, in turn invokes the [implCloseSelectableChannel](../java.nio.channels.spi/AbstractSelectableChannel.md))method in order to perform the actual work of closing this channel. It then cancels all of this channel's keys. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [implCloseSelectableChannel](../java.nio.channels.spi/AbstractSelectableChannel.md))`()` <br /> Closes this selectable channel. This method is invoked by the java.nio.channels.Channel#close method in order to perform the actual work of closing the channel. This method is only invoked if the channel has not yet been closed, and it is never invoked more than once. An implementation of this method must arrange for any other thread that is blocked in an I/O operation upon this channel to return immediately, either by throwing an exception or by returning normally. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [implConfigureBlocking](../java.nio.channels.spi/AbstractSelectableChannel.md))`(`block:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Adjusts this channel's blocking mode. This method is invoked by the [configureBlocking](../java.nio.channels.spi/AbstractSelectableChannel.md))method in order to perform the actual work of changing the blocking mode. This method is only invoked if the new mode is different from the current mode. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBlocking](../java.nio.channels.spi/AbstractSelectableChannel.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRegistered](../java.nio.channels.spi/AbstractSelectableChannel.md))`()` <br /> | | [SelectionKey](SelectionKey.md)! | [keyFor](../java.nio.channels.spi/AbstractSelectableChannel.md))`(`sel:` ` [Selector](Selector.md)!`)` <br /> | | [SelectorProvider](../java.nio.channels.spi/SelectorProvider.md)! | [provider](../java.nio.channels.spi/AbstractSelectableChannel.md))`()` <br /> Returns the provider that created this channel. <br /> | | [SelectionKey](SelectionKey.md)! | [register](../java.nio.channels.spi/AbstractSelectableChannel.md))`(`sel:` ` [Selector](Selector.md)!`, `ops:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `att:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Registers this channel with the given selector, returning a selection key. This method first verifies that this channel is open and that the given initial interest set is valid. If this channel is already registered with the given selector then the selection key representing that registration is returned after setting its interest set to the given value. Otherwise this channel has not yet been registered with the given selector, so the [register](../java.nio.channels.spi/AbstractSelector.md))method of the selector is invoked while holding the appropriate locks. The resulting key is added to this channel's key set before being returned. <br /> | ||
| From class [Channel](Channel.md) |------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](Channel.md))`()` <br /> Closes this channel. After a channel is closed, any further attempt to invoke I/O operations upon it will cause a [ClosedChannelException](ClosedChannelException.md) to be thrown. If this channel is already closed then invoking this method has no effect. This method may be invoked at any time. If some other thread has already invoked it, however, then another invocation will block until the first invocation is complete, after which it will return without effect. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpen](Channel.md))`()` <br /> Tells whether or not this channel is open. <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| From class [NetworkChannel](NetworkChannel.md) |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | T | [getOption](NetworkChannel.md))`(`name:` ` [SocketOption](../java.net/SocketOption.md)<T>!`)` <br /> Returns the value of a socket option. <br /> | | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [SocketOption](../java.net/SocketOption.md)<*>!>! | [supportedOptions](NetworkChannel.md))`()` <br /> Returns a set of the socket options supported by this channel. This method will continue to return the set of options even after the channel has been closed. <br /> | ||
| From class [SelectableChannel](SelectableChannel.md) |------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [SelectionKey](SelectionKey.md)! | [register](SelectableChannel.md))`(`sel:` ` [Selector](Selector.md)!`, `ops:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Registers this channel with the given selector, returning a selection key. An invocation of this convenience method of the form `sc.register(sel, ops)`behaves in exactly the same way as the invocation`sc.` [register(sel, ops, null)](SelectableChannel.md)) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [validOps](SelectableChannel.md))`()` <br /> Returns an [operation set](SelectionKey.md) identifying this channel's supported operations. The bits that are set in this integer value denote exactly the operations that are valid for this channel. This method always returns the same value for a given concrete channel class. <br /> | ||

## Protected constructors

### ServerSocketChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected ServerSocketChannel(provider: SelectorProvider!)
```

Initializes a new instance of this class.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [SelectorProvider](../java.nio.channels.spi/SelectorProvider.md)!:The provider that created this channel |

## Public methods

### accept

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun accept(): SocketChannel!
```

Accepts a connection made to this channel's socket.

If this channel is in non-blocking mode then this method will immediately return`null`if there are no pending connections. Otherwise it will block indefinitely until a new connection is available or an I/O error occurs.

The socket channel returned by this method, if any, will be in blocking mode regardless of the blocking mode of this channel.

This method performs exactly the same security checks as the [accept](../java.net/ServerSocket.md))method of the class. That is, if a security manager has been installed then for each new connection this method verifies that the address and port number of the connection's remote endpoint are permitted by the security manager's [checkAccept](../java.lang/SecurityManager.md))method.

| Return ||
|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [SocketChannel](SocketChannel.md)! | The socket channel for the new connection, or`null`if this channel is in non-blocking mode and no connection is available to be accepted |

| Exceptions ||
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.AsynchronousCloseException` | If another thread closes this channel while the accept operation is in progress |
| `java.nio.channels.ClosedByInterruptException` | If another thread interrupts the current thread while the accept operation is in progress, thereby closing the channel and setting the current thread's interrupt status |
| --- | --- |
| `java.nio.channels.NotYetBoundException` | If this channel's socket has not yet been bound |
| `java.lang.SecurityException` | If a security manager has been installed and it does not permit access to the remote endpoint of the new connection |
| `java.io.IOException` | If some other I/O error occurs |
| --- | --- |

### bind

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun bind(local: SocketAddress!): ServerSocketChannel!
```

Binds the channel's socket to a local address and configures the socket to listen for connections.

An invocation of this method is equivalent to the following: 

```kotlin
bind(local, 0);
  
```

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `local` | [SocketAddress](../java.net/SocketAddress.md)!:The local address to bind the socket, or`null`to bind to an automatically assigned socket address |

| Return ||
|---------------------------------------------------------------------------------------------------------------|--------------|
| [ServerSocketChannel](ServerSocketChannel.md)! | This channel |

| Exceptions ||
|-----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.AlreadyBoundException` | If the socket is already bound |
| `java.nio.channels.UnsupportedAddressTypeException` | If the type of the given address is not supported |
| `java.nio.channels.ClosedChannelException` | If the channel is closed |
| --- | --- |
| `java.io.IOException` | If some other I/O error occurs |
| `java.lang.SecurityException` | If a security manager has been installed and its [checkListen](../java.lang/SecurityManager.md))method denies the operation |

### bind

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun bind(
    local: SocketAddress!, 
    backlog: Int
): ServerSocketChannel!
```

Binds the channel's socket to a local address and configures the socket to listen for connections.

This method is used to establish an association between the socket and a local address. Once an association is established then the socket remains bound until the channel is closed.

The`backlog`parameter is the maximum number of pending connections on the socket. Its exact semantics are implementation specific. In particular, an implementation may impose a maximum length or may choose to ignore the parameter altogther. If the`backlog`parameter has the value`0`, or a negative value, then an implementation specific default is used.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `local` | [SocketAddress](../java.net/SocketAddress.md)!:The address to bind the socket, or`null`to bind to an automatically assigned socket address |
| `backlog` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The maximum number of pending connections |

| Return ||
|---------------------------------------------------------------------------------------------------------------|--------------|
| [ServerSocketChannel](ServerSocketChannel.md)! | This channel |

| Exceptions ||
|-----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.AlreadyBoundException` | If the socket is already bound |
| `java.nio.channels.UnsupportedAddressTypeException` | If the type of the given address is not supported |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| --- | --- |
| `java.io.IOException` | If some other I/O error occurs |
| `java.lang.SecurityException` | If a security manager has been installed and its [checkListen](../java.lang/SecurityManager.md))method denies the operation |

### getLocalAddress

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLocalAddress(): SocketAddress!
```

Returns the socket address that this channel's socket is bound to.

Where the channel is [bound](NetworkChannel.md))to an Internet Protocol socket address then the return value from this method is of type .

If there is a security manager set, its`checkConnect`method is called with the local address and`-1`as its arguments to see if the operation is allowed. If the operation is not allowed, a`SocketAddress`representing the [loopback](../java.net/InetAddress.md))address and the local port of the channel's socket is returned.

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SocketAddress](../java.net/SocketAddress.md)! | The`SocketAddress`that the socket is bound to, or the`SocketAddress`representing the loopback address if denied by the security manager, or`null`if the channel's socket is not bound |

| Exceptions ||
|--------------------------------------------|--------------------------|
| `java.nio.channels.ClosedChannelException` | If the channel is closed |
| `java.io.IOException` | If an I/O error occurs |

### open

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun open(): ServerSocketChannel!
```

Opens a server-socket channel.

The new channel is created by invoking the [openServerSocketChannel](../java.nio.channels.spi/SelectorProvider.md))method of the system-wide default object.

The new channel's socket is initially unbound; it must be bound to a specific address via one of its socket's [bind](../java.net/ServerSocket.md))methods before connections can be accepted.

| Return ||
|---------------------------------------------------------------------------------------------------------------|----------------------|
| [ServerSocketChannel](ServerSocketChannel.md)! | A new socket channel |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |

### setOption

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <T : Any!> setOption(
    name: SocketOption<T>!, 
    value: T
): ServerSocketChannel!
```

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------|
| `<T>` | The type of the socket option value |
| `name` | [SocketOption](../java.net/SocketOption.md)\<T\>!:The socket option |
| `value` | T:The value of the socket option. A value of`null`may be a valid value for some socket options. |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------------------------------------|--------------|
| [ServerSocketChannel](ServerSocketChannel.md)! | This channel |

| Exceptions ||
|--------------------------------------------|----------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | If the socket option is not supported by this channel |
| `java.lang.IllegalArgumentException` | If the value is not a valid value for this socket option |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| --- | --- |
| `java.io.IOException` | If an I/O error occurs |

### socket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun socket(): ServerSocket!
```

Retrieves a server socket associated with this channel.

The returned object will not declare any public methods that are not declared in the [java.net.ServerSocket](../java.net/ServerSocket.md) class.

| Return ||
|---------------------------------------------------------------------------------------------|----------------------------------------------|
| [ServerSocket](../java.net/ServerSocket.md)! | A server socket associated with this channel |

### validOps

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun validOps(): Int
```

Returns an operation set identifying this channel's supported operations.

Server-socket channels only support the accepting of new connections, so this method returns [SelectionKey.OP_ACCEPT](SelectionKey.md).

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The valid-operation set |
