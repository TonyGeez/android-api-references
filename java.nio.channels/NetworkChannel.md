Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NetworkChannel

```
interface NetworkChannel : Channel
```

| [java.nio.channels.NetworkChannel](../java/nio/channels/NetworkChannel.md) |

| Known Direct Subclasses [AsynchronousServerSocketChannel](../java/nio/channels/AsynchronousServerSocketChannel.md), [AsynchronousSocketChannel](../java/nio/channels/AsynchronousSocketChannel.md), [MulticastChannel](../java/nio/channels/MulticastChannel.md), [ServerSocketChannel](../java/nio/channels/ServerSocketChannel.md), [SocketChannel](../java/nio/channels/SocketChannel.md) |---|---| | [AsynchronousServerSocketChannel](../java/nio/channels/AsynchronousServerSocketChannel.md) | An asynchronous channel for stream-oriented listening sockets. | | [AsynchronousSocketChannel](../java/nio/channels/AsynchronousSocketChannel.md) | An asynchronous channel for stream-oriented connecting sockets. | | [MulticastChannel](../java/nio/channels/MulticastChannel.md) | A network channel that supports Internet Protocol (IP) multicasting. | | [ServerSocketChannel](../java/nio/channels/ServerSocketChannel.md) | A selectable channel for stream-oriented listening sockets. | | [SocketChannel](../java/nio/channels/SocketChannel.md) | A selectable channel for stream-oriented connecting sockets. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [DatagramChannel](../java/nio/channels/DatagramChannel.md) |---|---| | [DatagramChannel](../java/nio/channels/DatagramChannel.md) | A selectable channel for datagram-oriented sockets. | |
| --- | --- | --- | --- | --- | --- | --- |

A channel to a network socket.

A channel that implements this interface is a channel to a network socket. The `https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel#bind(java.net.SocketAddress)` method is used to bind the socket to a local `https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#`, the `https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel#getLocalAddress()` method returns the address that the socket is bound to, and the `https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel#setOption(java.net.SocketOption,%20java.nio.channels.NetworkChannel.setOption.T)` and `https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel#getOption(java.net.SocketOption)` methods are used to set and query socket options. An implementation of this interface should specify the socket options that it supports.

The `https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel#bind(java.net.SocketAddress)` and `https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel#setOption(java.net.SocketOption,%20java.nio.channels.NetworkChannel.setOption.T)` methods that do not otherwise have a value to return are specified to return the network channel upon which they are invoked. This allows method invocations to be chained. Implementations of this interface should specialize the return type so that method invocations on the implementation class can be chained.

## Summary

| Public methods ||
|---|---|
| abstract [NetworkChannel](../java/nio/channels/NetworkChannel.md)! | `https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel#bind(java.net.SocketAddress)(local: https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#!)` Binds the channel's socket to a local address. |
| abstract [SocketAddress](../java/net/SocketAddress.md)! | `https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel#getLocalAddress()()` Returns the socket address that this channel's socket is bound to. |
| abstract T | `https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel#getOption(java.net.SocketOption)(name: https://developer.android.com/reference/kotlin/java/net/SocketOption.html#<T>!)` Returns the value of a socket option. |
| --- | --- |
| abstract [NetworkChannel](../java/nio/channels/NetworkChannel.md)! | `https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel#setOption(java.net.SocketOption,%20java.nio.channels.NetworkChannel.setOption.T)(name: https://developer.android.com/reference/kotlin/java/net/SocketOption.html#<T>!, value: T)` Sets the value of a socket option. |
| abstract [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [SocketOption](../java/net/SocketOption.md)\<\*\>!\>! | `https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel#supportedOptions()()` Returns a set of the socket options supported by this channel. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/nio/channels/Channel` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/nio/channels/Channel#close()()` Closes this channel. After a channel is closed, any further attempt to invoke I/O operations upon it will cause a `https://developer.android.com/reference/kotlin/java/nio/channels/ClosedChannelException` to be thrown. If this channel is already closed then invoking this method has no effect. This method may be invoked at any time. If some other thread has already invoked it, however, then another invocation will block until the first invocation is complete, after which it will return without effect. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/nio/channels/Channel#isOpen()()` Tells whether or not this channel is open. <br /> | ||

## Public methods

### bind

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun bind(local: SocketAddress!): NetworkChannel!
```

Binds the channel's socket to a local address.

This method is used to establish an association between the socket and a local address. Once an association is established then the socket remains bound until the channel is closed. If the `local` parameter has the value `null` then the socket will be bound to an address that is assigned automatically.

| Parameters ||
|---|---|
| `local` | [SocketAddress](../java/net/SocketAddress.md)!: The address to bind the socket, or `null` to bind the socket to an automatically assigned socket address |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel#!` | This channel |

| Exceptions ||
|---|---|
| `java.io.IOException` | If some other I/O error occurs |
| `java.lang.SecurityException` | If a security manager is installed and it denies an unspecified permission. An implementation of this interface should specify any required permissions. |
| `java.nio.channels.AlreadyBoundException` | If the socket is already bound |
| --- | --- |
| `java.nio.channels.ClosedChannelException` | If the channel is closed |
| `java.nio.channels.UnsupportedAddressTypeException` | If the type of the given address is not supported |

**See Also**

- `https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel#getLocalAddress()`

### getLocalAddress

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getLocalAddress(): SocketAddress!
```

Returns the socket address that this channel's socket is bound to.

Where the channel is `https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel#bind(java.net.SocketAddress)` to an Internet Protocol socket address then the return value from this method is of type `https://developer.android.com/reference/kotlin/java/net/InetSocketAddress.html#`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#!` | The socket address that the socket is bound to, or `null` if the channel's socket is not bound |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |
| `java.nio.channels.ClosedChannelException` | If the channel is closed |

### getOption

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun <T : Any!> getOption(name: SocketOption<T>!): T
```

Returns the value of a socket option.

| Parameters ||
|---|---|
| `<T>` | The type of the socket option value |
| `name` | [SocketOption](../java/net/SocketOption.md)\<T\>!: The socket option |

| Return ||
|---|---|
| `T` | The value of the socket option. A value of `null` may be a valid value for some socket options. |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |
| `java.lang.UnsupportedOperationException` | If the socket option is not supported by this channel |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/StandardSocketOptions.html#`

### setOption

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun <T : Any!> setOption(
    name: SocketOption<T>!, 
    value: T
): NetworkChannel!
```

Sets the value of a socket option.

| Parameters ||
|---|---|
| `<T>` | The type of the socket option value |
| `name` | [SocketOption](../java/net/SocketOption.md)\<T\>!: The socket option |
| `value` | T: The value of the socket option. A value of `null` may be a valid value for some socket options. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel#!` | This channel |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |
| `java.lang.IllegalArgumentException` | If the value is not a valid value for this socket option |
| `java.lang.UnsupportedOperationException` | If the socket option is not supported by this channel |
| --- | --- |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/StandardSocketOptions.html#`

### supportedOptions

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun supportedOptions(): MutableSet<SocketOption<*>!>!
```

Returns a set of the socket options supported by this channel.

This method will continue to return the set of options even after the channel has been closed.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/java/net/SocketOption.html#<*>!>!` | A set of the socket options supported by this channel |
