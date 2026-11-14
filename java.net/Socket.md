# Socket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Socket

```
open class Socket : Closeable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.net.Socket](Socket.md) |

| Known Direct Subclasses [SSLSocket](../javax.net.ssl/SSLSocket.md) |-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [SSLSocket](../javax.net.ssl/SSLSocket.md) | This class extends`Socket`s and provides secure socket using protocols such as the "Secure Sockets Layer" (SSL) or IETF "Transport Layer Security" (TLS) protocols. | |
| --- | --- | --- | --- | --- | --- | --- |

This class implements client sockets (also called just "sockets"). A socket is an endpoint for communication between two machines.

The actual work of the socket is performed by an instance of the`SocketImpl`class. An application, by changing the socket factory that creates the socket implementation, can configure itself to create sockets appropriate to the local firewall.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Socket](Socket.md))`()` Creates an unconnected socket, with the system-default type of SocketImpl. |
| [Socket](Socket.md))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a stream socket and connects it to the specified port number on the named host. |
| [Socket](Socket.md))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `stream:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a stream socket and connects it to the specified port number on the named host. |
| [Socket](Socket.md))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `localAddr:` ` [InetAddress](InetAddress.md)!`, `localPort:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a socket and connects it to the specified remote host on the specified remote port. |
| [Socket](Socket.md))`(`address:` ` [InetAddress](InetAddress.md)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a stream socket and connects it to the specified port number at the specified IP address. |
| [Socket](Socket.md))`(`host:` ` [InetAddress](InetAddress.md)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `stream:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a socket and connects it to the specified port number at the specified IP address. |
| [Socket](Socket.md))`(`address:` ` [InetAddress](InetAddress.md)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `localAddr:` ` [InetAddress](InetAddress.md)!`, `localPort:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a socket and connects it to the specified remote address on the specified remote port. |
| [Socket](Socket.md))`(`proxy:` ` [Proxy](Proxy.md)!`)` Creates an unconnected socket, specifying the type of proxy, if any, that should be used regardless of any other settings. |

| Protected constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Socket](Socket.md))`(`impl:` ` [SocketImpl](SocketImpl.md)!`)` Creates an unconnected Socket with a user-specified SocketImpl. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bind](Socket.md))`(`bindpoint:` ` [SocketAddress](SocketAddress.md)!`)` Binds the socket to a local address. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](Socket.md))`()` Closes this socket. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](Socket.md))`(`endpoint:` ` [SocketAddress](SocketAddress.md)!`)` Connects this socket to the server. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](Socket.md))`(`endpoint:` ` [SocketAddress](SocketAddress.md)!`, `timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Connects this socket to the server with a specified timeout value. |
| open [SocketChannel](../java.nio.channels/SocketChannel.md)! | [getChannel](Socket.md))`()` Returns the unique [SocketChannel](../java.nio.channels/SocketChannel.md) object associated with this socket, if any. |
| open [InetAddress](InetAddress.md)! | [getInetAddress](Socket.md))`()` Returns the address to which the socket is connected. |
| --- | --- |
| open [InputStream](../java.io/InputStream.md)! | [getInputStream](Socket.md))`()` Returns an input stream for this socket. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getKeepAlive](Socket.md))`()` Tests if [SO_KEEPALIVE](SocketOptions.md) is enabled. |
| open [InetAddress](InetAddress.md)! | [getLocalAddress](Socket.md))`()` Gets the local address to which the socket is bound. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLocalPort](Socket.md))`()` Returns the local port number to which this socket is bound. |
| open [SocketAddress](SocketAddress.md)! | [getLocalSocketAddress](Socket.md))`()` Returns the address of the endpoint this socket is bound to. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getOOBInline](Socket.md))`()` Tests if [SO_OOBINLINE](SocketOptions.md) is enabled. |
| --- | --- |
| openT | [getOption](Socket.md))`(`name:` ` [SocketOption](SocketOption.md)<T>!`)` Returns the value of a socket option. |
| open [OutputStream](../java.io/OutputStream.md)! | [getOutputStream](Socket.md))`()` Returns an output stream for this socket. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPort](Socket.md))`()` Returns the remote port number to which this socket is connected. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getReceiveBufferSize](Socket.md))`()` Gets the value of the [SO_RCVBUF](SocketOptions.md) option for this`Socket`, that is the buffer size used by the platform for input on this`Socket`. |
| open [SocketAddress](SocketAddress.md)! | [getRemoteSocketAddress](Socket.md))`()` Returns the address of the endpoint this socket is connected to, or`null`if it is unconnected. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getReuseAddress](Socket.md))`()` Tests if [SO_REUSEADDR](SocketOptions.md) is enabled. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSendBufferSize](Socket.md))`()` Get value of the [SO_SNDBUF](SocketOptions.md) option for this`Socket`, that is the buffer size used by the platform for output on this`Socket`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSoLinger](Socket.md))`()` Returns setting for [SO_LINGER](SocketOptions.md). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSoTimeout](Socket.md))`()` Returns setting for [SO_TIMEOUT](SocketOptions.md). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getTcpNoDelay](Socket.md))`()` Tests if [TCP_NODELAY](SocketOptions.md) is enabled. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTrafficClass](Socket.md))`()` Gets traffic class or type-of-service in the IP header for packets sent from this Socket |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBound](Socket.md))`()` Returns the binding state of the socket. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isClosed](Socket.md))`()` Returns the closed state of the socket. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnected](Socket.md))`()` Returns the connection state of the socket. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInputShutdown](Socket.md))`()` Returns whether the read-half of the socket connection is closed. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOutputShutdown](Socket.md))`()` Returns whether the write-half of the socket connection is closed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendUrgentData](Socket.md))`(`data:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Send one byte of urgent data on the socket. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setKeepAlive](Socket.md))`(`on:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Enable/disable [SO_KEEPALIVE](SocketOptions.md). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOOBInline](Socket.md))`(`on:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Enable/disable [SO_OOBINLINE](SocketOptions.md)(receipt of TCP urgent data) By default, this option is disabled and TCP urgent data received on a socket is silently discarded. |
| open [Socket](Socket.md)! | [setOption](Socket.md))`(`name:` ` [SocketOption](SocketOption.md)<T>!`, `value:` `T`)` Sets the value of a socket option. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPerformancePreferences](Socket.md))`(`connectionTime:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `latency:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bandwidth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets performance preferences for this socket. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setReceiveBufferSize](Socket.md))`(`size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the [SO_RCVBUF](SocketOptions.md) option to the specified value for this`Socket`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setReuseAddress](Socket.md))`(`on:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Enable/disable the [SO_REUSEADDR](SocketOptions.md) socket option. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSendBufferSize](Socket.md))`(`size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the [SO_SNDBUF](SocketOptions.md) option to the specified value for this`Socket`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSoLinger](Socket.md))`(`on:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `linger:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Enable/disable [SO_LINGER](SocketOptions.md) with the specified linger time in seconds. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSoTimeout](Socket.md))`(`timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Enable/disable [SO_TIMEOUT](SocketOptions.md) with the specified timeout, in milliseconds. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSocketImplFactory](Socket.md))`(`fac:` ` [SocketImplFactory](SocketImplFactory.md)!`)` Sets the client socket implementation factory for the application. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTcpNoDelay](Socket.md))`(`on:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Enable/disable [TCP_NODELAY](SocketOptions.md)(disable/enable Nagle's algorithm). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTrafficClass](Socket.md))`(`tc:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets traffic class or type-of-service octet in the IP header for packets sent from this Socket. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [shutdownInput](Socket.md))`()` Places the input stream for this socket at "end of stream". |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [shutdownOutput](Socket.md))`()` Disables the output stream for this socket. |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [SocketOption](SocketOption.md)\<\*\>!\>! | [supportedOptions](Socket.md))`()` Returns a set of the socket options supported by this socket. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](Socket.md))`()` Converts this socket to a`String`. |
| --- | --- |

## Public constructors

### Socket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Socket()
```

Creates an unconnected socket, with the system-default type of SocketImpl. 

### Socket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Socket(
    host: String!, 
    port: Int)
```

Creates a stream socket and connects it to the specified port number on the named host.

If the specified host is`null`it is the equivalent of specifying the address as [InetAddress.getByName](InetAddress.md))`(null)`. In other words, it is equivalent to specifying an address of the loopback interface.

If the application has specified a server socket factory, that factory's`createSocketImpl`method is called to create the actual socket implementation. Otherwise a "plain" socket is created.

If there is a security manager, its`checkConnect`method is called with the host address and`port`as its arguments. This could result in a SecurityException.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------|
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the host name, or`null`for the loopback address. |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the port number. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| `java.net.UnknownHostException` | if the IP address of the host could not be determined. |
| `java.io.IOException` | if an I/O error occurs when creating the socket. |
| `java.lang.SecurityException` | if a security manager exists and its`checkConnect`method doesn't allow the operation. |
| --- | --- |
| `java.lang.IllegalArgumentException` | if the port parameter is outside the specified range of valid port values, which is between 0 and 65535, inclusive. |

**See Also**

- [java.net.Socket#setSocketImplFactory(java.net.SocketImplFactory)](Socket.md))
- [java.net.SocketImpl](SocketImpl.md)
- [java.net.SocketImplFactory#createSocketImpl()](SocketImplFactory.md)) 

### Socket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Socket(
    host: String!, 
    port: Int, 
    stream: Boolean)
```

**Deprecated:** *Use DatagramSocket instead for UDP transport.*

Creates a stream socket and connects it to the specified port number on the named host.

If the specified host is`null`it is the equivalent of specifying the address as [InetAddress.getByName](InetAddress.md))`(null)`. In other words, it is equivalent to specifying an address of the loopback interface.

If the stream argument is`true`, this creates a stream socket. If the stream argument is`false`, it creates a datagram socket.

If the application has specified a server socket factory, that factory's`createSocketImpl`method is called to create the actual socket implementation. Otherwise a "plain" socket is created.

If there is a security manager, its`checkConnect`method is called with the host address and`port`as its arguments. This could result in a SecurityException.

If a UDP socket is used, TCP/IP related socket options will not apply.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the host name, or`null`for the loopback address. |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the port number. |
| `stream` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):a`boolean`indicating whether this is a stream socket or a datagram socket. |
| --- | --- |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs when creating the socket. |
| `java.lang.SecurityException` | if a security manager exists and its`checkConnect`method doesn't allow the operation. |
| `java.lang.IllegalArgumentException` | if the port parameter is outside the specified range of valid port values, which is between 0 and 65535, inclusive. |
| --- | --- |

**See Also**

- [java.net.Socket#setSocketImplFactory(java.net.SocketImplFactory)](Socket.md))
- [java.net.SocketImpl](SocketImpl.md)
- [java.net.SocketImplFactory#createSocketImpl()](SocketImplFactory.md)) 

### Socket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Socket(
    host: String!, 
    port: Int, 
    localAddr: InetAddress!, 
    localPort: Int)
```

Creates a socket and connects it to the specified remote host on the specified remote port. The Socket will also bind() to the local address and port supplied.

If the specified host is`null`it is the equivalent of specifying the address as [InetAddress.getByName](InetAddress.md))`(null)`. In other words, it is equivalent to specifying an address of the loopback interface.

A local port number of`zero`will let the system pick up a free port in the`bind`operation.

If there is a security manager, its`checkConnect`method is called with the host address and`port`as its arguments. This could result in a SecurityException.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the remote host, or`null`for the loopback address. |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the remote port |
| `localAddr` | [InetAddress](InetAddress.md)!:the local address the socket is bound to, or`null`for the`anyLocal`address. |
| --- | --- |
| `localPort` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the local port the socket is bound to, or`zero`for a system selected free port. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs when creating the socket. |
| `java.lang.SecurityException` | if a security manager exists and its`checkConnect`method doesn't allow the connection to the destination, or if its`checkListen`method doesn't allow the bind to the local port. |
| `java.lang.IllegalArgumentException` | if the port parameter or localPort parameter is outside the specified range of valid port values, which is between 0 and 65535, inclusive. |
| --- | --- |

**See Also**

### Socket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Socket(
    address: InetAddress!, 
    port: Int)
```

Creates a stream socket and connects it to the specified port number at the specified IP address.

If the application has specified a socket factory, that factory's`createSocketImpl`method is called to create the actual socket implementation. Otherwise a "plain" socket is created.

If there is a security manager, its`checkConnect`method is called with the host address and`port`as its arguments. This could result in a SecurityException.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------|
| `address` | [InetAddress](InetAddress.md)!:the IP address. |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the port number. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs when creating the socket. |
| `java.lang.SecurityException` | if a security manager exists and its`checkConnect`method doesn't allow the operation. |
| `java.lang.IllegalArgumentException` | if the port parameter is outside the specified range of valid port values, which is between 0 and 65535, inclusive. |
| --- | --- |
| `java.lang.NullPointerException` | if`address`is null. |

**See Also**

- [java.net.Socket#setSocketImplFactory(java.net.SocketImplFactory)](Socket.md))
- [java.net.SocketImpl](SocketImpl.md)
- [java.net.SocketImplFactory#createSocketImpl()](SocketImplFactory.md)) 

### Socket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Socket(
    host: InetAddress!, 
    port: Int, 
    stream: Boolean)
```

**Deprecated:** *Use DatagramSocket instead for UDP transport.*

Creates a socket and connects it to the specified port number at the specified IP address.

If the stream argument is`true`, this creates a stream socket. If the stream argument is`false`, it creates a datagram socket.

If the application has specified a server socket factory, that factory's`createSocketImpl`method is called to create the actual socket implementation. Otherwise a "plain" socket is created.

If there is a security manager, its`checkConnect`method is called with`host.getHostAddress()`and`port`as its arguments. This could result in a SecurityException.

If UDP socket is used, TCP/IP related socket options will not apply.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `host` | [InetAddress](InetAddress.md)!:the IP address. |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the port number. |
| `stream` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if`true`, create a stream socket; otherwise, create a datagram socket. |
| --- | --- |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs when creating the socket. |
| `java.lang.SecurityException` | if a security manager exists and its`checkConnect`method doesn't allow the operation. |
| `java.lang.IllegalArgumentException` | if the port parameter is outside the specified range of valid port values, which is between 0 and 65535, inclusive. |
| --- | --- |
| `java.lang.NullPointerException` | if`host`is null. |

**See Also**

- [java.net.Socket#setSocketImplFactory(java.net.SocketImplFactory)](Socket.md))
- [java.net.SocketImpl](SocketImpl.md)
- [java.net.SocketImplFactory#createSocketImpl()](SocketImplFactory.md)) 

### Socket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Socket(
    address: InetAddress!, 
    port: Int, 
    localAddr: InetAddress!, 
    localPort: Int)
```

Creates a socket and connects it to the specified remote address on the specified remote port. The Socket will also bind() to the local address and port supplied.

If the specified local address is`null`it is the equivalent of specifying the address as the AnyLocal address (see [InetAddress.isAnyLocalAddress](InetAddress.md))`()`).

A local port number of`zero`will let the system pick up a free port in the`bind`operation.

If there is a security manager, its`checkConnect`method is called with the host address and`port`as its arguments. This could result in a SecurityException.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `address` | [InetAddress](InetAddress.md)!:the remote address |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the remote port |
| `localAddr` | [InetAddress](InetAddress.md)!:the local address the socket is bound to, or`null`for the`anyLocal`address. |
| --- | --- |
| `localPort` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the local port the socket is bound to or`zero`for a system selected free port. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs when creating the socket. |
| `java.lang.SecurityException` | if a security manager exists and its`checkConnect`method doesn't allow the connection to the destination, or if its`checkListen`method doesn't allow the bind to the local port. |
| `java.lang.IllegalArgumentException` | if the port parameter or localPort parameter is outside the specified range of valid port values, which is between 0 and 65535, inclusive. |
| --- | --- |
| `java.lang.NullPointerException` | if`address`is null. |

**See Also**

### Socket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Socket(proxy: Proxy!)
```

Creates an unconnected socket, specifying the type of proxy, if any, that should be used regardless of any other settings.

If there is a security manager, its`checkConnect`method is called with the proxy host address and port number as its arguments. This could result in a SecurityException.

Examples:

- `Socket s = new Socket(Proxy.NO_PROXY);`will create a plain socket ignoring any other proxy configuration.
- `Socket s = new Socket(new Proxy(Proxy.Type.SOCKS, new InetSocketAddress("socks.mydom.com", 1080)));`will create a socket connecting through the specified SOCKS proxy server.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `proxy` | [Proxy](Proxy.md)!:a [Proxy](Proxy.md) object specifying what kind of proxying should be used. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the proxy is of an invalid type or`null`. |
| `java.lang.SecurityException` | if a security manager is present and permission to connect to the proxy is denied. |

**See Also**

- [java.net.ProxySelector](ProxySelector.md)
- [java.net.Proxy](Proxy.md)

## Protected constructors

### Socket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected Socket(impl: SocketImpl!)
```

Creates an unconnected Socket with a user-specified SocketImpl.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `impl` | [SocketImpl](SocketImpl.md)!:an instance of a**SocketImpl**the subclass wishes to use on the Socket. |

| Exceptions ||
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if`impl`is non-null and a security manager is set and its`checkPermission`method doesn't allow`NetPermission("setSocketImpl")`. |
| `java.net.SocketException` | if there is an error in the underlying protocol, such as a TCP error. |

## Public methods

### bind

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun bind(bindpoint: SocketAddress!): Unit
```

Binds the socket to a local address.

If the address is`null`, then the system will pick up an ephemeral port and a valid local address to bind the socket.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------|
| `bindpoint` | [SocketAddress](SocketAddress.md)!:the`SocketAddress`to bind to |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if the bind operation fails, or if the socket is already bound. |
| `java.lang.IllegalArgumentException` | if bindpoint is a SocketAddress subclass not supported by this socket |
| `java.lang.SecurityException` | if a security manager exists and its`checkListen`method doesn't allow the bind to the local port. |
| --- | --- |

**See Also**

- [#isBound](Socket.md)) 

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Closes this socket.

Any thread currently blocked in an I/O operation upon this socket will throw a [SocketException](SocketException.md).

Once a socket has been closed, it is not available for further networking use (i.e. can't be reconnected or rebound). A new socket needs to be created.

Closing this socket will also close the socket's [InputStream](../java.io/InputStream.md) and [OutputStream](../java.io/OutputStream.md).

If this socket has an associated channel then the channel is closed as well.

| Exceptions ||
|-----------------------|--------------------------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs |
| `java.io.IOException` | if an I/O error occurs when closing this socket. |
| --- | --- |

**See Also**

- [#isClosed](Socket.md)) 

### connect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun connect(endpoint: SocketAddress!): Unit
```

Connects this socket to the server.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------|
| `endpoint` | [SocketAddress](SocketAddress.md)!:the`SocketAddress` |

| Exceptions ||
|--------------------------------------------------|-----------------------------------------------------------------------------------|
| `java.io.IOException` | if an error occurs during the connection |
| `java.nio.channels.IllegalBlockingModeException` | if this socket has an associated channel, and the channel is in non-blocking mode |
| `java.lang.IllegalArgumentException` | if endpoint is null or is a SocketAddress subclass not supported by this socket |
| --- | --- |

### connect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun connect(
    endpoint: SocketAddress!, 
    timeout: Int
): Unit
```

Connects this socket to the server with a specified timeout value. A timeout of zero is interpreted as an infinite timeout. The connection will then block until established or an error occurs.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------|
| `endpoint` | [SocketAddress](SocketAddress.md)!:the`SocketAddress` |
| `timeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the timeout value to be used in milliseconds. |

| Exceptions ||
|--------------------------------------------------|-----------------------------------------------------------------------------------|
| `java.io.IOException` | if an error occurs during the connection |
| `java.net.SocketTimeoutException` | if timeout expires before connecting |
| `java.nio.channels.IllegalBlockingModeException` | if this socket has an associated channel, and the channel is in non-blocking mode |
| --- | --- |
| `java.lang.IllegalArgumentException` | if endpoint is null or is a SocketAddress subclass not supported by this socket |

### getChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getChannel(): SocketChannel!
```

Returns the unique [SocketChannel](../java.nio.channels/SocketChannel.md) object associated with this socket, if any.

A socket will have a channel if, and only if, the channel itself was created via the java.nio.channels.SocketChannel#open or [ServerSocketChannel.accept](../java.nio.channels/ServerSocketChannel.md))methods.

| Return ||
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [SocketChannel](../java.nio.channels/SocketChannel.md)! | the socket channel associated with this socket, or`null`if this socket was not created for a channel |

### getInetAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInetAddress(): InetAddress!
```

Returns the address to which the socket is connected.

If the socket was connected prior to being #close, then this method will continue to return the connected address after the socket is closed.

| Return ||
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [InetAddress](InetAddress.md)! | the remote IP address to which this socket is connected, or`null`if the socket is not connected. |

### getInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInputStream(): InputStream!
```

Returns an input stream for this socket.

If this socket has an associated channel then the resulting input stream delegates all of its operations to the channel. If the channel is in non-blocking mode then the input stream's`read`operations will throw an [java.nio.channels.IllegalBlockingModeException](../java.nio.channels/IllegalBlockingModeException.md).

Under abnormal conditions the underlying connection may be broken by the remote host or the network software (for example a connection reset in the case of TCP connections). When a broken connection is detected by the network software the following applies to the returned input stream :-

- The network software may discard bytes that are buffered by the socket. Bytes that aren't discarded by the network software can be read using java.io.InputStream#read.
- If there are no bytes buffered on the socket, or all buffered bytes have been consumed by java.io.InputStream#read, then all subsequent calls to java.io.InputStream#read will throw an [IOException](../java.io/IOException.md).
- If there are no bytes buffered on the socket, and the socket has not been closed using #close, then [available](../java.io/InputStream.md))will return`0`.

Closing the returned [InputStream](../java.io/InputStream.md) will close the associated socket.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [InputStream](../java.io/InputStream.md)! | an input stream for reading bytes from this socket. |

| Exceptions ||
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs when creating the input stream, the socket is closed, the socket is not connected, or the socket input has been shutdown using [shutdownInput()](Socket.md)) |

### getKeepAlive

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKeepAlive(): Boolean
```

Tests if [SO_KEEPALIVE](SocketOptions.md) is enabled.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a`boolean`indicating whether or not [SO_KEEPALIVE](SocketOptions.md) is enabled. |

| Exceptions ||
|----------------------------|-----------------------------------------------------------------------|
| `java.net.SocketException` | if there is an error in the underlying protocol, such as a TCP error. |

**See Also**

- [#setKeepAlive(boolean)](Socket.md)) 

### getLocalAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLocalAddress(): InetAddress!
```

Gets the local address to which the socket is bound.

If there is a security manager set, its`checkConnect`method is called with the local address and`-1`as its arguments to see if the operation is allowed. If the operation is not allowed, the [loopback](InetAddress.md))address is returned.

| Return ||
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [InetAddress](InetAddress.md)! | the local address to which the socket is bound, the loopback address if denied by the security manager, or the wildcard address if the socket is closed or not bound yet. |

**See Also**

### getLocalPort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLocalPort(): Int
```

Returns the local port number to which this socket is bound.

If the socket was bound prior to being #close, then this method will continue to return the local port number after the socket is closed.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the local port number to which this socket is bound or -1 if the socket is not bound yet. |

### getLocalSocketAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLocalSocketAddress(): SocketAddress!
```

Returns the address of the endpoint this socket is bound to.

If a socket bound to an endpoint represented by an`InetSocketAddress `is #close, then this method will continue to return an`InetSocketAddress`after the socket is closed. In that case the returned`InetSocketAddress`'s address is the [wildcard](InetAddress.md))address and its port is the local port that it was bound to.

If there is a security manager set, its`checkConnect`method is called with the local address and`-1`as its arguments to see if the operation is allowed. If the operation is not allowed, a`SocketAddress`representing the [loopback](InetAddress.md))address and the local port to which this socket is bound is returned.

| Return ||
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SocketAddress](SocketAddress.md)! | a`SocketAddress`representing the local endpoint of this socket, or a`SocketAddress`representing the loopback address if denied by the security manager, or`null`if the socket is not bound yet. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/Socket#getLocalAddress()>
- <https://developer.android.com/reference/kotlin/java/net/Socket#getLocalPort()>
- [#bind(SocketAddress)](Socket.md)) 

### getOOBInline

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOOBInline(): Boolean
```

Tests if [SO_OOBINLINE](SocketOptions.md) is enabled.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a`boolean`indicating whether or not [SO_OOBINLINE](SocketOptions.md) is enabled. |

| Exceptions ||
|----------------------------|-----------------------------------------------------------------------|
| `java.net.SocketException` | if there is an error in the underlying protocol, such as a TCP error. |

**See Also**

- [#setOOBInline(boolean)](Socket.md)) 

### getOption

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Any!> getOption(name: SocketOption<T>!): T
```

Returns the value of a socket option.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------|
| `<T>` | The type of the socket option value |
| `name` | [SocketOption](SocketOption.md)\<T\>!:The socket option |

| Return ||
|---|---------------------------------|
| T | The value of the socket option. |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the socket does not support the option. |
| `java.io.IOException` | if an I/O error occurs, or if the socket is closed. |
| `java.lang.NullPointerException` | if name is`null` |
| --- | --- |
| `java.lang.SecurityException` | if a security manager is set and if the socket option requires a security permission and if the caller does not have the required permission. [StandardSocketOptions](StandardSocketOptions.md) do not require any security permission. |

### getOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOutputStream(): OutputStream!
```

Returns an output stream for this socket.

If this socket has an associated channel then the resulting output stream delegates all of its operations to the channel. If the channel is in non-blocking mode then the output stream's`write`operations will throw an .

Closing the returned [OutputStream](../java.io/OutputStream.md) will close the associated socket.

| Return ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------|
| [OutputStream](../java.io/OutputStream.md)! | an output stream for writing bytes to this socket. |

| Exceptions ||
|-----------------------|-------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs when creating the output stream or if the socket is not connected. |

### getPort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPort(): Int
```

Returns the remote port number to which this socket is connected.

If the socket was connected prior to being #close, then this method will continue to return the connected port number after the socket is closed.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the remote port number to which this socket is connected, or 0 if the socket is not connected yet. |

### getReceiveBufferSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getReceiveBufferSize(): Int
```

Gets the value of the [SO_RCVBUF](SocketOptions.md) option for this`Socket`, that is the buffer size used by the platform for input on this`Socket`.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value of the [SO_RCVBUF](SocketOptions.md) option for this`Socket`. |

| Exceptions ||
|----------------------------|-----------------------------------------------------------------------|
| `java.net.SocketException` | if there is an error in the underlying protocol, such as a TCP error. |

**See Also**

- [#setReceiveBufferSize(int)](Socket.md)) 

### getRemoteSocketAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRemoteSocketAddress(): SocketAddress!
```

Returns the address of the endpoint this socket is connected to, or`null`if it is unconnected.

If the socket was connected prior to being #close, then this method will continue to return the connected address after the socket is closed.

| Return ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [SocketAddress](SocketAddress.md)! | a`SocketAddress`representing the remote endpoint of this socket, or`null`if it is not connected yet. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/Socket#getInetAddress()>
- <https://developer.android.com/reference/kotlin/java/net/Socket#getPort()>
- [#connect(SocketAddress, int)](Socket.md))
- [#connect(SocketAddress)](Socket.md)) 

### getReuseAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getReuseAddress(): Boolean
```

Tests if [SO_REUSEADDR](SocketOptions.md) is enabled.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a`boolean`indicating whether or not [SO_REUSEADDR](SocketOptions.md) is enabled. |

| Exceptions ||
|----------------------------|-----------------------------------------------------------------------|
| `java.net.SocketException` | if there is an error in the underlying protocol, such as a TCP error. |

**See Also**

- [#setReuseAddress(boolean)](Socket.md)) 

### getSendBufferSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSendBufferSize(): Int
```

Get value of the [SO_SNDBUF](SocketOptions.md) option for this`Socket`, that is the buffer size used by the platform for output on this`Socket`.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value of the [SO_SNDBUF](SocketOptions.md) option for this`Socket`. |

| Exceptions ||
|----------------------------|-----------------------------------------------------------------------|
| `java.net.SocketException` | if there is an error in the underlying protocol, such as a TCP error. |

**See Also**

- [#setSendBufferSize(int)](Socket.md)) 

### getSoLinger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSoLinger(): Int
```

Returns setting for [SO_LINGER](SocketOptions.md). -1 returns implies that the option is disabled. The setting only affects socket close.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the setting for [SO_LINGER](SocketOptions.md). |

| Exceptions ||
|----------------------------|-----------------------------------------------------------------------|
| `java.net.SocketException` | if there is an error in the underlying protocol, such as a TCP error. |

**See Also**

- [#setSoLinger(boolean, int)](Socket.md)) 

### getSoTimeout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSoTimeout(): Int
```

Returns setting for [SO_TIMEOUT](SocketOptions.md). 0 returns implies that the option is disabled (i.e., timeout of infinity).

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the setting for [SO_TIMEOUT](SocketOptions.md) |

| Exceptions ||
|----------------------------|-----------------------------------------------------------------------|
| `java.net.SocketException` | if there is an error in the underlying protocol, such as a TCP error. |

**See Also**

- [#setSoTimeout(int)](Socket.md)) 

### getTcpNoDelay

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTcpNoDelay(): Boolean
```

Tests if [TCP_NODELAY](SocketOptions.md) is enabled.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a`boolean`indicating whether or not [TCP_NODELAY](SocketOptions.md) is enabled. |

| Exceptions ||
|----------------------------|-----------------------------------------------------------------------|
| `java.net.SocketException` | if there is an error in the underlying protocol, such as a TCP error. |

**See Also**

- [#setTcpNoDelay(boolean)](Socket.md)) 

### getTrafficClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTrafficClass(): Int
```

Gets traffic class or type-of-service in the IP header for packets sent from this Socket

As the underlying network implementation may ignore the traffic class or type-of-service set using [setTrafficClass(int)](Socket.md))this method may return a different value than was previously set using the [setTrafficClass(int)](Socket.md))method on this Socket.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the traffic class or type-of-service already set |

| Exceptions ||
|----------------------------|----------------------------------------------------------------------------|
| `java.net.SocketException` | if there is an error obtaining the traffic class or type-of-service value. |

**See Also**

- [#setTrafficClass(int)](Socket.md))
- [java.net.SocketOptions#IP_TOS](SocketOptions.md) 

### isBound

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isBound(): Boolean
```

Returns the binding state of the socket.

Note: Closing a socket doesn't clear its binding state, which means this method will return`true`for a closed socket (see [isClosed()](Socket.md))) if it was successfuly bound prior to being closed.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the socket was successfuly bound to an address |

**See Also**

- [#bind](Socket.md)) 

### isClosed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isClosed(): Boolean
```

Returns the closed state of the socket.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the socket has been closed |

**See Also**

### isConnected

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isConnected(): Boolean
```

Returns the connection state of the socket.

Note: Closing a socket doesn't clear its connection state, which means this method will return`true`for a closed socket (see [isClosed()](Socket.md))) if it was successfuly connected prior to being closed.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the socket was successfuly connected to a server |

### isInputShutdown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isInputShutdown(): Boolean
```

Returns whether the read-half of the socket connection is closed.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the input of the socket has been shutdown |

**See Also**

- [#shutdownInput](Socket.md)) 

### isOutputShutdown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isOutputShutdown(): Boolean
```

Returns whether the write-half of the socket connection is closed.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the output of the socket has been shutdown |

**See Also**

- [#shutdownOutput](Socket.md)) 

### sendUrgentData

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun sendUrgentData(data: Int): Unit
```

Send one byte of urgent data on the socket. The byte to be sent is the lowest eight bits of the data parameter. The urgent byte is sent after any preceding writes to the socket OutputStream and before any future writes to the OutputStream.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------|
| `data` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The byte of data to send |

| Exceptions ||
|-----------------------|----------------------------------------|
| `java.io.IOException` | if there is an error sending the data. |

### setKeepAlive

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setKeepAlive(on: Boolean): Unit
```

Enable/disable [SO_KEEPALIVE](SocketOptions.md).

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------------------|
| `on` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether or not to have socket keep alive turned on. |

| Exceptions ||
|----------------------------|-----------------------------------------------------------------------|
| `java.net.SocketException` | if there is an error in the underlying protocol, such as a TCP error. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/Socket#getKeepAlive()> 

### setOOBInline

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOOBInline(on: Boolean): Unit
```

Enable/disable [SO_OOBINLINE](SocketOptions.md)(receipt of TCP urgent data) By default, this option is disabled and TCP urgent data received on a socket is silently discarded. If the user wishes to receive urgent data, then this option must be enabled. When enabled, urgent data is received inline with normal data.

Note, only limited support is provided for handling incoming urgent data. In particular, no notification of incoming urgent data is provided and there is no capability to distinguish between normal data and urgent data unless provided by a higher level protocol.

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `on` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`to enable [SO_OOBINLINE](SocketOptions.md),`false`to disable. |

| Exceptions ||
|----------------------------|-----------------------------------------------------------------------|
| `java.net.SocketException` | if there is an error in the underlying protocol, such as a TCP error. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/Socket#getOOBInline()> 

### setOption

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Any!> setOption(
    name: SocketOption<T>!, 
    value: T
): Socket!
```

Sets the value of a socket option.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `<T>` | The type of the socket option value |
| `name` | [SocketOption](SocketOption.md)\<T\>!:The socket option |
| `value` | T:The value of the socket option. A value of`null`may be valid for some options. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|-------------|
| [Socket](Socket.md)! | this Socket |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the socket does not support the option. |
| `java.lang.IllegalArgumentException` | if the value is not valid for the option. |
| `java.io.IOException` | if an I/O error occurs, or if the socket is closed. |
| --- | --- |
| `java.lang.NullPointerException` | if name is`null` |
| `java.lang.SecurityException` | if a security manager is set and if the socket option requires a security permission and if the caller does not have the required permission. [StandardSocketOptions](StandardSocketOptions.md) do not require any security permission. |

### setPerformancePreferences

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPerformancePreferences(
    connectionTime: Int, 
    latency: Int, 
    bandwidth: Int
): Unit
```

Sets performance preferences for this socket.

Sockets use the TCP/IP protocol by default. Some implementations may offer alternative protocols which have different performance characteristics than TCP/IP. This method allows the application to express its own preferences as to how these tradeoffs should be made when the implementation chooses from the available protocols.

Performance preferences are described by three integers whose values indicate the relative importance of short connection time, low latency, and high bandwidth. The absolute values of the integers are irrelevant; in order to choose a protocol the values are simply compared, with larger values indicating stronger preferences. Negative values represent a lower priority than positive values. If the application prefers short connection time over both low latency and high bandwidth, for example, then it could invoke this method with the values`(1, 0, 0)`. If the application prefers high bandwidth above low latency, and low latency above short connection time, then it could invoke this method with the values`(0, 1, 2)`.

Invoking this method after this socket has been connected will have no effect.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `connectionTime` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):An`int`expressing the relative importance of a short connection time |
| `latency` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):An`int`expressing the relative importance of low latency |
| `bandwidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):An`int`expressing the relative importance of high bandwidth |
| --- | --- |

### setReceiveBufferSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setReceiveBufferSize(size: Int): Unit
```

Sets the [SO_RCVBUF](SocketOptions.md) option to the specified value for this`Socket`. The [SO_RCVBUF](SocketOptions.md) option is used by the platform's networking code as a hint for the size to set the underlying network I/O buffers.

Increasing the receive buffer size can increase the performance of network I/O for high-volume connection, while decreasing it can help reduce the backlog of incoming data.

Because [SO_RCVBUF](SocketOptions.md) is a hint, applications that want to verify what size the buffers were set to should call [getReceiveBufferSize()](Socket.md)).

The value of [SO_RCVBUF](SocketOptions.md) is also used to set the TCP receive window that is advertized to the remote peer. Generally, the window size can be modified at any time when a socket is connected. However, if a receive window larger than 64K is required then this must be requested**before**the socket is connected to the remote peer. There are two cases to be aware of:

1. For sockets accepted from a ServerSocket, this must be done by calling [ServerSocket.setReceiveBufferSize(int)](ServerSocket.md))before the ServerSocket is bound to a local address.
2. For client sockets, setReceiveBufferSize() must be called before connecting the socket to its remote peer.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the size to which to set the receive buffer size. This value must be greater than 0. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the value is 0 or is negative. |
| `java.net.SocketException` | if there is an error in the underlying protocol, such as a TCP error. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/Socket#getReceiveBufferSize()>
- [java.net.ServerSocket#setReceiveBufferSize(int)](ServerSocket.md)) 

### setReuseAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setReuseAddress(on: Boolean): Unit
```

Enable/disable the [SO_REUSEADDR](SocketOptions.md) socket option.

When a TCP connection is closed the connection may remain in a timeout state for a period of time after the connection is closed (typically known as the`TIME_WAIT`state or`2MSL`wait state). For applications using a well known socket address or port it may not be possible to bind a socket to the required`SocketAddress`if there is a connection in the timeout state involving the socket address or port.

Enabling [SO_REUSEADDR](SocketOptions.md) prior to binding the socket using [bind(java.net.SocketAddress)](Socket.md))allows the socket to be bound even though a previous connection is in a timeout state.

When a`Socket`is created the initial setting of [SO_REUSEADDR](SocketOptions.md) is disabled.

The behaviour when [SO_REUSEADDR](SocketOptions.md) is enabled or disabled after a socket is bound (See [isBound()](Socket.md))) is not defined.

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------------------|
| `on` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether to enable or disable the socket option |

| Exceptions ||
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.net.SocketException` | if an error occurs enabling or disabling the [SO_REUSEADDR](SocketOptions.md) socket option, or the socket is closed. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/Socket#getReuseAddress()>
- [#bind(SocketAddress)](Socket.md))
- <https://developer.android.com/reference/kotlin/java/net/Socket#isClosed()>
- <https://developer.android.com/reference/kotlin/java/net/Socket#isBound()> 

### setSendBufferSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSendBufferSize(size: Int): Unit
```

Sets the [SO_SNDBUF](SocketOptions.md) option to the specified value for this`Socket`. The [SO_SNDBUF](SocketOptions.md) option is used by the platform's networking code as a hint for the size to set the underlying network I/O buffers.

Because [SO_SNDBUF](SocketOptions.md) is a hint, applications that want to verify what size the buffers were set to should call [getSendBufferSize()](Socket.md)).

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the size to which to set the send buffer size. This value must be greater than 0. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------|
| `java.net.SocketException` | if there is an error in the underlying protocol, such as a TCP error. |
| `java.lang.IllegalArgumentException` | if the value is 0 or is negative. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/Socket#getSendBufferSize()> 

### setSoLinger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSoLinger(
    on: Boolean, 
    linger: Int
): Unit
```

Enable/disable [SO_LINGER](SocketOptions.md) with the specified linger time in seconds. The maximum timeout value is platform specific. The setting only affects socket close.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------|
| `on` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether or not to linger on. |
| `linger` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):how long to linger for, if on is true. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------|
| `java.net.SocketException` | if there is an error in the underlying protocol, such as a TCP error. |
| `java.lang.IllegalArgumentException` | if the linger value is negative. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/Socket#getSoLinger()> 

### setSoTimeout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSoTimeout(timeout: Int): Unit
```

Enable/disable [SO_TIMEOUT](SocketOptions.md) with the specified timeout, in milliseconds. With this option set to a non-zero timeout, a read() call on the InputStream associated with this Socket will block for only this amount of time. If the timeout expires, a**java.net.SocketTimeoutException** is raised, though the Socket is still valid. The option**must** be enabled prior to entering the blocking operation to have effect. The timeout must be`> 0`. A timeout of zero is interpreted as an infinite timeout.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the specified timeout, in milliseconds. |

| Exceptions ||
|----------------------------|-----------------------------------------------------------------------|
| `java.net.SocketException` | if there is an error in the underlying protocol, such as a TCP error. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/Socket#getSoTimeout()> 

### setSocketImplFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun setSocketImplFactory(fac: SocketImplFactory!): Unit
```

Sets the client socket implementation factory for the application. The factory can be specified only once.

When an application creates a new client socket, the socket implementation factory's`createSocketImpl`method is called to create the actual socket implementation.

Passing`null`to the method is a no-op unless the factory was already set.

If there is a security manager, this method first calls the security manager's`checkSetFactory`method to ensure the operation is allowed. This could result in a SecurityException.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------|
| `fac` | [SocketImplFactory](SocketImplFactory.md)!:the desired factory. |

| Exceptions ||
|-------------------------------|------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs when setting the socket factory. |
| `java.net.SocketException` | if the factory is already defined. |
| `java.lang.SecurityException` | if a security manager exists and its`checkSetFactory`method doesn't allow the operation. |
| --- | --- |

**See Also**

- [java.net.SocketImplFactory#createSocketImpl()](SocketImplFactory.md))
- [java.lang.SecurityManager#checkSetFactory](../java.lang/SecurityManager.md)) 

### setTcpNoDelay

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTcpNoDelay(on: Boolean): Unit
```

Enable/disable [TCP_NODELAY](SocketOptions.md)(disable/enable Nagle's algorithm).

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------------------|
| `on` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`to enable TCP_NODELAY,`false`to disable. |

| Exceptions ||
|----------------------------|-----------------------------------------------------------------------|
| `java.net.SocketException` | if there is an error in the underlying protocol, such as a TCP error. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/Socket#getTcpNoDelay()> 

### setTrafficClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTrafficClass(tc: Int): Unit
```

Sets traffic class or type-of-service octet in the IP header for packets sent from this Socket. As the underlying network implementation may ignore this value applications should consider it a hint.

The tc**must** be in the range`0 <= tc <= 255`or an IllegalArgumentException will be thrown.

Notes:

For Internet Protocol v4 the value consists of an`integer`, the least significant 8 bits of which represent the value of the TOS octet in IP packets sent by the socket. RFC 1349 defines the TOS values as follows:

- `IPTOS_LOWCOST (0x02)`
- `IPTOS_RELIABILITY (0x04)`
- `IPTOS_THROUGHPUT (0x08)`
- `IPTOS_LOWDELAY (0x10)`

The last low order bit is always ignored as this corresponds to the MBZ (must be zero) bit.

Setting bits in the precedence field may result in a SocketException indicating that the operation is not permitted.

As RFC 1122 section 4.2.4.2 indicates, a compliant TCP implementation should, but is not required to, let application change the TOS field during the lifetime of a connection. So whether the type-of-service field can be changed after the TCP connection has been established depends on the implementation in the underlying platform. Applications should not assume that they can change the TOS field after the connection.

For Internet Protocol v6`tc`is the value that would be placed into the sin6_flowinfo field of the IP header.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------|
| `tc` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an`int`value for the bitset. |

| Exceptions ||
|----------------------------|-------------------------------------------------------------------|
| `java.net.SocketException` | if there is an error setting the traffic class or type-of-service |

**See Also**

- [#getTrafficClass](Socket.md))
- [java.net.SocketOptions#IP_TOS](SocketOptions.md) 

### shutdownInput

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun shutdownInput(): Unit
```

Places the input stream for this socket at "end of stream". Any data sent to the input stream side of the socket is acknowledged and then silently discarded.

If you read from a socket input stream after invoking this method on the socket, the stream's`available`method will return 0, and its`read`methods will return`-1`(end of stream).

| Exceptions ||
|-----------------------|--------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs when shutting down this socket. |

**See Also**

- [java.net.Socket#shutdownOutput()](Socket.md))
- [java.net.Socket#setSoLinger(boolean, int)](Socket.md))
- [#isInputShutdown](Socket.md)) 

### shutdownOutput

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun shutdownOutput(): Unit
```

Disables the output stream for this socket. For a TCP socket, any previously written data will be sent followed by TCP's normal connection termination sequence. If you write to a socket output stream after invoking shutdownOutput() on the socket, the stream will throw an IOException.

| Exceptions ||
|-----------------------|--------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs when shutting down this socket. |

**See Also**

- [java.net.Socket#shutdownInput()](Socket.md))
- [java.net.Socket#setSoLinger(boolean, int)](Socket.md))
- [#isOutputShutdown](Socket.md)) 

### supportedOptions

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun supportedOptions(): MutableSet<SocketOption<*>!>!
```

Returns a set of the socket options supported by this socket. This method will continue to return the set of options even after the socket has been closed.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [SocketOption](SocketOption.md)<*>!>! | A set of the socket options supported by this socket. This set may be empty if the socket's SocketImpl cannot be created. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Converts this socket to a`String`.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of this socket. |
