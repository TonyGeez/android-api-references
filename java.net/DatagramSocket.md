Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DatagramSocket

```
open class DatagramSocket : Closeable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.net.DatagramSocket](DatagramSocket.md) |

| Known Direct Subclasses [MulticastSocket](MulticastSocket.md) |---|---| | [MulticastSocket](MulticastSocket.md) | The multicast datagram socket class is useful for sending and receiving IP multicast packets. | |
| --- | --- | --- | --- | --- | --- | --- |

This class represents a socket for sending and receiving datagram packets.

A datagram socket is the sending or receiving point for a packet delivery service. Each packet sent or received on a datagram socket is individually addressed and routed. Multiple packets sent from one machine to another may be routed differently, and may arrive in any order.

Where possible, a newly constructed `DatagramSocket` has the `https://developer.android.com/reference/kotlin/java/net/SocketOptions#SO_BROADCAST:kotlin.Int` socket option enabled so as to allow the transmission of broadcast datagrams. In order to receive broadcast packets a DatagramSocket should be bound to the wildcard address. In some implementations, broadcast packets may also be received when a DatagramSocket is bound to a more specific address.

Example: `DatagramSocket s = new DatagramSocket(null); s.bind(new InetSocketAddress(8888)); ` Which is equivalent to: `DatagramSocket s = new DatagramSocket(8888); ` Both cases will create a DatagramSocket able to receive broadcasts on UDP port 8888.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#DatagramSocket()()` Constructs a datagram socket and binds it to any available port on the local host machine. |
| `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#DatagramSocket(kotlin.Int)(port: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Constructs a datagram socket and binds it to the specified port on the local host machine. |
| `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#DatagramSocket(kotlin.Int,%20java.net.InetAddress)(port: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, laddr: https://developer.android.com/reference/kotlin/java/net/InetAddress!)` Creates a datagram socket, bound to the specified local address. |
| `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#DatagramSocket(java.net.SocketAddress)(bindaddr: https://developer.android.com/reference/kotlin/java/net/SocketAddress!)` Creates a datagram socket, bound to the specified local socket address. |

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#DatagramSocket(java.net.DatagramSocketImpl)(impl: https://developer.android.com/reference/kotlin/java/net/DatagramSocketImpl!)` Creates an unbound datagram socket with the specified DatagramSocketImpl. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#bind(java.net.SocketAddress)(addr: https://developer.android.com/reference/kotlin/java/net/SocketAddress!)` Binds this DatagramSocket to a specific address and port. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#close()()` Closes this datagram socket. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#connect(java.net.InetAddress,%20kotlin.Int)(address: https://developer.android.com/reference/kotlin/java/net/InetAddress!, port: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Connects the socket to a remote address for this socket. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#connect(java.net.SocketAddress)(addr: https://developer.android.com/reference/kotlin/java/net/SocketAddress!)` Connects this socket to a remote socket address (IP address + port number). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#disconnect()()` Disconnects the socket. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getBroadcast()()` Tests if SO_BROADCAST is enabled. |
| --- | --- |
| open [DatagramChannel](../java.nio.channels/DatagramChannel.md)! | `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getChannel()()` Returns the unique `https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel.html#` object associated with this datagram socket, if any. |
| open [InetAddress](InetAddress.md)! | `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getInetAddress()()` Returns the address to which this socket is connected. |
| open [InetAddress](InetAddress.md)! | `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getLocalAddress()()` Gets the local address to which the socket is bound. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getLocalPort()()` Returns the port number on the local host to which this socket is bound. |
| open [SocketAddress](SocketAddress.md)! | `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getLocalSocketAddress()()` Returns the address of the endpoint this socket is bound to. |
| open T | `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getOption(java.net.SocketOption)(name: https://developer.android.com/reference/kotlin/java/net/SocketOption<T>!)` Returns the value of a socket option. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getPort()()` Returns the port number to which this socket is connected. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getReceiveBufferSize()()` Get value of the SO_RCVBUF option for this `DatagramSocket`, that is the buffer size used by the platform for input on this `DatagramSocket`. |
| open [SocketAddress](SocketAddress.md)! | `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getRemoteSocketAddress()()` Returns the address of the endpoint this socket is connected to, or `null` if it is unconnected. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getReuseAddress()()` Tests if SO_REUSEADDR is enabled. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getSendBufferSize()()` Get value of the SO_SNDBUF option for this `DatagramSocket`, that is the buffer size used by the platform for output on this `DatagramSocket`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getSoTimeout()()` Retrieve setting for SO_TIMEOUT. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getTrafficClass()()` Gets traffic class or type-of-service in the IP datagram header for packets sent from this DatagramSocket. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#isBound()()` Returns the binding state of the socket. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#isClosed()()` Returns whether the socket is closed or not. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#isConnected()()` Returns the connection state of the socket. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#receive(java.net.DatagramPacket)(p: https://developer.android.com/reference/kotlin/java/net/DatagramPacket!)` Receives a datagram packet from this socket. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#send(java.net.DatagramPacket)(p: https://developer.android.com/reference/kotlin/java/net/DatagramPacket!)` Sends a datagram packet from this socket. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#setBroadcast(kotlin.Boolean)(on: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Enable/disable SO_BROADCAST. |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#setDatagramSocketImplFactory(java.net.DatagramSocketImplFactory)(fac: https://developer.android.com/reference/kotlin/java/net/DatagramSocketImplFactory!)` Sets the datagram socket implementation factory for the application. |
| open [DatagramSocket](DatagramSocket.md)! | `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#setOption(java.net.SocketOption,%20java.net.DatagramSocket.setOption.T)(name: https://developer.android.com/reference/kotlin/java/net/SocketOption<T>!, value: T)` Sets the value of a socket option. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#setReceiveBufferSize(kotlin.Int)(size: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the SO_RCVBUF option to the specified value for this `DatagramSocket`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#setReuseAddress(kotlin.Boolean)(on: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Enable/disable the SO_REUSEADDR socket option. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#setSendBufferSize(kotlin.Int)(size: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the SO_SNDBUF option to the specified value for this `DatagramSocket`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#setSoTimeout(kotlin.Int)(timeout: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Enable/disable SO_TIMEOUT with the specified timeout, in milliseconds. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#setTrafficClass(kotlin.Int)(tc: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets traffic class or type-of-service octet in the IP datagram header for datagrams sent from this DatagramSocket. |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [SocketOption](SocketOption.md)\<\*\>!\>! | `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#supportedOptions()()` Returns a set of the socket options supported by this socket. |
| --- | --- |

## Public constructors

### DatagramSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
DatagramSocket()
```

Constructs a datagram socket and binds it to any available port on the local host machine. The socket will be bound to the `https://developer.android.com/reference/kotlin/java/net/InetAddress#isAnyLocalAddress()` address, an IP address chosen by the kernel.

If there is a security manager, its `checkListen` method is first called with 0 as its argument to ensure the operation is allowed. This could result in a SecurityException.

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if a security manager exists and its `checkListen` method doesn't allow the operation. |
| `java.net.SocketException` | if the socket could not be opened, or the socket could not bind to the specified local port. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkListen(kotlin.Int)`

### DatagramSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
DatagramSocket(port: Int)
```

Constructs a datagram socket and binds it to the specified port on the local host machine. The socket will be bound to the `https://developer.android.com/reference/kotlin/java/net/InetAddress#isAnyLocalAddress()` address, an IP address chosen by the kernel.

If there is a security manager, its `checkListen` method is first called with the `port` argument as its argument to ensure the operation is allowed. This could result in a SecurityException.

| Parameters ||
|---|---|
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): port to use. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if a security manager exists and its `checkListen` method doesn't allow the operation. |
| `java.net.SocketException` | if the socket could not be opened, or the socket could not bind to the specified local port. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkListen(kotlin.Int)`

### DatagramSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
DatagramSocket(
    port: Int, 
    laddr: InetAddress!)
```

Creates a datagram socket, bound to the specified local address. The local port must be between 0 and 65535 inclusive. If the IP address is 0.0.0.0, the socket will be bound to the `https://developer.android.com/reference/kotlin/java/net/InetAddress#isAnyLocalAddress()` address, an IP address chosen by the kernel.

If there is a security manager, its `checkListen` method is first called with the `port` argument as its argument to ensure the operation is allowed. This could result in a SecurityException.

| Parameters ||
|---|---|
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): local port to use |
| `laddr` | [InetAddress](InetAddress.md)!: local address to bind |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if a security manager exists and its `checkListen` method doesn't allow the operation. |
| `java.net.SocketException` | if the socket could not be opened, or the socket could not bind to the specified local port. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkListen(kotlin.Int)`

### DatagramSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
DatagramSocket(bindaddr: SocketAddress!)
```

Creates a datagram socket, bound to the specified local socket address.

If, if the address is `null`, creates an unbound socket.

If there is a security manager, its `checkListen` method is first called with the port from the socket address as its argument to ensure the operation is allowed. This could result in a SecurityException.

| Parameters ||
|---|---|
| `bindaddr` | [SocketAddress](SocketAddress.md)!: local socket address to bind, or `null` for an unbound socket. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if a security manager exists and its `checkListen` method doesn't allow the operation. |
| `java.net.SocketException` | if the socket could not be opened, or the socket could not bind to the specified local port. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkListen(kotlin.Int)`

## Protected constructors

### DatagramSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected DatagramSocket(impl: DatagramSocketImpl!)
```

Creates an unbound datagram socket with the specified DatagramSocketImpl.

| Parameters ||
|---|---|
| `impl` | [DatagramSocketImpl](DatagramSocketImpl.md)!: an instance of a **DatagramSocketImpl** the subclass wishes to use on the DatagramSocket. |

## Public methods

### bind

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun bind(addr: SocketAddress!): Unit
```

Binds this DatagramSocket to a specific address and port.

If the address is `null`, then the system will pick up an ephemeral port and a valid local address to bind the socket.

| Parameters ||
|---|---|
| `addr` | [SocketAddress](SocketAddress.md)!: The address and port to bind to. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if addr is a SocketAddress subclass not supported by this socket. |
| `java.lang.SecurityException` | if a security manager exists and its `checkListen` method doesn't allow the operation. |
| `java.net.SocketException` | if any error happens during the bind, or if the socket is already bound. |
| --- | --- |

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun close(): Unit
```

Closes this datagram socket.

Any thread currently blocked in `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#receive(java.net.DatagramPacket)` upon this socket will throw a `https://developer.android.com/reference/kotlin/java/net/SocketException`.

If this socket has an associated channel then the channel is closed as well.

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs |

### connect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun connect(
    address: InetAddress!, 
    port: Int
): Unit
```

Connects the socket to a remote address for this socket. When a socket is connected to a remote address, packets may only be sent to or received from that address. By default a datagram socket is not connected.

If the remote destination to which the socket is connected does not exist, or is otherwise unreachable, and if an ICMP destination unreachable packet has been received for that address, then a subsequent call to send or receive may throw a PortUnreachableException. Note, there is no guarantee that the exception will be thrown.

If a security manager has been installed then it is invoked to check access to the remote address. Specifically, if the given `address` is a `https://developer.android.com/reference/kotlin/java/net/InetAddress#isMulticastAddress()`, the security manager's `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkMulticast(java.net.InetAddress)` method is invoked with the given `address`. Otherwise, the security manager's `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkConnect(kotlin.String,%20kotlin.Int)` and `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkAccept(kotlin.String,%20kotlin.Int)` methods are invoked, with the given `address` and `port`, to verify that datagrams are permitted to be sent and received respectively.

When a socket is connected, `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#receive(java.net.DatagramPacket)` and `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#send(java.net.DatagramPacket)` **will not perform any security checks** on incoming and outgoing packets, other than matching the packet's and the socket's address and port. On a send operation, if the packet's address is set and the packet's address and the socket's address do not match, an `IllegalArgumentException` will be thrown. A socket connected to a multicast address may only be used to send packets.

| Parameters ||
|---|---|
| `address` | [InetAddress](InetAddress.md)!: the remote address for the socket |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the remote port for the socket. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the address is null, or the port is out of range. |
| `java.lang.SecurityException` | if a security manager has been installed and it does not permit access to the given remote address |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#disconnect()`

### connect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun connect(addr: SocketAddress!): Unit
```

Connects this socket to a remote socket address (IP address + port number).

If given an `https://developer.android.com/reference/kotlin/java/net/InetSocketAddress`, this method behaves as if invoking `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#connect(java.net.InetAddress,%20kotlin.Int)` with the given socket addresses IP address and port number.

| Parameters ||
|---|---|
| `addr` | [SocketAddress](SocketAddress.md)!: The remote address. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `addr` is `null`, or `addr` is a SocketAddress subclass not supported by this socket |
| `java.lang.SecurityException` | if a security manager has been installed and it does not permit access to the given remote address |
| `java.net.SocketException` | if the connect fails |
| --- | --- |

### disconnect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun disconnect(): Unit
```

Disconnects the socket. If the socket is closed or not connected, then this method has no effect.
**See Also**

### getBroadcast

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBroadcast(): Boolean
```

Tests if SO_BROADCAST is enabled.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | a `boolean` indicating whether or not SO_BROADCAST is enabled. |

| Exceptions ||
|---|---|
| `java.net.SocketException` | if there is an error in the underlying protocol, such as an UDP error. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#setBroadcast(kotlin.Boolean)`

### getChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getChannel(): DatagramChannel!
```

Returns the unique `https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel.html#` object associated with this datagram socket, if any.

A datagram socket will have a channel if, and only if, the channel itself was created via the java.nio.channels.DatagramChannel#open method.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel.html#!` | the datagram channel associated with this datagram socket, or `null` if this socket was not created for a channel |

### getInetAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInetAddress(): InetAddress!
```

Returns the address to which this socket is connected. Returns `null` if the socket is not connected.

If the socket was connected prior to being #close, then this method will continue to return the connected address after the socket is closed.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/net/InetAddress!` | the address to which this socket is connected. |

### getLocalAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLocalAddress(): InetAddress!
```

Gets the local address to which the socket is bound.

If there is a security manager, its `checkConnect` method is first called with the host address and `-1` as its arguments to see if the operation is allowed.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/net/InetAddress!` | the local address to which the socket is bound, `null` if the socket is closed, or an `InetAddress` representing `https://developer.android.com/reference/kotlin/java/net/InetAddress#isAnyLocalAddress()` address if either the socket is not bound, or the security manager `checkConnect` method does not allow the operation |

**See Also**

### getLocalPort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLocalPort(): Int
```

Returns the port number on the local host to which this socket is bound.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the port number on the local host to which this socket is bound, `-1` if the socket is closed, or `0` if it is not bound yet. |

### getLocalSocketAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLocalSocketAddress(): SocketAddress!
```

Returns the address of the endpoint this socket is bound to.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/net/SocketAddress!` | a `SocketAddress` representing the local endpoint of this socket, or `null` if it is closed or not bound yet. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getLocalAddress()`
- `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getLocalPort()`
- `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#bind(java.net.SocketAddress)`

### getOption

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <T : Any!> getOption(name: SocketOption<T>!): T
```

Returns the value of a socket option.

| Parameters ||
|---|---|
| `<T>` | The type of the socket option value |
| `name` | [SocketOption](SocketOption.md)\<T\>!: The socket option |

| Return ||
|---|---|
| `T` | The value of the socket option. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs, or if the socket is closed. |
| `java.lang.NullPointerException` | if name is `null` |
| `java.lang.SecurityException` | if a security manager is set and if the socket option requires a security permission and if the caller does not have the required permission. `https://developer.android.com/reference/kotlin/java/net/StandardSocketOptions` do not require any security permission. |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the datagram socket does not support the option. |

### getPort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPort(): Int
```

Returns the port number to which this socket is connected. Returns `-1` if the socket is not connected.

If the socket was connected prior to being #close, then this method will continue to return the connected port number after the socket is closed.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the port number to which this socket is connected. |

### getReceiveBufferSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getReceiveBufferSize(): Int
```

Get value of the SO_RCVBUF option for this `DatagramSocket`, that is the buffer size used by the platform for input on this `DatagramSocket`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value of the SO_RCVBUF option for this `DatagramSocket` |

| Exceptions ||
|---|---|
| `java.net.SocketException` | if there is an error in the underlying protocol, such as an UDP error. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#setReceiveBufferSize(kotlin.Int)`

### getRemoteSocketAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRemoteSocketAddress(): SocketAddress!
```

Returns the address of the endpoint this socket is connected to, or `null` if it is unconnected.

If the socket was connected prior to being #close, then this method will continue to return the connected address after the socket is closed.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/net/SocketAddress!` | a `SocketAddress` representing the remote endpoint of this socket, or `null` if it is not connected yet. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getInetAddress()`
- `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getPort()`
- `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#connect(java.net.SocketAddress)`

### getReuseAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getReuseAddress(): Boolean
```

Tests if SO_REUSEADDR is enabled.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | a `boolean` indicating whether or not SO_REUSEADDR is enabled. |

| Exceptions ||
|---|---|
| `java.net.SocketException` | if there is an error in the underlying protocol, such as an UDP error. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#setReuseAddress(kotlin.Boolean)`

### getSendBufferSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSendBufferSize(): Int
```

Get value of the SO_SNDBUF option for this `DatagramSocket`, that is the buffer size used by the platform for output on this `DatagramSocket`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value of the SO_SNDBUF option for this `DatagramSocket` |

| Exceptions ||
|---|---|
| `java.net.SocketException` | if there is an error in the underlying protocol, such as an UDP error. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#setSendBufferSize(kotlin.Int)`

### getSoTimeout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSoTimeout(): Int
```

Retrieve setting for SO_TIMEOUT. 0 returns implies that the option is disabled (i.e., timeout of infinity).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the setting for SO_TIMEOUT |

| Exceptions ||
|---|---|
| `java.net.SocketException` | if there is an error in the underlying protocol, such as an UDP error. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#setSoTimeout(kotlin.Int)`

### getTrafficClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTrafficClass(): Int
```

Gets traffic class or type-of-service in the IP datagram header for packets sent from this DatagramSocket.

As the underlying network implementation may ignore the traffic class or type-of-service set using `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#setTrafficClass(kotlin.Int)` this method may return a different value than was previously set using the `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#setTrafficClass(kotlin.Int)` method on this DatagramSocket.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the traffic class or type-of-service already set |

| Exceptions ||
|---|---|
| `java.net.SocketException` | if there is an error obtaining the traffic class or type-of-service value. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#setTrafficClass(kotlin.Int)`

### isBound

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isBound(): Boolean
```

Returns the binding state of the socket.

If the socket was bound prior to being #close, then this method will continue to return `true` after the socket is closed.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the socket successfully bound to an address |

### isClosed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isClosed(): Boolean
```

Returns whether the socket is closed or not.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the socket has been closed |

### isConnected

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isConnected(): Boolean
```

Returns the connection state of the socket.

If the socket was connected prior to being #close, then this method will continue to return `true` after the socket is closed.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the socket successfully connected to a server |

### receive

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun receive(p: DatagramPacket!): Unit
```

Receives a datagram packet from this socket. When this method returns, the `DatagramPacket`'s buffer is filled with the data received. The datagram packet also contains the sender's IP address, and the port number on the sender's machine.

This method blocks until a datagram is received. The `length` field of the datagram packet object contains the length of the received message. If the message is longer than the packet's length, the message is truncated.

If there is a security manager, a packet cannot be received if the security manager's `checkAccept` method does not allow it.

| Parameters ||
|---|---|
| `p` | [DatagramPacket](DatagramPacket.md)!: the `DatagramPacket` into which to place the incoming data. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |
| `java.net.PortUnreachableException` | may be thrown if the socket is connected to a currently unreachable destination. Note, there is no guarantee that the exception will be thrown. |
| `java.net.SocketTimeoutException` | if setSoTimeout was previously called and the timeout has expired. |
| --- | --- |
| `java.nio.channels.IllegalBlockingModeException` | if this socket has an associated channel, and the channel is in non-blocking mode. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/DatagramPacket`
- `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#`

### send

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun send(p: DatagramPacket!): Unit
```

Sends a datagram packet from this socket. The `DatagramPacket` includes information indicating the data to be sent, its length, the IP address of the remote host, and the port number on the remote host.

If there is a security manager, and the socket is not currently connected to a remote address, this method first performs some security checks. First, if `p.getAddress().isMulticastAddress()` is true, this method calls the security manager's `checkMulticast` method with `p.getAddress()` as its argument. If the evaluation of that expression is false, this method instead calls the security manager's `checkConnect` method with arguments `p.getAddress().getHostAddress()` and `p.getPort()`. Each call to a security manager method could result in a SecurityException if the operation is not allowed.

| Parameters ||
|---|---|
| `p` | [DatagramPacket](DatagramPacket.md)!: the `DatagramPacket` to be sent. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |
| `java.lang.IllegalArgumentException` | if the socket is connected, and connected address and packet address differ. |
| `java.lang.SecurityException` | if a security manager exists and its `checkMulticast` or `checkConnect` method doesn't allow the send. |
| --- | --- |
| `java.net.PortUnreachableException` | may be thrown if the socket is connected to a currently unreachable destination. Note, there is no guarantee that the exception will be thrown. |
| `java.nio.channels.IllegalBlockingModeException` | if this socket has an associated channel, and the channel is in non-blocking mode. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/DatagramPacket`
- `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkMulticast(java.net.InetAddress)`

### setBroadcast

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setBroadcast(on: Boolean): Unit
```

Enable/disable SO_BROADCAST.

Some operating systems may require that the Java virtual machine be started with implementation specific privileges to enable this option or send broadcast datagrams.

| Parameters ||
|---|---|
| `on` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether or not to have broadcast turned on. |

| Exceptions ||
|---|---|
| `java.net.SocketException` | if there is an error in the underlying protocol, such as an UDP error. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getBroadcast()`

### setDatagramSocketImplFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun setDatagramSocketImplFactory(fac: DatagramSocketImplFactory!): Unit
```

Sets the datagram socket implementation factory for the application. The factory can be specified only once.

When an application creates a new datagram socket, the socket implementation factory's `createDatagramSocketImpl` method is called to create the actual datagram socket implementation.

Passing `null` to the method is a no-op unless the factory was already set.

If there is a security manager, this method first calls the security manager's `checkSetFactory` method to ensure the operation is allowed. This could result in a SecurityException.

| Parameters ||
|---|---|
| `fac` | [DatagramSocketImplFactory](DatagramSocketImplFactory.md)!: the desired factory. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs when setting the datagram socket factory. |
| `java.lang.SecurityException` | if a security manager exists and its `checkSetFactory` method doesn't allow the operation. |
| `java.net.SocketException` | if the factory is already defined. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/DatagramSocketImplFactory#createDatagramSocketImpl()`
- `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkSetFactory()`

### setOption

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <T : Any!> setOption(
    name: SocketOption<T>!, 
    value: T
): DatagramSocket!
```

Sets the value of a socket option.

| Parameters ||
|---|---|
| `<T>` | The type of the socket option value |
| `name` | [SocketOption](SocketOption.md)\<T\>!: The socket option |
| `value` | T: The value of the socket option. A value of `null` may be valid for some options. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#!` | this DatagramSocket |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs, or if the socket is closed. |
| `java.lang.IllegalArgumentException` | if the value is not valid for the option. |
| `java.lang.NullPointerException` | if name is `null` |
| --- | --- |
| `java.lang.SecurityException` | if a security manager is set and if the socket option requires a security permission and if the caller does not have the required permission. `https://developer.android.com/reference/kotlin/java/net/StandardSocketOptions` do not require any security permission. |
| `java.lang.UnsupportedOperationException` | if the datagram socket does not support the option. |

### setReceiveBufferSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setReceiveBufferSize(size: Int): Unit
```

Sets the SO_RCVBUF option to the specified value for this `DatagramSocket`. The SO_RCVBUF option is used by the network implementation as a hint to size the underlying network I/O buffers. The SO_RCVBUF setting may also be used by the network implementation to determine the maximum size of the packet that can be received on this socket.

Because SO_RCVBUF is a hint, applications that want to verify what size the buffers were set to should call `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getReceiveBufferSize()`.

Increasing SO_RCVBUF may allow the network implementation to buffer multiple packets when packets arrive faster than are being received using `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#receive(java.net.DatagramPacket)`.

Note: It is implementation specific if a packet larger than SO_RCVBUF can be received.

| Parameters ||
|---|---|
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the size to which to set the receive buffer size. This value must be greater than 0. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the value is 0 or is negative. |
| `java.net.SocketException` | if there is an error in the underlying protocol, such as an UDP error. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getReceiveBufferSize()`

### setReuseAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setReuseAddress(on: Boolean): Unit
```

Enable/disable the SO_REUSEADDR socket option.

For UDP sockets it may be necessary to bind more than one socket to the same socket address. This is typically for the purpose of receiving multicast packets (See `https://developer.android.com/reference/kotlin/java/net/MulticastSocket`). The `SO_REUSEADDR` socket option allows multiple sockets to be bound to the same socket address if the `SO_REUSEADDR` socket option is enabled prior to binding the socket using `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#bind(java.net.SocketAddress)`.

Note: This functionality is not supported by all existing platforms, so it is implementation specific whether this option will be ignored or not. However, if it is not supported then `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getReuseAddress()` will always return `false`.

When a `DatagramSocket` is created the initial setting of `SO_REUSEADDR` is disabled.

The behaviour when `SO_REUSEADDR` is enabled or disabled after a socket is bound (See `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#isBound()`) is not defined.

| Parameters ||
|---|---|
| `on` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether to enable or disable the |

| Exceptions ||
|---|---|
| `java.net.SocketException` | if an error occurs enabling or disabling the `SO_RESUEADDR` socket option, or the socket is closed. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getReuseAddress()`
- `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#bind(java.net.SocketAddress)`
- `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#isBound()`
- `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#isClosed()`

### setSendBufferSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSendBufferSize(size: Int): Unit
```

Sets the SO_SNDBUF option to the specified value for this `DatagramSocket`. The SO_SNDBUF option is used by the network implementation as a hint to size the underlying network I/O buffers. The SO_SNDBUF setting may also be used by the network implementation to determine the maximum size of the packet that can be sent on this socket.

As SO_SNDBUF is a hint, applications that want to verify what size the buffer is should call `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getSendBufferSize()`.

Increasing the buffer size may allow multiple outgoing packets to be queued by the network implementation when the send rate is high.

Note: If `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#send(java.net.DatagramPacket)` is used to send a `DatagramPacket` that is larger than the setting of SO_SNDBUF then it is implementation specific if the packet is sent or discarded.

| Parameters ||
|---|---|
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the size to which to set the send buffer size. This value must be greater than 0. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the value is 0 or is negative. |
| `java.net.SocketException` | if there is an error in the underlying protocol, such as an UDP error. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getSendBufferSize()`

### setSoTimeout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSoTimeout(timeout: Int): Unit
```

Enable/disable SO_TIMEOUT with the specified timeout, in milliseconds. With this option set to a non-zero timeout, a call to receive() for this DatagramSocket will block for only this amount of time. If the timeout expires, a **java.net.SocketTimeoutException** is raised, though the DatagramSocket is still valid. The option **must** be enabled prior to entering the blocking operation to have effect. The timeout must be `> 0`. A timeout of zero is interpreted as an infinite timeout.

| Parameters ||
|---|---|
| `timeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the specified timeout in milliseconds. |

| Exceptions ||
|---|---|
| `java.net.SocketException` | if there is an error in the underlying protocol, such as an UDP error. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getSoTimeout()`

### setTrafficClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTrafficClass(tc: Int): Unit
```

Sets traffic class or type-of-service octet in the IP datagram header for datagrams sent from this DatagramSocket. As the underlying network implementation may ignore this value applications should consider it a hint.

The tc **must** be in the range `0 <= tc <= 255` or an IllegalArgumentException will be thrown.

Notes:

For Internet Protocol v4 the value consists of an `integer`, the least significant 8 bits of which represent the value of the TOS octet in IP packets sent by the socket. RFC 1349 defines the TOS values as follows:

- `IPTOS_LOWCOST (0x02)`
- `IPTOS_RELIABILITY (0x04)`
- `IPTOS_THROUGHPUT (0x08)`
- `IPTOS_LOWDELAY (0x10)`

The last low order bit is always ignored as this corresponds to the MBZ (must be zero) bit.

Setting bits in the precedence field may result in a SocketException indicating that the operation is not permitted.

for Internet Protocol v6 `tc` is the value that would be placed into the sin6_flowinfo field of the IP header.

| Parameters ||
|---|---|
| `tc` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): an `int` value for the bitset. |

| Exceptions ||
|---|---|
| `java.net.SocketException` | if there is an error setting the traffic class or type-of-service |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getTrafficClass()`

### supportedOptions

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun supportedOptions(): MutableSet<SocketOption<*>!>!
```

Returns a set of the socket options supported by this socket. This method will continue to return the set of options even after the socket has been closed.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/java/net/SocketOption<*>!>!` | A set of the socket options supported by this socket. This set may be empty if the socket's DatagramSocketImpl cannot be created. |
