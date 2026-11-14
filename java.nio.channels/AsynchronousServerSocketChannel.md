# AsynchronousServerSocketChannel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AsynchronousServerSocketChannel

```
abstract class AsynchronousServerSocketChannel : AsynchronousChannel, NetworkChannel
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.nio.channels.AsynchronousServerSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousServerSocketChannel#) |

An asynchronous channel for stream-oriented listening sockets.

An asynchronous server-socket channel is created by invoking the #open method of this class. A newly-created asynchronous server-socket channel is open but not yet bound. It can be bound to a local address and configured to listen for connections by invoking the [bind](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousServerSocketChannel#bind(java.net.SocketAddress,%20kotlin.Int))method. Once bound, the [accept](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousServerSocketChannel#accept(java.nio.channels.AsynchronousServerSocketChannel.accept.A,%20java.nio.channels.CompletionHandler))method is used to initiate the accepting of connections to the channel's socket. An attempt to invoke the`accept`method on an unbound channel will cause a [NotYetBoundException](https://developer.android.com/reference/kotlin/java/nio/channels/NotYetBoundException) to be thrown.

Channels of this type are safe for use by multiple concurrent threads though at most one accept operation can be outstanding at any time. If a thread initiates an accept operation before a previous accept operation has completed then an [AcceptPendingException](https://developer.android.com/reference/kotlin/java/nio/channels/AcceptPendingException) will be thrown.

Socket options are configured using the [setOption](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousServerSocketChannel#setOption(java.net.SocketOption,%20java.nio.channels.AsynchronousServerSocketChannel.setOption.T))method. Channels of this type support the following options:

| Option Name | Description |
| [SO_RCVBUF](https://developer.android.com/reference/kotlin/java/net/StandardSocketOptions.html#SO_RCVBUF:java.net.SocketOption) | The size of the socket receive buffer |
| [SO_REUSEADDR](https://developer.android.com/reference/kotlin/java/net/StandardSocketOptions.html#SO_REUSEADDR:java.net.SocketOption) | Re-use address |
|---------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|

Additional (implementation specific) options may also be supported.

**Usage Example:** 

```kotlin
final AsynchronousServerSocketChannel listener =
       AsynchronousServerSocketChannel.open().bind(new InetSocketAddress(5000));
 
   listener.accept(null, new CompletionHandler<AsynchronousSocketChannel,Void>() {
       public void completed(AsynchronousSocketChannel ch, Void att) {
           // accept the next connection
           listener.accept(null, this);
 
           // handle this connection
           handle(ch);
       }
       public void failed(Throwable exc, Void att) {
           ...
       }
   });
  
```

## Summary

| Protected constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AsynchronousServerSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousServerSocketChannel#AsynchronousServerSocketChannel(java.nio.channels.spi.AsynchronousChannelProvider))`(`provider:` ` [AsynchronousChannelProvider](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AsynchronousChannelProvider)!`)` Initializes a new instance of this class. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future.html#)\< [AsynchronousSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel)!\>! | [accept](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousServerSocketChannel#accept())`()` Accepts a connection. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [accept](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousServerSocketChannel#accept(java.nio.channels.AsynchronousServerSocketChannel.accept.A,%20java.nio.channels.CompletionHandler))`(`attachment:` `A`, `handler:` ` [CompletionHandler](https://developer.android.com/reference/kotlin/java/nio/channels/CompletionHandler)< [AsynchronousSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel)!,` `in` `A>!`)` Accepts a connection. |
| [AsynchronousServerSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousServerSocketChannel#)! | [bind](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousServerSocketChannel#bind(java.net.SocketAddress))`(`local:` ` [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#)!`)` Binds the channel's socket to a local address and configures the socket to listen for connections. |
| abstract [AsynchronousServerSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousServerSocketChannel#)! | [bind](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousServerSocketChannel#bind(java.net.SocketAddress,%20kotlin.Int))`(`local:` ` [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#)!`, `backlog:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Binds the channel's socket to a local address and configures the socket to listen for connections. |
| abstract [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#)! | [getLocalAddress](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousServerSocketChannel#getLocalAddress())`()` Returns the socket address that this channel's socket is bound to. |
| openstatic [AsynchronousServerSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousServerSocketChannel#)! | [open](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousServerSocketChannel#open())`()` Opens an asynchronous server-socket channel. |
| openstatic [AsynchronousServerSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousServerSocketChannel#)! | [open](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousServerSocketChannel#open(java.nio.channels.AsynchronousChannelGroup))`(`group:` ` [AsynchronousChannelGroup](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup)!`)` Opens an asynchronous server-socket channel. |
| [AsynchronousChannelProvider](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AsynchronousChannelProvider)! | [provider](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousServerSocketChannel#provider())`()` Returns the provider that created this channel. |
| abstract [AsynchronousServerSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousServerSocketChannel#)! | [setOption](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousServerSocketChannel#setOption(java.net.SocketOption,%20java.nio.channels.AsynchronousServerSocketChannel.setOption.T))`(`name:` ` [SocketOption](https://developer.android.com/reference/kotlin/java/net/SocketOption.html#)<T>!`, `value:` `T`)` <br /> |

| Inherited functions ||
|---|---|
| From class [AsynchronousChannel](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannel) |------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannel#close())`()` <br /> Closes this channel. Any outstanding asynchronous operations upon this channel will complete with the exception [AsynchronousCloseException](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousCloseException). After a channel is closed, further attempts to initiate asynchronous I/O operations complete immediately with cause [ClosedChannelException](https://developer.android.com/reference/kotlin/java/nio/channels/ClosedChannelException). This method otherwise behaves exactly as specified by the [Channel](https://developer.android.com/reference/kotlin/java/nio/channels/Channel) interface. <br /> | ||
| From class [Channel](https://developer.android.com/reference/kotlin/java/nio/channels/Channel) |------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/nio/channels/Channel#close())`()` <br /> Closes this channel. After a channel is closed, any further attempt to invoke I/O operations upon it will cause a [ClosedChannelException](https://developer.android.com/reference/kotlin/java/nio/channels/ClosedChannelException) to be thrown. If this channel is already closed then invoking this method has no effect. This method may be invoked at any time. If some other thread has already invoked it, however, then another invocation will block until the first invocation is complete, after which it will return without effect. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpen](https://developer.android.com/reference/kotlin/java/nio/channels/Channel#isOpen())`()` <br /> Tells whether or not this channel is open. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpen](https://developer.android.com/reference/kotlin/java/nio/channels/Channel#isOpen())`()` <br /> Tells whether or not this channel is open. <br /> | ||
| From class [NetworkChannel](https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel) |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | T | [getOption](https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel#getOption(java.net.SocketOption))`(`name:` ` [SocketOption](https://developer.android.com/reference/kotlin/java/net/SocketOption.html#)<T>!`)` <br /> Returns the value of a socket option. <br /> | | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [SocketOption](https://developer.android.com/reference/kotlin/java/net/SocketOption.html#)<*>!>! | [supportedOptions](https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel#supportedOptions())`()` <br /> Returns a set of the socket options supported by this channel. This method will continue to return the set of options even after the channel has been closed. <br /> | ||

## Protected constructors

### AsynchronousServerSocketChannel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected AsynchronousServerSocketChannel(provider: AsynchronousChannelProvider!)
```

Initializes a new instance of this class.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [AsynchronousChannelProvider](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AsynchronousChannelProvider)!:The provider that created this channel |

## Public methods

### accept

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun accept(): Future<AsynchronousSocketChannel!>!
```

Accepts a connection.

This method initiates an asynchronous operation to accept a connection made to this channel's socket. The method behaves in exactly the same manner as the [accept(java.lang.Object,java.nio.channels.CompletionHandler)](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousServerSocketChannel#accept(java.nio.channels.AsynchronousServerSocketChannel.accept.A,%20java.nio.channels.CompletionHandler))method except that instead of specifying a completion handler, this method returns a`Future`representing the pending result. The`Future`'s [get](https://developer.android.com/reference/kotlin/java/util/concurrent/Future.html#get())method returns the [AsynchronousSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel) to the new connection on successful completion.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future.html#)< [AsynchronousSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel)!>! | a`Future`object representing the pending result |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------|
| `java.nio.channels.AcceptPendingException` | If an accept operation is already in progress on this channel |
| `java.nio.channels.NotYetBoundException` | If this channel's socket has not yet been bound |

### accept

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <A : Any!> accept(
    attachment: A, 
    handler: CompletionHandler<AsynchronousSocketChannel!, in A>!
): Unit
```

Accepts a connection.

This method initiates an asynchronous operation to accept a connection made to this channel's socket. The`handler`parameter is a completion handler that is invoked when a connection is accepted (or the operation fails). The result passed to the completion handler is the [AsynchronousSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel) to the new connection.

When a new connection is accepted then the resulting`AsynchronousSocketChannel`will be bound to the same [AsynchronousChannelGroup](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup) as this channel. If the group is [shutdown](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup#isShutdown())and a connection is accepted, then the connection is closed, and the operation completes with an`IOException`and cause [ShutdownChannelGroupException](https://developer.android.com/reference/kotlin/java/nio/channels/ShutdownChannelGroupException).

To allow for concurrent handling of new connections, the completion handler is not invoked directly by the initiating thread when a new connection is accepted immediately (see [Threading](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup#threading)).

If a security manager has been installed then it verifies that the address and port number of the connection's remote endpoint are permitted by the security manager's [checkAccept](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkAccept(kotlin.String,%20kotlin.Int))method. The permission check is performed with privileges that are restricted by the calling context of this method. If the permission check fails then the connection is closed and the operation completes with a [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#).

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<A>` | The type of the attachment |
| `attachment` | A:The object to attach to the I/O operation; can be`null` |
| `handler` | [CompletionHandler](https://developer.android.com/reference/kotlin/java/nio/channels/CompletionHandler)\< [AsynchronousSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel)!,inA\>!:The handler for consuming the result |

| Exceptions ||
|---------------------------------------------------|---------------------------------------------------------------|
| `java.nio.channels.AcceptPendingException` | If an accept operation is already in progress on this channel |
| `java.nio.channels.NotYetBoundException` | If this channel's socket has not yet been bound |
| `java.nio.channels.ShutdownChannelGroupException` | If the channel group has terminated |

### bind

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun bind(local: SocketAddress!): AsynchronousServerSocketChannel!
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
|---------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [AsynchronousServerSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousServerSocketChannel#)! | This channel |

| Exceptions ||
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.AlreadyBoundException` | If the socket is already bound |
| `java.nio.channels.UnsupportedAddressTypeException` | If the type of the given address is not supported |
| `java.nio.channels.ClosedChannelException` | If the channel is closed |
| `java.io.IOException` | If some other I/O error occurs |
| `java.lang.SecurityException` | If a security manager is installed and it denies an unspecified permission. An implementation of this interface should specify any required permissions. |

### bind

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun bind(
    local: SocketAddress!, 
    backlog: Int
): AsynchronousServerSocketChannel!
```

Binds the channel's socket to a local address and configures the socket to listen for connections.

This method is used to establish an association between the socket and a local address. Once an association is established then the socket remains bound until the associated channel is closed.

The`backlog`parameter is the maximum number of pending connections on the socket. Its exact semantics are implementation specific. In particular, an implementation may impose a maximum length or may choose to ignore the parameter altogther. If the`backlog`parameter has the value`0`, or a negative value, then an implementation specific default is used.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `local` | [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#)!:The local address to bind the socket, or`null`to bind to an automatically assigned socket address |
| `backlog` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The maximum number of pending connections |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [AsynchronousServerSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousServerSocketChannel#)! | This channel |

| Exceptions ||
|-----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.AlreadyBoundException` | If the socket is already bound |
| `java.nio.channels.UnsupportedAddressTypeException` | If the type of the given address is not supported |
| `java.lang.SecurityException` | If a security manager has been installed and its [checkListen](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkListen(kotlin.Int))method denies the operation |
| `java.nio.channels.ClosedChannelException` | If the channel is closed |
| `java.io.IOException` | If some other I/O error occurs |

### getLocalAddress

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun open(): AsynchronousServerSocketChannel!
```

Opens an asynchronous server-socket channel.

This method returns an asynchronous server socket channel that is bound to the*default group*. This method is equivalent to evaluating the expression: 

```kotlin
open((AsynchronousChannelGroup)null);
  
```

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| [AsynchronousServerSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousServerSocketChannel#)! | A new asynchronous server socket channel |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |

### open

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun open(group: AsynchronousChannelGroup!): AsynchronousServerSocketChannel!
```

Opens an asynchronous server-socket channel.

The new channel is created by invoking the [openAsynchronousServerSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AsynchronousChannelProvider#openAsynchronousServerSocketChannel(java.nio.channels.AsynchronousChannelGroup))method on the object that created the given group. If the group parameter is`null`then the resulting channel is created by the system-wide default provider, and bound to the*default group*.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `group` | [AsynchronousChannelGroup](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup)!:The group to which the newly constructed channel should be bound, or`null`for the default group |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| [AsynchronousServerSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousServerSocketChannel#)! | A new asynchronous server socket channel |

| Exceptions ||
|---------------------------------------------------|----------------------------------|
| `java.nio.channels.ShutdownChannelGroupException` | If the channel group is shutdown |
| `java.io.IOException` | If an I/O error occurs |

### provider

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun provider(): AsynchronousChannelProvider!
```

Returns the provider that created this channel.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| [AsynchronousChannelProvider](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AsynchronousChannelProvider)! | The provider that created this channel |

### setOption

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <T : Any!> setOption(
    name: SocketOption<T>!, 
    value: T
): AsynchronousServerSocketChannel!
```

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------|
| `<T>` | The type of the socket option value |
| `name` | [SocketOption](https://developer.android.com/reference/kotlin/java/net/SocketOption.html#)\<T\>!:The socket option |
| `value` | T:The value of the socket option. A value of`null`may be a valid value for some socket options. |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [AsynchronousServerSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousServerSocketChannel#)! | This channel |

| Exceptions ||
|--------------------------------------------|----------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | If the socket option is not supported by this channel |
| `java.lang.IllegalArgumentException` | If the value is not a valid value for this socket option |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.io.IOException` | If an I/O error occurs |
