# AsynchronousServerSocketChannel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AsynchronousServerSocketChannel

```
abstract class AsynchronousServerSocketChannel : AsynchronousChannel, NetworkChannel
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.nio.channels.AsynchronousServerSocketChannel](../java/nio/channels/AsynchronousServerSocketChannel.md) |

An asynchronous channel for stream-oriented listening sockets.

An asynchronous server-socket channel is created by invoking the #open method of this class. A newly-created asynchronous server-socket channel is open but not yet bound. It can be bound to a local address and configured to listen for connections by invoking the [bind](../java/nio/channels/AsynchronousServerSocketChannel.md))method. Once bound, the [accept](../java/nio/channels/AsynchronousServerSocketChannel.md))method is used to initiate the accepting of connections to the channel's socket. An attempt to invoke the`accept`method on an unbound channel will cause a [NotYetBoundException](../java/nio/channels/NotYetBoundException.md) to be thrown.

Channels of this type are safe for use by multiple concurrent threads though at most one accept operation can be outstanding at any time. If a thread initiates an accept operation before a previous accept operation has completed then an [AcceptPendingException](../java/nio/channels/AcceptPendingException.md) will be thrown.

Socket options are configured using the [setOption](../java/nio/channels/AsynchronousServerSocketChannel.md))method. Channels of this type support the following options:

| Option Name | Description |
| --- | --- |
| [SO_RCVBUF](../java/net/StandardSocketOptions.md) | The size of the socket receive buffer |
| [SO_REUSEADDR](../java/net/StandardSocketOptions.md) | Re-use address |
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
| [AsynchronousServerSocketChannel](../java/nio/channels/AsynchronousServerSocketChannel.md))`(`provider:` ` [AsynchronousChannelProvider](../java/nio/channels/spi/AsynchronousChannelProvider.md)!`)` Initializes a new instance of this class. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Future](../java/util/concurrent/Future.md)\< [AsynchronousSocketChannel](../java/nio/channels/AsynchronousSocketChannel.md)!\>! | [accept](../java/nio/channels/AsynchronousServerSocketChannel.md))`()` Accepts a connection. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [accept](../java/nio/channels/AsynchronousServerSocketChannel.md))`(`attachment:` `A`, `handler:` ` [CompletionHandler](../java/nio/channels/CompletionHandler.md)< [AsynchronousSocketChannel](../java/nio/channels/AsynchronousSocketChannel.md)!,` `in` `A>!`)` Accepts a connection. |
| [AsynchronousServerSocketChannel](../java/nio/channels/AsynchronousServerSocketChannel.md)! | [bind](../java/nio/channels/AsynchronousServerSocketChannel.md))`(`local:` ` [SocketAddress](../java/net/SocketAddress.md)!`)` Binds the channel's socket to a local address and configures the socket to listen for connections. |
| --- | --- |
| abstract [AsynchronousServerSocketChannel](../java/nio/channels/AsynchronousServerSocketChannel.md)! | [bind](../java/nio/channels/AsynchronousServerSocketChannel.md))`(`local:` ` [SocketAddress](../java/net/SocketAddress.md)!`, `backlog:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Binds the channel's socket to a local address and configures the socket to listen for connections. |
| abstract [SocketAddress](../java/net/SocketAddress.md)! | [getLocalAddress](../java/nio/channels/AsynchronousServerSocketChannel.md))`()` Returns the socket address that this channel's socket is bound to. |
| openstatic [AsynchronousServerSocketChannel](../java/nio/channels/AsynchronousServerSocketChannel.md)! | [open](../java/nio/channels/AsynchronousServerSocketChannel.md))`()` Opens an asynchronous server-socket channel. |
| --- | --- |
| openstatic [AsynchronousServerSocketChannel](../java/nio/channels/AsynchronousServerSocketChannel.md)! | [open](../java/nio/channels/AsynchronousServerSocketChannel.md))`(`group:` ` [AsynchronousChannelGroup](../java/nio/channels/AsynchronousChannelGroup.md)!`)` Opens an asynchronous server-socket channel. |
| [AsynchronousChannelProvider](../java/nio/channels/spi/AsynchronousChannelProvider.md)! | [provider](../java/nio/channels/AsynchronousServerSocketChannel.md))`()` Returns the provider that created this channel. |
| abstract [AsynchronousServerSocketChannel](../java/nio/channels/AsynchronousServerSocketChannel.md)! | [setOption](../java/nio/channels/AsynchronousServerSocketChannel.md))`(`name:` ` [SocketOption](../java/net/SocketOption.md)<T>!`, `value:` `T`)` <br /> |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [AsynchronousChannel](../java/nio/channels/AsynchronousChannel.md) |------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../java/nio/channels/AsynchronousChannel.md))`()` <br /> Closes this channel. Any outstanding asynchronous operations upon this channel will complete with the exception [AsynchronousCloseException](../java/nio/channels/AsynchronousCloseException.md). After a channel is closed, further attempts to initiate asynchronous I/O operations complete immediately with cause [ClosedChannelException](../java/nio/channels/ClosedChannelException.md). This method otherwise behaves exactly as specified by the [Channel](../java/nio/channels/Channel.md) interface. <br /> | ||
| From class [Channel](../java/nio/channels/Channel.md) |------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../java/nio/channels/Channel.md))`()` <br /> Closes this channel. After a channel is closed, any further attempt to invoke I/O operations upon it will cause a [ClosedChannelException](../java/nio/channels/ClosedChannelException.md) to be thrown. If this channel is already closed then invoking this method has no effect. This method may be invoked at any time. If some other thread has already invoked it, however, then another invocation will block until the first invocation is complete, after which it will return without effect. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpen](../java/nio/channels/Channel.md))`()` <br /> Tells whether or not this channel is open. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpen](../java/nio/channels/Channel.md))`()` <br /> Tells whether or not this channel is open. <br /> | ||
| From class [NetworkChannel](../java/nio/channels/NetworkChannel.md) |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | T | [getOption](../java/nio/channels/NetworkChannel.md))`(`name:` ` [SocketOption](../java/net/SocketOption.md)<T>!`)` <br /> Returns the value of a socket option. <br /> | | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [SocketOption](../java/net/SocketOption.md)<*>!>! | [supportedOptions](../java/nio/channels/NetworkChannel.md))`()` <br /> Returns a set of the socket options supported by this channel. This method will continue to return the set of options even after the channel has been closed. <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

## Protected constructors

### AsynchronousServerSocketChannel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected AsynchronousServerSocketChannel(provider: AsynchronousChannelProvider!)
```

Initializes a new instance of this class.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [AsynchronousChannelProvider](../java/nio/channels/spi/AsynchronousChannelProvider.md)!:The provider that created this channel |

## Public methods

### accept

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun accept(): Future<AsynchronousSocketChannel!>!
```

Accepts a connection.

This method initiates an asynchronous operation to accept a connection made to this channel's socket. The method behaves in exactly the same manner as the [accept(java.lang.Object,java.nio.channels.CompletionHandler)](../java/nio/channels/AsynchronousServerSocketChannel.md))method except that instead of specifying a completion handler, this method returns a`Future`representing the pending result. The`Future`'s [get](../java/util/concurrent/Future.md))method returns the [AsynchronousSocketChannel](../java/nio/channels/AsynchronousSocketChannel.md) to the new connection on successful completion.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| [Future](../java/util/concurrent/Future.md)< [AsynchronousSocketChannel](../java/nio/channels/AsynchronousSocketChannel.md)!>! | a`Future`object representing the pending result |

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

This method initiates an asynchronous operation to accept a connection made to this channel's socket. The`handler`parameter is a completion handler that is invoked when a connection is accepted (or the operation fails). The result passed to the completion handler is the [AsynchronousSocketChannel](../java/nio/channels/AsynchronousSocketChannel.md) to the new connection.

When a new connection is accepted then the resulting`AsynchronousSocketChannel`will be bound to the same [AsynchronousChannelGroup](../java/nio/channels/AsynchronousChannelGroup.md) as this channel. If the group is [shutdown](../java/nio/channels/AsynchronousChannelGroup.md))and a connection is accepted, then the connection is closed, and the operation completes with an`IOException`and cause [ShutdownChannelGroupException](../java/nio/channels/ShutdownChannelGroupException.md).

To allow for concurrent handling of new connections, the completion handler is not invoked directly by the initiating thread when a new connection is accepted immediately (see [Threading](../java/nio/channels/AsynchronousChannelGroup.md)).

If a security manager has been installed then it verifies that the address and port number of the connection's remote endpoint are permitted by the security manager's [checkAccept](../java/lang/SecurityManager.md))method. The permission check is performed with privileges that are restricted by the calling context of this method. If the permission check fails then the connection is closed and the operation completes with a [SecurityException](../java/lang/SecurityException.md).

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<A>` | The type of the attachment |
| `attachment` | A:The object to attach to the I/O operation; can be`null` |
| `handler` | [CompletionHandler](../java/nio/channels/CompletionHandler.md)\< [AsynchronousSocketChannel](../java/nio/channels/AsynchronousSocketChannel.md)!,inA\>!:The handler for consuming the result |
| --- | --- |

| Exceptions ||
|---------------------------------------------------|---------------------------------------------------------------|
| `java.nio.channels.AcceptPendingException` | If an accept operation is already in progress on this channel |
| `java.nio.channels.NotYetBoundException` | If this channel's socket has not yet been bound |
| `java.nio.channels.ShutdownChannelGroupException` | If the channel group has terminated |
| --- | --- |

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
| `local` | [SocketAddress](../java/net/SocketAddress.md)!:The local address to bind the socket, or`null`to bind to an automatically assigned socket address |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [AsynchronousServerSocketChannel](../java/nio/channels/AsynchronousServerSocketChannel.md)! | This channel |

| Exceptions ||
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.AlreadyBoundException` | If the socket is already bound |
| `java.nio.channels.UnsupportedAddressTypeException` | If the type of the given address is not supported |
| `java.nio.channels.ClosedChannelException` | If the channel is closed |
| --- | --- |
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
| `local` | [SocketAddress](../java/net/SocketAddress.md)!:The local address to bind the socket, or`null`to bind to an automatically assigned socket address |
| `backlog` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The maximum number of pending connections |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [AsynchronousServerSocketChannel](../java/nio/channels/AsynchronousServerSocketChannel.md)! | This channel |

| Exceptions ||
|-----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.AlreadyBoundException` | If the socket is already bound |
| `java.nio.channels.UnsupportedAddressTypeException` | If the type of the given address is not supported |
| `java.lang.SecurityException` | If a security manager has been installed and its [checkListen](../java/lang/SecurityManager.md))method denies the operation |
| --- | --- |
| `java.nio.channels.ClosedChannelException` | If the channel is closed |
| `java.io.IOException` | If some other I/O error occurs |

### getLocalAddress

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
| [AsynchronousServerSocketChannel](../java/nio/channels/AsynchronousServerSocketChannel.md)! | A new asynchronous server socket channel |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |

### open

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun open(group: AsynchronousChannelGroup!): AsynchronousServerSocketChannel!
```

Opens an asynchronous server-socket channel.

The new channel is created by invoking the [openAsynchronousServerSocketChannel](../java/nio/channels/spi/AsynchronousChannelProvider.md))method on the object that created the given group. If the group parameter is`null`then the resulting channel is created by the system-wide default provider, and bound to the*default group*.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `group` | [AsynchronousChannelGroup](../java/nio/channels/AsynchronousChannelGroup.md)!:The group to which the newly constructed channel should be bound, or`null`for the default group |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| [AsynchronousServerSocketChannel](../java/nio/channels/AsynchronousServerSocketChannel.md)! | A new asynchronous server socket channel |

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
| [AsynchronousChannelProvider](../java/nio/channels/spi/AsynchronousChannelProvider.md)! | The provider that created this channel |

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
| `name` | [SocketOption](../java/net/SocketOption.md)\<T\>!:The socket option |
| `value` | T:The value of the socket option. A value of`null`may be a valid value for some socket options. |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [AsynchronousServerSocketChannel](../java/nio/channels/AsynchronousServerSocketChannel.md)! | This channel |

| Exceptions ||
|--------------------------------------------|----------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | If the socket option is not supported by this channel |
| `java.lang.IllegalArgumentException` | If the value is not a valid value for this socket option |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| --- | --- |
| `java.io.IOException` | If an I/O error occurs |
