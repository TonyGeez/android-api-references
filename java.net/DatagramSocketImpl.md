Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DatagramSocketImpl

```
abstract class DatagramSocketImpl : SocketOptions
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.net.DatagramSocketImpl](DatagramSocketImpl.md) |

Abstract datagram and multicast socket implementation base class.

## Summary

| Inherited constants ||
|---|---|
| From class SocketOptions |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#IP_MULTICAST_IF:kotlin.Int` Set which outgoing interface on which to send multicast packets. Useful on hosts with multiple network interfaces, where applications want to use other than the system default. Takes/returns an InetAddress. Valid for Multicast: DatagramSocketImpl <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#IP_MULTICAST_IF2:kotlin.Int` Same as above. This option is introduced so that the behaviour with IP_MULTICAST_IF will be kept the same as before, while this new option can support setting outgoing interfaces with either IPv4 and IPv6 addresses. NOTE: make sure there is no conflict with this <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#IP_MULTICAST_LOOP:kotlin.Int` This option enables or disables local loopback of multicast datagrams. This option is enabled by default for Multicast Sockets. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#IP_TOS:kotlin.Int` This option sets the type-of-service or traffic class field in the IP header for a TCP or UDP socket. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#SO_BINDADDR:kotlin.Int` Fetch the local address binding of a socket (this option cannot be "set" only "gotten", since sockets are bound at creation time, and so the locally bound address cannot be changed). The default local address of a socket is INADDR_ANY, meaning any local address on a multi-homed host. A multi-homed host can use this option to accept connections to only one of its addresses (in the case of a ServerSocket or DatagramSocket), or to specify its return address to the peer (for a Socket or DatagramSocket). The parameter of this option is an InetAddress. This option **must** be specified in the constructor. Valid for: SocketImpl, DatagramSocketImpl <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#SO_BROADCAST:kotlin.Int` Sets SO_BROADCAST for a socket. This option enables and disables the ability of the process to send broadcast messages. It is supported for only datagram sockets and only on networks that support the concept of a broadcast message (e.g. Ethernet, token ring, etc.), and it is set by default for DatagramSockets. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#SO_KEEPALIVE:kotlin.Int` When the keepalive option is set for a TCP socket and no data has been exchanged across the socket in either direction for 2 hours (NOTE: the actual value is implementation dependent), TCP automatically sends a keepalive probe to the peer. This probe is a TCP segment to which the peer must respond. One of three responses is expected: 1. The peer responds with the expected ACK. The application is not notified (since everything is OK). TCP will send another probe following another 2 hours of inactivity. 2. The peer responds with an RST, which tells the local TCP that the peer host has crashed and rebooted. The socket is closed. 3. There is no response from the peer. The socket is closed. The purpose of this option is to detect if the peer host crashes. Valid only for TCP socket: SocketImpl <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#SO_LINGER:kotlin.Int` Specify a linger-on-close timeout. This option disables/enables immediate return from a **close()** of a TCP Socket. Enabling this option with a non-zero Integer *timeout* means that a **close()** will block pending the transmission and acknowledgement of all data written to the peer, at which point the socket is closed *gracefully* . Upon reaching the linger timeout, the socket is closed *forcefully*, with a TCP RST. Enabling the option with a timeout of zero does a forceful close immediately. If the specified timeout value exceeds 65,535 it will be reduced to 65,535. Valid only for TCP: SocketImpl <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#SO_OOBINLINE:kotlin.Int` When the OOBINLINE option is set, any TCP urgent data received on the socket will be received through the socket input stream. When the option is disabled (which is the default) urgent data is silently discarded. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#SO_RCVBUF:kotlin.Int` Set a hint the size of the underlying buffers used by the platform for incoming network I/O. When used in set, this is a suggestion to the kernel from the application about the size of buffers to use for the data to be received over the socket. When used in get, this must return the size of the buffer actually used by the platform when receiving in data on this socket. Valid for all sockets: SocketImpl, DatagramSocketImpl <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#SO_REUSEADDR:kotlin.Int` Sets SO_REUSEADDR for a socket. This is used only for MulticastSockets in java, and it is set by default for MulticastSockets. Valid for: DatagramSocketImpl <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#SO_REUSEPORT:kotlin.Int` Sets SO_REUSEPORT for a socket. This option enables and disables the ability to have multiple sockets listen to the same address and port. Valid for: SocketImpl, DatagramSocketImpl <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#SO_SNDBUF:kotlin.Int` Set a hint the size of the underlying buffers used by the platform for outgoing network I/O. When used in set, this is a suggestion to the kernel from the application about the size of buffers to use for the data to be sent over the socket. When used in get, this must return the size of the buffer actually used by the platform when sending out data on this socket. Valid for all sockets: SocketImpl, DatagramSocketImpl <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#SO_TIMEOUT:kotlin.Int` Set a timeout on blocking Socket operations: ```kotlin ServerSocket.accept(); SocketInputStream.read(); DatagramSocket.receive(); ``` <br /> The option must be set prior to entering a blocking operation to take effect. If the timeout expires and the operation would continue to block, **java.io.InterruptedIOException** is raised. The Socket is not closed in this case. Valid for all sockets: SocketImpl, DatagramSocketImpl <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#TCP_NODELAY:kotlin.Int` Disable Nagle's algorithm for this connection. Written data to the network is not buffered pending acknowledgement of previously written data. Valid for TCP only: SocketImpl. <br /> | ||

| Public constructors ||
|---|---|
| DatagramSocketImpl <br /> |

| Protected methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | bind Binds a datagram socket to a local port and address. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | close Close the socket. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | connect Connects a datagram socket to a remote destination. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | create Creates a datagram socket. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | disconnect Disconnects a datagram socket from its remote destination. |
| open [FileDescriptor](../java.io/FileDescriptor.md)! | getFileDescriptor Gets the datagram socket file descriptor. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getLocalPort Gets the local port. |
| open T | getOption Called to get a socket option. |
| abstract [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | getTTL Retrieve the TTL (time-to-live) option. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getTimeToLive Retrieve the TTL (time-to-live) option. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | join Join the multicast group. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | joinGroup Join the multicast group. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | leave Leave the multicast group. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | leaveGroup Leave the multicast group. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | peek Peek at the packet to see who it is from. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | peekData Peek at the packet to see who it is from. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | receive Receive the datagram packet. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | send Sends a datagram packet. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOption Called to set a socket option. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setTTL Set the TTL (time-to-live) option. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setTimeToLive Set the TTL (time-to-live) option. |
| --- | --- |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [SocketOption](SocketOption.md)\<\*\>!\>! | supportedOptions Returns a set of SocketOptions supported by this impl and by this impl's socket (DatagramSocket or MulticastSocket) |

| Inherited functions ||
|---|---|
| From class SocketOptions |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | getOption Fetch the value of an option. Binary options will return java.lang.Boolean.TRUE if enabled, java.lang.Boolean.FALSE if disabled, e.g.: ```kotlin SocketImpl s; ... Boolean noDelay = (Boolean)(s.getOption(TCP_NODELAY)); if (noDelay.booleanValue()) { // true if TCP_NODELAY is enabled... ... } ``` <br /> For options that take a particular type as a parameter, getOption(int) will return the parameter's value, else it will return java.lang.Boolean.FALSE: ```kotlin Object o = s.getOption(SO_LINGER); if (o instanceof Integer) { System.out.print("Linger time is " + ((Integer)o).intValue()); } else { // the true type of o is java.lang.Boolean.FALSE; } ``` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setOption Enable/disable the option specified by *optID* . If the option is to be enabled, and it takes an option-specific "value", this is passed in *value* . The actual type of value is option-specific, and it is an error to pass something that isn't of the expected type: ```kotlin SocketImpl s; ... s.setOption(SO_LINGER, new Integer(10)); // OK - set SO_LINGER w/ timeout of 10 sec. s.setOption(SO_LINGER, new Double(10)); // ERROR - expects java.lang.Integer ``` If the requested option is binary, it can be set using this method by a java.lang.Boolean: ```kotlin s.setOption(TCP_NODELAY, Boolean.TRUE); // OK - enables TCP_NODELAY, a binary option ``` <br /> Any option can be disabled using this method with a Boolean.FALSE: ```kotlin s.setOption(TCP_NODELAY, Boolean.FALSE); // OK - disables TCP_NODELAY s.setOption(SO_LINGER, Boolean.FALSE); // OK - disables SO_LINGER ``` <br /> For an option that has a notion of on and off, and requires a non-boolean parameter, setting its value to anything other than *Boolean.FALSE* implicitly enables it. Throws SocketException if the option is unrecognized, the socket is closed, or some low-level error occurred <br /> <br /> | ||

| Properties ||
|---|---|
| [FileDescriptor](../java.io/FileDescriptor.md)! | `https://developer.android.com/reference/kotlin/java/net/DatagramSocketImpl#fd:java.io.FileDescriptor` The file descriptor object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/DatagramSocketImpl#localPort:kotlin.Int` The local port number. |

## Public constructors

### DatagramSocketImpl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
DatagramSocketImpl()
```

## Protected methods

### bind

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun bind(
    lport: Int, 
    laddr: InetAddress!
): Unit
```

Binds a datagram socket to a local port and address.

| Parameters ||
|---|---|
| `lport` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the local port |
| `laddr` | [InetAddress](InetAddress.md)!: the local address |

| Exceptions ||
|---|---|
| `java.net.SocketException` | if there is an error in the underlying protocol, such as a TCP error. |

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun close(): Unit
```

Close the socket.

### connect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun connect(
    address: InetAddress!, 
    port: Int
): Unit
```

Connects a datagram socket to a remote destination. This associates the remote address with the local socket so that datagrams may only be sent to this destination and received from this destination. This may be overridden to call a native system connect.

If the remote destination to which the socket is connected does not exist, or is otherwise unreachable, and if an ICMP destination unreachable packet has been received for that address, then a subsequent call to send or receive may throw a PortUnreachableException. Note, there is no guarantee that the exception will be thrown.

| Parameters ||
|---|---|
| `address` | [InetAddress](InetAddress.md)!: the remote InetAddress to connect to |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the remote port number |

| Exceptions ||
|---|---|
| `java.net.SocketException` | may be thrown if the socket cannot be connected to the remote destination |

### create

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun create(): Unit
```

Creates a datagram socket.

| Exceptions ||
|---|---|
| `java.net.SocketException` | if there is an error in the underlying protocol, such as a TCP error. |

### disconnect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun disconnect(): Unit
```

Disconnects a datagram socket from its remote destination.

### getFileDescriptor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun getFileDescriptor(): FileDescriptor!
```

Gets the datagram socket file descriptor.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!` | a `FileDescriptor` object representing the datagram socket file descriptor |

### getLocalPort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun getLocalPort(): Int
```

Gets the local port.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | an `int` representing the local port value |

### getOption

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun <T : Any!> getOption(name: SocketOption<T>!): T
```

Called to get a socket option.

| Parameters ||
|---|---|
| `<T>` | The type of the socket option value |
| `name` | [SocketOption](SocketOption.md)\<T\>!: The socket option |

| Return ||
|---|---|
| `T` | the socket option |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O problem occurs while attempting to set the option |
| `java.lang.NullPointerException` | if name is `null` |
| `java.lang.UnsupportedOperationException` | if the DatagramSocketImpl does not support the option |
| --- | --- |

### getTTL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun getTTL(): Byte
```

**Deprecated:** *use getTimeToLive instead.*

Retrieve the TTL (time-to-live) option.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html` | a byte representing the TTL value |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O exception occurs while retrieving the time-to-live option |

**See Also**

- setTTL

### getTimeToLive

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun getTimeToLive(): Int
```

Retrieve the TTL (time-to-live) option.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | an `int` representing the time-to-live value |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O exception occurs while retrieving the time-to-live option |

**See Also**

- setTimeToLive

### join

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun join(inetaddr: InetAddress!): Unit
```

Join the multicast group.

| Parameters ||
|---|---|
| `inetaddr` | [InetAddress](InetAddress.md)!: multicast address to join. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O exception occurs while joining the multicast group. |

### joinGroup

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun joinGroup(
    mcastaddr: SocketAddress!, 
    netIf: NetworkInterface!
): Unit
```

Join the multicast group.

| Parameters ||
|---|---|
| `mcastaddr` | [SocketAddress](SocketAddress.md)!: address to join. |
| `netIf` | [NetworkInterface](NetworkInterface.md)!: specifies the local interface to receive multicast datagram packets |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O exception occurs while joining the multicast group |

### leave

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun leave(inetaddr: InetAddress!): Unit
```

Leave the multicast group.

| Parameters ||
|---|---|
| `inetaddr` | [InetAddress](InetAddress.md)!: multicast address to leave. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O exception occurs while leaving the multicast group. |

### leaveGroup

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun leaveGroup(
    mcastaddr: SocketAddress!, 
    netIf: NetworkInterface!
): Unit
```

Leave the multicast group.

| Parameters ||
|---|---|
| `mcastaddr` | [SocketAddress](SocketAddress.md)!: address to leave. |
| `netIf` | [NetworkInterface](NetworkInterface.md)!: specified the local interface to leave the group at |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O exception occurs while leaving the multicast group |

### peek

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun peek(i: InetAddress!): Int
```

Peek at the packet to see who it is from. Updates the specified `InetAddress` to the address which the packet came from.

| Parameters ||
|---|---|
| `i` | [InetAddress](InetAddress.md)!: an InetAddress object |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the port number which the packet came from. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O exception occurs |
| `java.net.PortUnreachableException` | may be thrown if the socket is connected to a currently unreachable destination. Note, there is no guarantee that the exception will be thrown. |

### peekData

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun peekData(p: DatagramPacket!): Int
```

Peek at the packet to see who it is from. The data is copied into the specified `DatagramPacket`. The data is returned, but not consumed, so that a subsequent peekData/receive operation will see the same data.

| Parameters ||
|---|---|
| `p` | [DatagramPacket](DatagramPacket.md)!: the Packet Received. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the port number which the packet came from. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O exception occurs |
| `java.net.PortUnreachableException` | may be thrown if the socket is connected to a currently unreachable destination. Note, there is no guarantee that the exception will be thrown. |

### receive

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun receive(p: DatagramPacket!): Unit
```

Receive the datagram packet.

| Parameters ||
|---|---|
| `p` | [DatagramPacket](DatagramPacket.md)!: the Packet Received. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O exception occurs while receiving the datagram packet. |
| `java.net.PortUnreachableException` | may be thrown if the socket is connected to a currently unreachable destination. Note, there is no guarantee that the exception will be thrown. |

### send

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun send(p: DatagramPacket!): Unit
```

Sends a datagram packet. The packet contains the data and the destination address to send the packet to.

| Parameters ||
|---|---|
| `p` | [DatagramPacket](DatagramPacket.md)!: the packet to be sent. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O exception occurs while sending the datagram packet. |
| `java.net.PortUnreachableException` | may be thrown if the socket is connected to a currently unreachable destination. Note, there is no guarantee that the exception will be thrown. |

### setOption

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun <T : Any!> setOption(
    name: SocketOption<T>!, 
    value: T
): Unit
```

Called to set a socket option.

| Parameters ||
|---|---|
| `<T>` | The type of the socket option value |
| `name` | [SocketOption](SocketOption.md)\<T\>!: The socket option |
| `value` | T: The value of the socket option. A value of `null` may be valid for some options. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O problem occurs while attempting to set the option |
| `java.lang.NullPointerException` | if name is `null` |
| `java.lang.UnsupportedOperationException` | if the DatagramSocketImpl does not support the option |
| --- | --- |

### setTTL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun setTTL(ttl: Byte): Unit
```

**Deprecated:** *use setTimeToLive instead.*

Set the TTL (time-to-live) option.

| Parameters ||
|---|---|
| `ttl` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html): a byte specifying the TTL value |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O exception occurs while setting the time-to-live option. |

**See Also**

- getTTL

### setTimeToLive

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun setTimeToLive(ttl: Int): Unit
```

Set the TTL (time-to-live) option.

| Parameters ||
|---|---|
| `ttl` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): an `int` specifying the time-to-live value |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O exception occurs while setting the time-to-live option. |

**See Also**

- getTimeToLive

### supportedOptions

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun supportedOptions(): MutableSet<SocketOption<*>!>!
```

Returns a set of SocketOptions supported by this impl and by this impl's socket (DatagramSocket or MulticastSocket)

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/java/net/SocketOption<*>!>!` | a Set of SocketOptions |

## Properties

### fd

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected var fd: FileDescriptor!
```

The file descriptor object.

### localPort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected var localPort: Int
```

The local port number.
