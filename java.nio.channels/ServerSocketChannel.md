# ServerSocketChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ServerSocketChannel

```
abstract class ServerSocketChannel : AbstractSelectableChannel, NetworkChannel
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [java.nio.channels.spi.AbstractInterruptibleChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel) ||||
| | ↳ | [java.nio.channels.SelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel) |||
| | | ↳ | [java.nio.channels.spi.AbstractSelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel) ||
| | | | ↳ | [java.nio.channels.ServerSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel#) |

A selectable channel for stream-oriented listening sockets.

A server-socket channel is created by invoking the [open](https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel#open())method of this class. It is not possible to create a channel for an arbitrary, pre-existing [ServerSocket](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#). A newly-created server-socket channel is open but not yet bound. An attempt to invoke the [accept](https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel#accept())method of an unbound server-socket channel will cause a [NotYetBoundException](https://developer.android.com/reference/kotlin/java/nio/channels/NotYetBoundException) to be thrown. A server-socket channel can be bound by invoking one of the [bind](https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel#bind(java.net.SocketAddress,%20kotlin.Int))methods defined by this class.

Socket options are configured using the [setOption](https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel#setOption(java.net.SocketOption,%20java.nio.channels.ServerSocketChannel.setOption.T))method. Server-socket channels support the following options:

| Option Name | Description |
| [SO_RCVBUF](https://developer.android.com/reference/kotlin/java/net/StandardSocketOptions.html#SO_RCVBUF:java.net.SocketOption) | The size of the socket receive buffer |
| [SO_REUSEADDR](https://developer.android.com/reference/kotlin/java/net/StandardSocketOptions.html#SO_REUSEADDR:java.net.SocketOption) | Re-use address |
|---------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|

Additional (implementation specific) options may also be supported.

Server-socket channels are safe for use by multiple concurrent threads.

## Summary

| Protected constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ServerSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel#ServerSocketChannel(java.nio.channels.spi.SelectorProvider))`(`provider:` ` [SelectorProvider](https://developer.android.com/reference/kotlin/java/nio/channels/spi/SelectorProvider)!`)` Initializes a new instance of this class. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [SocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel)! | [accept](https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel#accept())`()` Accepts a connection made to this channel's socket. |
| [ServerSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel#)! | [bind](https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel#bind(java.net.SocketAddress))`(`local:` ` [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#)!`)` Binds the channel's socket to a local address and configures the socket to listen for connections. |
| abstract [ServerSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel#)! | [bind](https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel#bind(java.net.SocketAddress,%20kotlin.Int))`(`local:` ` [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#)!`, `backlog:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Binds the channel's socket to a local address and configures the socket to listen for connections. |
| abstract [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#)! | [getLocalAddress](https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel#getLocalAddress())`()` Returns the socket address that this channel's socket is bound to. |
| openstatic [ServerSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel#)! | [open](https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel#open())`()` Opens a server-socket channel. |
| abstract [ServerSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel#)! | [setOption](https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel#setOption(java.net.SocketOption,%20java.nio.channels.ServerSocketChannel.setOption.T))`(`name:` ` [SocketOption](https://developer.android.com/reference/kotlin/java/net/SocketOption.html#)<T>!`, `value:` `T`)` <br /> |
| abstract [ServerSocket](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#)! | [socket](https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel#socket())`()` Retrieves a server socket associated with this channel. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [validOps](https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel#validOps())`()` Returns an operation set identifying this channel's supported operations. |

| Inherited functions ||
|---|---|
| From class [AbstractInterruptibleChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel) |------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [begin](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#begin())`()` <br /> Marks the beginning of an I/O operation that might block indefinitely. This method should be invoked in tandem with the [end](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#end(kotlin.Boolean))method, using a`try`...`finally`block as shown [above](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#be), in order to implement asynchronous closing and interruption for this channel. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#close())`()` <br /> Closes this channel. If the channel has already been closed then this method returns immediately. Otherwise it marks the channel as closed and then invokes the [implCloseChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#implCloseChannel())method in order to complete the close operation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [end](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#end(kotlin.Boolean))`(`completed:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Marks the end of an I/O operation that might block indefinitely. This method should be invoked in tandem with the [begin](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#begin())method, using a`try`...`finally`block as shown [above](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#be), in order to implement asynchronous closing and interruption for this channel. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [implCloseChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#implCloseChannel())`()` <br /> Closes this channel. This method is invoked by the #close method in order to perform the actual work of closing the channel. This method is only invoked if the channel has not yet been closed, and it is never invoked more than once. An implementation of this method must arrange for any other thread that is blocked in an I/O operation upon this channel to return immediately, either by throwing an exception or by returning normally. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpen](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#isOpen())`()` <br /> | ||
| From class [AbstractSelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel) |------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [blockingLock](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#blockingLock())`()` <br /> | | [SelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel)! | [configureBlocking](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#configureBlocking(kotlin.Boolean))`(`block:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Adjusts this channel's blocking mode. If the given blocking mode is different from the current blocking mode then this method invokes the [implConfigureBlocking](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#implConfigureBlocking(kotlin.Boolean))method, while holding the appropriate locks, in order to change the mode. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [implCloseChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#implCloseChannel())`()` <br /> Closes this channel. This method, which is specified in the [AbstractInterruptibleChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel) class and is invoked by the java.nio.channels.Channel#close method, in turn invokes the [implCloseSelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#implCloseSelectableChannel())method in order to perform the actual work of closing this channel. It then cancels all of this channel's keys. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [implCloseSelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#implCloseSelectableChannel())`()` <br /> Closes this selectable channel. This method is invoked by the java.nio.channels.Channel#close method in order to perform the actual work of closing the channel. This method is only invoked if the channel has not yet been closed, and it is never invoked more than once. An implementation of this method must arrange for any other thread that is blocked in an I/O operation upon this channel to return immediately, either by throwing an exception or by returning normally. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [implConfigureBlocking](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#implConfigureBlocking(kotlin.Boolean))`(`block:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Adjusts this channel's blocking mode. This method is invoked by the [configureBlocking](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#configureBlocking(kotlin.Boolean))method in order to perform the actual work of changing the blocking mode. This method is only invoked if the new mode is different from the current mode. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBlocking](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#isBlocking())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRegistered](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#isRegistered())`()` <br /> | | [SelectionKey](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey)! | [keyFor](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#keyFor(java.nio.channels.Selector))`(`sel:` ` [Selector](https://developer.android.com/reference/kotlin/java/nio/channels/Selector)!`)` <br /> | | [SelectorProvider](https://developer.android.com/reference/kotlin/java/nio/channels/spi/SelectorProvider)! | [provider](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#provider())`()` <br /> Returns the provider that created this channel. <br /> | | [SelectionKey](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey)! | [register](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#register(java.nio.channels.Selector,%20kotlin.Int,%20kotlin.Any))`(`sel:` ` [Selector](https://developer.android.com/reference/kotlin/java/nio/channels/Selector)!`, `ops:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `att:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Registers this channel with the given selector, returning a selection key. This method first verifies that this channel is open and that the given initial interest set is valid. If this channel is already registered with the given selector then the selection key representing that registration is returned after setting its interest set to the given value. Otherwise this channel has not yet been registered with the given selector, so the [register](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelector#register(java.nio.channels.spi.AbstractSelectableChannel,%20kotlin.Int,%20kotlin.Any))method of the selector is invoked while holding the appropriate locks. The resulting key is added to this channel's key set before being returned. <br /> | ||
| From class [Channel](https://developer.android.com/reference/kotlin/java/nio/channels/Channel) |------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/nio/channels/Channel#close())`()` <br /> Closes this channel. After a channel is closed, any further attempt to invoke I/O operations upon it will cause a [ClosedChannelException](https://developer.android.com/reference/kotlin/java/nio/channels/ClosedChannelException) to be thrown. If this channel is already closed then invoking this method has no effect. This method may be invoked at any time. If some other thread has already invoked it, however, then another invocation will block until the first invocation is complete, after which it will return without effect. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpen](https://developer.android.com/reference/kotlin/java/nio/channels/Channel#isOpen())`()` <br /> Tells whether or not this channel is open. <br /> | ||
| From class [NetworkChannel](https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel) |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | T | [getOption](https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel#getOption(java.net.SocketOption))`(`name:` ` [SocketOption](https://developer.android.com/reference/kotlin/java/net/SocketOption.html#)<T>!`)` <br /> Returns the value of a socket option. <br /> | | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [SocketOption](https://developer.android.com/reference/kotlin/java/net/SocketOption.html#)<*>!>! | [supportedOptions](https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel#supportedOptions())`()` <br /> Returns a set of the socket options supported by this channel. This method will continue to return the set of options even after the channel has been closed. <br /> | ||
| From class [SelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel) |------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [SelectionKey](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey)! | [register](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel#register(java.nio.channels.Selector,%20kotlin.Int))`(`sel:` ` [Selector](https://developer.android.com/reference/kotlin/java/nio/channels/Selector)!`, `ops:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Registers this channel with the given selector, returning a selection key. An invocation of this convenience method of the form `sc.register(sel, ops)`behaves in exactly the same way as the invocation`sc.` [register(sel, ops, null)](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel#register(java.nio.channels.Selector,%20kotlin.Int,%20kotlin.Any)) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [validOps](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel#validOps())`()` <br /> Returns an [operation set](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#opsets) identifying this channel's supported operations. The bits that are set in this integer value denote exactly the operations that are valid for this channel. This method always returns the same value for a given concrete channel class. <br /> | ||

## Protected constructors

### ServerSocketChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected ServerSocketChannel(provider: SelectorProvider!)
```

Initializes a new instance of this class.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [SelectorProvider](https://developer.android.com/reference/kotlin/java/nio/channels/spi/SelectorProvider)!:The provider that created this channel |

## Public methods

### accept

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun accept(): SocketChannel!
```

Accepts a connection made to this channel's socket.

If this channel is in non-blocking mode then this method will immediately return`null`if there are no pending connections. Otherwise it will block indefinitely until a new connection is available or an I/O error occurs.

The socket channel returned by this method, if any, will be in blocking mode regardless of the blocking mode of this channel.

This method performs exactly the same security checks as the [accept](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#accept())method of the class. That is, if a security manager has been installed then for each new connection this method verifies that the address and port number of the connection's remote endpoint are permitted by the security manager's [checkAccept](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkAccept(kotlin.String,%20kotlin.Int))method.

| Return ||
|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [SocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel)! | The socket channel for the new connection, or`null`if this channel is in non-blocking mode and no connection is available to be accepted |

| Exceptions ||
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.AsynchronousCloseException` | If another thread closes this channel while the accept operation is in progress |
| `java.nio.channels.ClosedByInterruptException` | If another thread interrupts the current thread while the accept operation is in progress, thereby closing the channel and setting the current thread's interrupt status |
| `java.nio.channels.NotYetBoundException` | If this channel's socket has not yet been bound |
| `java.lang.SecurityException` | If a security manager has been installed and it does not permit access to the remote endpoint of the new connection |
| `java.io.IOException` | If some other I/O error occurs |

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
| `local` | [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#)!:The local address to bind the socket, or`null`to bind to an automatically assigned socket address |

| Return ||
|---------------------------------------------------------------------------------------------------------------|--------------|
| [ServerSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel#)! | This channel |

| Exceptions ||
|-----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.AlreadyBoundException` | If the socket is already bound |
| `java.nio.channels.UnsupportedAddressTypeException` | If the type of the given address is not supported |
| `java.nio.channels.ClosedChannelException` | If the channel is closed |
| `java.io.IOException` | If some other I/O error occurs |
| `java.lang.SecurityException` | If a security manager has been installed and its [checkListen](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkListen(kotlin.Int))method denies the operation |

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
| `local` | [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#)!:The address to bind the socket, or`null`to bind to an automatically assigned socket address |
| `backlog` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The maximum number of pending connections |

| Return ||
|---------------------------------------------------------------------------------------------------------------|--------------|
| [ServerSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel#)! | This channel |

| Exceptions ||
|-----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.AlreadyBoundException` | If the socket is already bound |
| `java.nio.channels.UnsupportedAddressTypeException` | If the type of the given address is not supported |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.io.IOException` | If some other I/O error occurs |
| `java.lang.SecurityException` | If a security manager has been installed and its [checkListen](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkListen(kotlin.Int))method denies the operation |

### getLocalAddress

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLocalAddress(): SocketAddress!
```

Returns the socket address that this channel's socket is bound to.

Where the channel is [bound](https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel#bind(java.net.SocketAddress))to an Internet Protocol socket address then the return value from this method is of type .

If there is a security manager set, its`checkConnect`method is called with the local address and`-1`as its arguments to see if the operation is allowed. If the operation is not allowed, a`SocketAddress`representing the [loopback](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#getLoopbackAddress())address and the local port of the channel's socket is returned.

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#)! | The`SocketAddress`that the socket is bound to, or the`SocketAddress`representing the loopback address if denied by the security manager, or`null`if the channel's socket is not bound |

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

The new channel is created by invoking the [openServerSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/SelectorProvider#openServerSocketChannel())method of the system-wide default object.

The new channel's socket is initially unbound; it must be bound to a specific address via one of its socket's [bind](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#bind(java.net.SocketAddress))methods before connections can be accepted.

| Return ||
|---------------------------------------------------------------------------------------------------------------|----------------------|
| [ServerSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel#)! | A new socket channel |

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
| `name` | [SocketOption](https://developer.android.com/reference/kotlin/java/net/SocketOption.html#)\<T\>!:The socket option |
| `value` | T:The value of the socket option. A value of`null`may be a valid value for some socket options. |

| Return ||
|---------------------------------------------------------------------------------------------------------------|--------------|
| [ServerSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel#)! | This channel |

| Exceptions ||
|--------------------------------------------|----------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | If the socket option is not supported by this channel |
| `java.lang.IllegalArgumentException` | If the value is not a valid value for this socket option |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.io.IOException` | If an I/O error occurs |

### socket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun socket(): ServerSocket!
```

Retrieves a server socket associated with this channel.

The returned object will not declare any public methods that are not declared in the [java.net.ServerSocket](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#) class.

| Return ||
|---------------------------------------------------------------------------------------------|----------------------------------------------|
| [ServerSocket](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#)! | A server socket associated with this channel |

### validOps

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun validOps(): Int
```

Returns an operation set identifying this channel's supported operations.

Server-socket channels only support the accepting of new connections, so this method returns [SelectionKey.OP_ACCEPT](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#OP_ACCEPT:kotlin.Int).

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The valid-operation set |
