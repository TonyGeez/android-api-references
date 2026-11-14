Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SocketImpl

```
abstract class SocketImpl : SocketOptions
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.net.SocketImpl](../java/net/SocketImpl.md) |

The abstract class `SocketImpl` is a common superclass of all classes that actually implement sockets. It is used to create both client and server sockets.

A "plain" socket implements these methods exactly as described, without attempting to go through a firewall or proxy.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/net/SocketOptions` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#IP_MULTICAST_IF:kotlin.Int` Set which outgoing interface on which to send multicast packets. Useful on hosts with multiple network interfaces, where applications want to use other than the system default. Takes/returns an InetAddress. Valid for Multicast: DatagramSocketImpl <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#IP_MULTICAST_IF2:kotlin.Int` Same as above. This option is introduced so that the behaviour with IP_MULTICAST_IF will be kept the same as before, while this new option can support setting outgoing interfaces with either IPv4 and IPv6 addresses. NOTE: make sure there is no conflict with this <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#IP_MULTICAST_LOOP:kotlin.Int` This option enables or disables local loopback of multicast datagrams. This option is enabled by default for Multicast Sockets. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#IP_TOS:kotlin.Int` This option sets the type-of-service or traffic class field in the IP header for a TCP or UDP socket. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#SO_BINDADDR:kotlin.Int` Fetch the local address binding of a socket (this option cannot be "set" only "gotten", since sockets are bound at creation time, and so the locally bound address cannot be changed). The default local address of a socket is INADDR_ANY, meaning any local address on a multi-homed host. A multi-homed host can use this option to accept connections to only one of its addresses (in the case of a ServerSocket or DatagramSocket), or to specify its return address to the peer (for a Socket or DatagramSocket). The parameter of this option is an InetAddress. This option **must** be specified in the constructor. Valid for: SocketImpl, DatagramSocketImpl <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#SO_BROADCAST:kotlin.Int` Sets SO_BROADCAST for a socket. This option enables and disables the ability of the process to send broadcast messages. It is supported for only datagram sockets and only on networks that support the concept of a broadcast message (e.g. Ethernet, token ring, etc.), and it is set by default for DatagramSockets. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#SO_KEEPALIVE:kotlin.Int` When the keepalive option is set for a TCP socket and no data has been exchanged across the socket in either direction for 2 hours (NOTE: the actual value is implementation dependent), TCP automatically sends a keepalive probe to the peer. This probe is a TCP segment to which the peer must respond. One of three responses is expected: 1. The peer responds with the expected ACK. The application is not notified (since everything is OK). TCP will send another probe following another 2 hours of inactivity. 2. The peer responds with an RST, which tells the local TCP that the peer host has crashed and rebooted. The socket is closed. 3. There is no response from the peer. The socket is closed. The purpose of this option is to detect if the peer host crashes. Valid only for TCP socket: SocketImpl <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#SO_LINGER:kotlin.Int` Specify a linger-on-close timeout. This option disables/enables immediate return from a **close()** of a TCP Socket. Enabling this option with a non-zero Integer *timeout* means that a **close()** will block pending the transmission and acknowledgement of all data written to the peer, at which point the socket is closed *gracefully* . Upon reaching the linger timeout, the socket is closed *forcefully*, with a TCP RST. Enabling the option with a timeout of zero does a forceful close immediately. If the specified timeout value exceeds 65,535 it will be reduced to 65,535. Valid only for TCP: SocketImpl <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#SO_OOBINLINE:kotlin.Int` When the OOBINLINE option is set, any TCP urgent data received on the socket will be received through the socket input stream. When the option is disabled (which is the default) urgent data is silently discarded. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#SO_RCVBUF:kotlin.Int` Set a hint the size of the underlying buffers used by the platform for incoming network I/O. When used in set, this is a suggestion to the kernel from the application about the size of buffers to use for the data to be received over the socket. When used in get, this must return the size of the buffer actually used by the platform when receiving in data on this socket. Valid for all sockets: SocketImpl, DatagramSocketImpl <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#SO_REUSEADDR:kotlin.Int` Sets SO_REUSEADDR for a socket. This is used only for MulticastSockets in java, and it is set by default for MulticastSockets. Valid for: DatagramSocketImpl <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#SO_REUSEPORT:kotlin.Int` Sets SO_REUSEPORT for a socket. This option enables and disables the ability to have multiple sockets listen to the same address and port. Valid for: SocketImpl, DatagramSocketImpl <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#SO_SNDBUF:kotlin.Int` Set a hint the size of the underlying buffers used by the platform for outgoing network I/O. When used in set, this is a suggestion to the kernel from the application about the size of buffers to use for the data to be sent over the socket. When used in get, this must return the size of the buffer actually used by the platform when sending out data on this socket. Valid for all sockets: SocketImpl, DatagramSocketImpl <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#SO_TIMEOUT:kotlin.Int` Set a timeout on blocking Socket operations: ```kotlin ServerSocket.accept(); SocketInputStream.read(); DatagramSocket.receive(); ``` <br /> The option must be set prior to entering a blocking operation to take effect. If the timeout expires and the operation would continue to block, **java.io.InterruptedIOException** is raised. The Socket is not closed in this case. Valid for all sockets: SocketImpl, DatagramSocketImpl <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#TCP_NODELAY:kotlin.Int` Disable Nagle's algorithm for this connection. Written data to the network is not buffered pending acknowledgement of previously written data. Valid for TCP only: SocketImpl. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/net/SocketImpl#SocketImpl()()` <br /> |

| Public methods ||
|---|---|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/net/SocketImpl#toString()()` Returns the address and port of this socket as a `String`. |

| Protected methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/net/SocketImpl#accept(java.net.SocketImpl)(s: https://developer.android.com/reference/kotlin/java/net/SocketImpl#!)` Accepts a connection. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/SocketImpl#available()()` Returns the number of bytes that can be read from this socket without blocking. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/net/SocketImpl#bind(java.net.InetAddress,%20kotlin.Int)(host: https://developer.android.com/reference/kotlin/java/net/InetAddress!, port: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Binds this socket to the specified local IP address and port number. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/net/SocketImpl#close()()` Closes this socket. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/net/SocketImpl#connect(kotlin.String,%20kotlin.Int)(host: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, port: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Connects this socket to the specified port on the named host. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/net/SocketImpl#connect(java.net.InetAddress,%20kotlin.Int)(address: https://developer.android.com/reference/kotlin/java/net/InetAddress!, port: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Connects this socket to the specified port number on the specified host. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/net/SocketImpl#connect(java.net.SocketAddress,%20kotlin.Int)(address: https://developer.android.com/reference/kotlin/java/net/SocketAddress!, timeout: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Connects this socket to the specified port number on the specified host. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/net/SocketImpl#create(kotlin.Boolean)(stream: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Creates either a stream or a datagram socket. |
| open [FileDescriptor](../java/io/FileDescriptor.md)! | `https://developer.android.com/reference/kotlin/java/net/SocketImpl#getFileDescriptor()()` Returns the value of this socket's `fd` field. |
| --- | --- |
| open [InetAddress](../java/net/InetAddress.md)! | `https://developer.android.com/reference/kotlin/java/net/SocketImpl#getInetAddress()()` Returns the value of this socket's `address` field. |
| abstract [InputStream](../java/io/InputStream.md)! | `https://developer.android.com/reference/kotlin/java/net/SocketImpl#getInputStream()()` Returns an input stream for this socket. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/SocketImpl#getLocalPort()()` Returns the value of this socket's `localport` field. |
| --- | --- |
| open T | `https://developer.android.com/reference/kotlin/java/net/SocketImpl#getOption(java.net.SocketOption)(name: https://developer.android.com/reference/kotlin/java/net/SocketOption<T>!)` Called to get a socket option. |
| abstract [OutputStream](../java/io/OutputStream.md)! | `https://developer.android.com/reference/kotlin/java/net/SocketImpl#getOutputStream()()` Returns an output stream for this socket. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/SocketImpl#getPort()()` Returns the value of this socket's `port` field. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/net/SocketImpl#listen(kotlin.Int)(backlog: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the maximum queue length for incoming connection indications (a request to connect) to the `count` argument. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/net/SocketImpl#sendUrgentData(kotlin.Int)(data: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Send one byte of urgent data on the socket. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/net/SocketImpl#setOption(java.net.SocketOption,%20java.net.SocketImpl.setOption.T)(name: https://developer.android.com/reference/kotlin/java/net/SocketOption<T>!, value: T)` Called to set a socket option. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/net/SocketImpl#setPerformancePreferences(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(connectionTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, latency: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bandwidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets performance preferences for this socket. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/net/SocketImpl#shutdownInput()()` Places the input stream for this socket at "end of stream". |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/net/SocketImpl#shutdownOutput()()` Disables the output stream for this socket. |
| --- | --- |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [SocketOption](../java/net/SocketOption.md)\<\*\>!\>! | `https://developer.android.com/reference/kotlin/java/net/SocketImpl#supportedOptions()()` Returns a set of SocketOptions supported by this impl and by this impl's socket (Socket or ServerSocket) |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/net/SocketImpl#supportsUrgentData()()` Returns whether or not this SocketImpl supports sending urgent data. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/net/SocketOptions` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#getOption(kotlin.Int)(optID: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Fetch the value of an option. Binary options will return java.lang.Boolean.TRUE if enabled, java.lang.Boolean.FALSE if disabled, e.g.: ```kotlin SocketImpl s; ... Boolean noDelay = (Boolean)(s.getOption(TCP_NODELAY)); if (noDelay.booleanValue()) { // true if TCP_NODELAY is enabled... ... } ``` <br /> For options that take a particular type as a parameter, getOption(int) will return the parameter's value, else it will return java.lang.Boolean.FALSE: ```kotlin Object o = s.getOption(SO_LINGER); if (o instanceof Integer) { System.out.print("Linger time is " + ((Integer)o).intValue()); } else { // the true type of o is java.lang.Boolean.FALSE; } ``` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#setOption(kotlin.Int,%20kotlin.Any)(optID: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Enable/disable the option specified by *optID* . If the option is to be enabled, and it takes an option-specific "value", this is passed in *value* . The actual type of value is option-specific, and it is an error to pass something that isn't of the expected type: ```kotlin SocketImpl s; ... s.setOption(SO_LINGER, new Integer(10)); // OK - set SO_LINGER w/ timeout of 10 sec. s.setOption(SO_LINGER, new Double(10)); // ERROR - expects java.lang.Integer ``` If the requested option is binary, it can be set using this method by a java.lang.Boolean: ```kotlin s.setOption(TCP_NODELAY, Boolean.TRUE); // OK - enables TCP_NODELAY, a binary option ``` <br /> Any option can be disabled using this method with a Boolean.FALSE: ```kotlin s.setOption(TCP_NODELAY, Boolean.FALSE); // OK - disables TCP_NODELAY s.setOption(SO_LINGER, Boolean.FALSE); // OK - disables SO_LINGER ``` <br /> For an option that has a notion of on and off, and requires a non-boolean parameter, setting its value to anything other than *Boolean.FALSE* implicitly enables it. Throws SocketException if the option is unrecognized, the socket is closed, or some low-level error occurred <br /> <br /> | ||

| Properties ||
|---|---|
| [InetAddress](../java/net/InetAddress.md)! | `https://developer.android.com/reference/kotlin/java/net/SocketImpl#address:java.net.InetAddress` The IP address of the remote end of this socket. |
| [FileDescriptor](../java/io/FileDescriptor.md)! | `https://developer.android.com/reference/kotlin/java/net/SocketImpl#fd:java.io.FileDescriptor` The file descriptor object for this socket. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/SocketImpl#localport:kotlin.Int` The local port number to which this socket is connected. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/SocketImpl#port:kotlin.Int` The port number on the remote host to which this socket is connected. |

## Public constructors

### SocketImpl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
SocketImpl()
```

## Public methods

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns the address and port of this socket as a `String`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of this socket. |

## Protected methods

### accept

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun accept(s: SocketImpl!): Unit
```

Accepts a connection.

| Parameters ||
|---|---|
| `s` | [SocketImpl](../java/net/SocketImpl.md)!: the accepted connection. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs when accepting the connection. |

### available

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun available(): Int
```

Returns the number of bytes that can be read from this socket without blocking.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of bytes that can be read from this socket without blocking. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs when determining the number of bytes available. |

### bind

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun bind(
    host: InetAddress!, 
    port: Int
): Unit
```

Binds this socket to the specified local IP address and port number.

| Parameters ||
|---|---|
| `host` | [InetAddress](../java/net/InetAddress.md)!: an IP address that belongs to a local interface. |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the port number. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs when binding this socket. |

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun close(): Unit
```

Closes this socket.

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs when closing this socket. |

### connect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun connect(
    host: String!, 
    port: Int
): Unit
```

Connects this socket to the specified port on the named host.

| Parameters ||
|---|---|
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of the remote host. |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the port number. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs when connecting to the remote host. |

### connect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun connect(
    address: InetAddress!, 
    port: Int
): Unit
```

Connects this socket to the specified port number on the specified host.

| Parameters ||
|---|---|
| `address` | [InetAddress](../java/net/InetAddress.md)!: the IP address of the remote host. |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the port number. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs when attempting a connection. |

### connect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun connect(
    address: SocketAddress!, 
    timeout: Int
): Unit
```

Connects this socket to the specified port number on the specified host. A timeout of zero is interpreted as an infinite timeout. The connection will then block until established or an error occurs.

| Parameters ||
|---|---|
| `address` | [SocketAddress](../java/net/SocketAddress.md)!: the Socket address of the remote host. |
| `timeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the timeout value, in milliseconds, or zero for no timeout. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs when attempting a connection. |

### create

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun create(stream: Boolean): Unit
```

Creates either a stream or a datagram socket.

| Parameters ||
|---|---|
| `stream` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if `true`, create a stream socket; otherwise, create a datagram socket. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs while creating the socket. |

### getFileDescriptor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun getFileDescriptor(): FileDescriptor!
```

Returns the value of this socket's `fd` field.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!` | the value of this socket's `fd` field. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/SocketImpl#fd:java.io.FileDescriptor`

### getInetAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun getInetAddress(): InetAddress!
```

Returns the value of this socket's `address` field.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/net/InetAddress!` | the value of this socket's `address` field. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/SocketImpl#address:java.net.InetAddress`

### getInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun getInputStream(): InputStream!
```

Returns an input stream for this socket.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/InputStream.html#!` | a stream for reading from this socket. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs when creating the input stream. |

### getLocalPort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun getLocalPort(): Int
```

Returns the value of this socket's `localport` field.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value of this socket's `localport` field. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/SocketImpl#localport:kotlin.Int`

### getOption

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun <T : Any!> getOption(name: SocketOption<T>!): T
```

Called to get a socket option.

| Parameters ||
|---|---|
| `<T>` | The type of the socket option value |
| `name` | [SocketOption](../java/net/SocketOption.md)\<T\>!: The socket option |

| Return ||
|---|---|
| `T` | the value of the named option |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs, or if the socket is closed. |
| `java.lang.UnsupportedOperationException` | if the SocketImpl does not support the option. |

### getOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun getOutputStream(): OutputStream!
```

Returns an output stream for this socket.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/OutputStream.html#!` | an output stream for writing to this socket. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs when creating the output stream. |

### getPort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun getPort(): Int
```

Returns the value of this socket's `port` field.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value of this socket's `port` field. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/SocketImpl#port:kotlin.Int`

### listen

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun listen(backlog: Int): Unit
```

Sets the maximum queue length for incoming connection indications (a request to connect) to the `count` argument. If a connection indication arrives when the queue is full, the connection is refused.

| Parameters ||
|---|---|
| `backlog` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the maximum length of the queue. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs when creating the queue. |

### sendUrgentData

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun sendUrgentData(data: Int): Unit
```

Send one byte of urgent data on the socket. The byte to be sent is the low eight bits of the parameter

| Parameters ||
|---|---|
| `data` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The byte of data to send |

| Exceptions ||
|---|---|
| `java.io.IOException` | if there is an error sending the data. |

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
| `name` | [SocketOption](../java/net/SocketOption.md)\<T\>!: The socket option |
| `value` | T: The value of the socket option. A value of `null` may be valid for some options. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs, or if the socket is closed. |
| `java.lang.UnsupportedOperationException` | if the SocketImpl does not support the option |

### setPerformancePreferences

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun setPerformancePreferences(
    connectionTime: Int, 
    latency: Int, 
    bandwidth: Int
): Unit
```

Sets performance preferences for this socket.

Sockets use the TCP/IP protocol by default. Some implementations may offer alternative protocols which have different performance characteristics than TCP/IP. This method allows the application to express its own preferences as to how these tradeoffs should be made when the implementation chooses from the available protocols.

Performance preferences are described by three integers whose values indicate the relative importance of short connection time, low latency, and high bandwidth. The absolute values of the integers are irrelevant; in order to choose a protocol the values are simply compared, with larger values indicating stronger preferences. Negative values represent a lower priority than positive values. If the application prefers short connection time over both low latency and high bandwidth, for example, then it could invoke this method with the values `(1, 0, 0)`. If the application prefers high bandwidth above low latency, and low latency above short connection time, then it could invoke this method with the values `(0, 1, 2)`. By default, this method does nothing, unless it is overridden in a sub-class.

| Parameters ||
|---|---|
| `connectionTime` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An `int` expressing the relative importance of a short connection time |
| `latency` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An `int` expressing the relative importance of low latency |
| `bandwidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An `int` expressing the relative importance of high bandwidth |
| --- | --- |

### shutdownInput

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun shutdownInput(): Unit
```

Places the input stream for this socket at "end of stream". Any data sent to this socket is acknowledged and then silently discarded. If you read from a socket input stream after invoking this method on the socket, the stream's `available` method will return 0, and its `read` methods will return `-1` (end of stream).

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs when shutting down this socket. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/Socket#shutdownOutput()`
- `https://developer.android.com/reference/kotlin/java/net/Socket#setSoLinger(kotlin.Boolean,%20kotlin.Int)`

### shutdownOutput

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun shutdownOutput(): Unit
```

Disables the output stream for this socket. For a TCP socket, any previously written data will be sent followed by TCP's normal connection termination sequence. If you write to a socket output stream after invoking shutdownOutput() on the socket, the stream will throw an IOException.

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs when shutting down this socket. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/Socket#shutdownInput()`
- `https://developer.android.com/reference/kotlin/java/net/Socket#setSoLinger(kotlin.Boolean,%20kotlin.Int)`

### supportedOptions

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun supportedOptions(): MutableSet<SocketOption<*>!>!
```

Returns a set of SocketOptions supported by this impl and by this impl's socket (Socket or ServerSocket)

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/java/net/SocketOption<*>!>!` | a Set of SocketOptions |

### supportsUrgentData

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun supportsUrgentData(): Boolean
```

Returns whether or not this SocketImpl supports sending urgent data. By default, false is returned unless the method is overridden in a sub-class

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if urgent data supported |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/SocketImpl#address:java.net.InetAddress`

## Properties

### address

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected var address: InetAddress!
```

The IP address of the remote end of this socket.

### fd

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected var fd: FileDescriptor!
```

The file descriptor object for this socket.

### localport

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected var localport: Int
```

The local port number to which this socket is connected.

### port

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected var port: Int
```

The port number on the remote host to which this socket is connected.
