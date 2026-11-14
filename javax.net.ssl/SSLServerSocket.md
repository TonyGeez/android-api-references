# SSLServerSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SSLServerSocket

```
abstract class SSLServerSocket : ServerSocket
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [java.net.ServerSocket](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#) ||
| | ↳ | [javax.net.ssl.SSLServerSocket](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#) |

This class extends`ServerSocket`s and provides secure server sockets using protocols such as the Secure Sockets Layer (SSL) or Transport Layer Security (TLS) protocols.

Instances of this class are generally created using a`SSLServerSocketFactory`. The primary function of`SSLServerSocket`s is to create`SSLSocket`s by`accept`ing connections.

`SSLServerSocket`s contain several pieces of state data which are inherited by the`SSLSocket`at socket creation. These include the enabled cipher suites and protocols, whether client authentication is necessary, and whether created sockets should begin handshaking in client or server mode. The state inherited by the created`SSLSocket`can be overriden by calling the appropriate methods.

## Summary

| Protected constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SSLServerSocket](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#SSLServerSocket())`()` Used only by subclasses. |
| [SSLServerSocket](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#SSLServerSocket(kotlin.Int))`(`port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Used only by subclasses. |
| [SSLServerSocket](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#SSLServerSocket(kotlin.Int,%20kotlin.Int))`(`port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `backlog:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Used only by subclasses. |
| [SSLServerSocket](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#SSLServerSocket(kotlin.Int,%20kotlin.Int,%20java.net.InetAddress))`(`port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `backlog:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `address:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!`)` Used only by subclasses. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getEnableSessionCreation](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#getEnableSessionCreation())`()` Returns true if new SSL sessions may be established by the sockets which are created from this server socket. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getEnabledCipherSuites](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#getEnabledCipherSuites())`()` Returns the list of cipher suites which are currently enabled for use by newly accepted connections. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getEnabledProtocols](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#getEnabledProtocols())`()` Returns the names of the protocols which are currently enabled for use by the newly accepted connections. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getNeedClientAuth](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#getNeedClientAuth())`()` Returns true if client authentication will be*required* on newly`accept`ed server-mode`SSLSocket`s. |
| open [SSLParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters)! | [getSSLParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#getSSLParameters())`()` Returns the SSLParameters in effect for newly accepted connections. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getSupportedCipherSuites](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#getSupportedCipherSuites())`()` Returns the names of the cipher suites which could be enabled for use on an SSL connection. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getSupportedProtocols](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#getSupportedProtocols())`()` Returns the names of the protocols which could be enabled for use. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getUseClientMode](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#getUseClientMode())`()` Returns true if accepted connections will be in SSL client mode. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getWantClientAuth](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#getWantClientAuth())`()` Returns true if client authentication will be*requested*on newly accepted server-mode connections. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEnableSessionCreation](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#setEnableSessionCreation(kotlin.Boolean))`(`flag:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Controls whether new SSL sessions may be established by the sockets which are created from this server socket. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEnabledCipherSuites](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#setEnabledCipherSuites(kotlin.Array))`(`suites:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Sets the cipher suites enabled for use by accepted connections. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEnabledProtocols](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#setEnabledProtocols(kotlin.Array))`(`protocols:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Controls which particular protocols are enabled for use by accepted connections. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNeedClientAuth](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#setNeedClientAuth(kotlin.Boolean))`(`need:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Controls whether`accept`ed server-mode`SSLSockets`will be initially configured to*require*client authentication. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSSLParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#setSSLParameters(javax.net.ssl.SSLParameters))`(`params:` ` [SSLParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters)!`)` Applies SSLParameters to newly accepted connections. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUseClientMode](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#setUseClientMode(kotlin.Boolean))`(`mode:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Controls whether accepted connections are in the (default) SSL server mode, or the SSL client mode. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setWantClientAuth](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#setWantClientAuth(kotlin.Boolean))`(`want:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Controls whether`accept`ed server-mode`SSLSockets`will be initially configured to*request*client authentication. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#toString())`()` <br /> |

| Inherited functions ||
|---|---|
| From class [ServerSocket](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#) |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | [accept](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#accept())`()` <br /> Listens for a connection to be made to this socket and accepts it. The method blocks until a connection is made. A new Socket`s`is created and, if there is a security manager, the security manager's`checkAccept`method is called with`s.getInetAddress().getHostAddress()`and`s.getPort()`as its arguments to ensure the operation is allowed. This could result in a SecurityException. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bind](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#bind(java.net.SocketAddress))`(`endpoint:` ` [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#)!`)` <br /> Binds the`ServerSocket`to a specific address (IP address and port number). If the address is`null`, then the system will pick up an ephemeral port and a valid local address to bind the socket. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bind](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#bind(java.net.SocketAddress,%20kotlin.Int))`(`endpoint:` ` [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#)!`, `backlog:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Binds the`ServerSocket`to a specific address (IP address and port number). If the address is`null`, then the system will pick up an ephemeral port and a valid local address to bind the socket. The`backlog`argument is the requested maximum number of pending connections on the socket. Its exact semantics are implementation specific. In particular, an implementation may impose a maximum length or may choose to ignore the parameter altogther. The value provided should be greater than`0`. If it is less than or equal to`0`, then an implementation specific default will be used. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#close())`()` <br /> Closes this socket. Any thread currently blocked in [accept()](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#accept())will throw a [SocketException](https://developer.android.com/reference/kotlin/java/net/SocketException.html#). If this socket has an associated channel then the channel is closed as well. <br /> | | [ServerSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel.html#)! | [getChannel](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#getChannel())`()` <br /> Returns the unique [java.nio.channels.ServerSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel.html#) object associated with this socket, if any. A server socket will have a channel if, and only if, the channel itself was created via the [ServerSocketChannel.open](https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel.html#open())method. <br /> | | [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)! | [getInetAddress](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#getInetAddress())`()` <br /> Returns the local address of this server socket. If the socket was bound prior to being #close, then this method will continue to return the local address after the socket is closed. If there is a security manager set, its`checkConnect`method is called with the local address and`-1`as its arguments to see if the operation is allowed. If the operation is not allowed, the [loopback](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#getLoopbackAddress())address is returned. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLocalPort](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#getLocalPort())`()` <br /> Returns the port number on which this socket is listening. If the socket was bound prior to being #close, then this method will continue to return the port number after the socket is closed. <br /> | | [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#)! | [getLocalSocketAddress](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#getLocalSocketAddress())`()` <br /> Returns the address of the endpoint this socket is bound to. If the socket was bound prior to being #close, then this method will continue to return the address of the endpoint after the socket is closed. If there is a security manager set, its`checkConnect`method is called with the local address and`-1`as its arguments to see if the operation is allowed. If the operation is not allowed, a`SocketAddress`representing the [loopback](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#getLoopbackAddress())address and the local port to which the socket is bound is returned. <br /> | | T | [getOption](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#getOption(java.net.SocketOption))`(`name:` ` [SocketOption](https://developer.android.com/reference/kotlin/java/net/SocketOption.html#)<T>!`)` <br /> Returns the value of a socket option. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getReceiveBufferSize](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#getReceiveBufferSize())`()` <br /> Gets the value of the [SO_RCVBUF](https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#SO_RCVBUF:kotlin.Int) option for this`ServerSocket`, that is the proposed buffer size that will be used for Sockets accepted from this`ServerSocket`. Note, the value actually set in the accepted socket is determined by calling [Socket.getReceiveBufferSize()](https://developer.android.com/reference/kotlin/java/net/Socket.html#getReceiveBufferSize()). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getReuseAddress](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#getReuseAddress())`()` <br /> Tests if [SO_REUSEADDR](https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#SO_REUSEADDR:kotlin.Int) is enabled. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSoTimeout](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#getSoTimeout())`()` <br /> Retrieve setting for [SO_TIMEOUT](https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#SO_TIMEOUT:kotlin.Int). 0 returns implies that the option is disabled (i.e., timeout of infinity). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [implAccept](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#implAccept(java.net.Socket))`(`s:` ` [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)!`)` <br /> Subclasses of ServerSocket use this method to override accept() to return their own subclass of socket. So a FooServerSocket will typically hand this method an*empty*FooSocket. On return from implAccept the FooSocket will be connected to a client. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBound](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#isBound())`()` <br /> Returns the binding state of the ServerSocket. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isClosed](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#isClosed())`()` <br /> Returns the closed state of the ServerSocket. <br /> | | [ServerSocket](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#)! | [setOption](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#setOption(java.net.SocketOption,%20java.net.ServerSocket.setOption.T))`(`name:` ` [SocketOption](https://developer.android.com/reference/kotlin/java/net/SocketOption.html#)<T>!`, `value:` `T`)` <br /> Sets the value of a socket option. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPerformancePreferences](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#setPerformancePreferences(kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`connectionTime:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `latency:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bandwidth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets performance preferences for this ServerSocket. Sockets use the TCP/IP protocol by default. Some implementations may offer alternative protocols which have different performance characteristics than TCP/IP. This method allows the application to express its own preferences as to how these tradeoffs should be made when the implementation chooses from the available protocols. Performance preferences are described by three integers whose values indicate the relative importance of short connection time, low latency, and high bandwidth. The absolute values of the integers are irrelevant; in order to choose a protocol the values are simply compared, with larger values indicating stronger preferences. If the application prefers short connection time over both low latency and high bandwidth, for example, then it could invoke this method with the values`(1, 0, 0)`. If the application prefers high bandwidth above low latency, and low latency above short connection time, then it could invoke this method with the values`(0, 1, 2)`. Invoking this method after this socket has been bound will have no effect. This implies that in order to use this capability requires the socket to be created with the no-argument constructor. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setReceiveBufferSize](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#setReceiveBufferSize(kotlin.Int))`(`size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets a default proposed value for the [SO_RCVBUF](https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#SO_RCVBUF:kotlin.Int) option for sockets accepted from this`ServerSocket`. The value actually set in the accepted socket must be determined by calling [Socket.getReceiveBufferSize()](https://developer.android.com/reference/kotlin/java/net/Socket.html#getReceiveBufferSize())after the socket is returned by [accept()](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#accept()). The value of [SO_RCVBUF](https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#SO_RCVBUF:kotlin.Int) is used both to set the size of the internal socket receive buffer, and to set the size of the TCP receive window that is advertized to the remote peer. It is possible to change the value subsequently, by calling [Socket.setReceiveBufferSize(int)](https://developer.android.com/reference/kotlin/java/net/Socket.html#setReceiveBufferSize(kotlin.Int)). However, if the application wishes to allow a receive window larger than 64K bytes, as defined by RFC1323 then the proposed value must be set in the ServerSocket**before**it is bound to a local address. This implies, that the ServerSocket must be created with the no-argument constructor, then setReceiveBufferSize() must be called and lastly the ServerSocket is bound to an address by calling bind(). Failure to do this will not cause an error, and the buffer size may be set to the requested value but the TCP receive window in sockets accepted from this ServerSocket will be no larger than 64K bytes. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setReuseAddress](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#setReuseAddress(kotlin.Boolean))`(`on:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Enable/disable the [SO_REUSEADDR](https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#SO_REUSEADDR:kotlin.Int) socket option. When a TCP connection is closed the connection may remain in a timeout state for a period of time after the connection is closed (typically known as the`TIME_WAIT`state or`2MSL`wait state). For applications using a well known socket address or port it may not be possible to bind a socket to the required`SocketAddress`if there is a connection in the timeout state involving the socket address or port. Enabling [SO_REUSEADDR](https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#SO_REUSEADDR:kotlin.Int) prior to binding the socket using [bind(java.net.SocketAddress)](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#bind(java.net.SocketAddress))allows the socket to be bound even though a previous connection is in a timeout state. When a`ServerSocket`is created the initial setting of [SO_REUSEADDR](https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#SO_REUSEADDR:kotlin.Int) is not defined. Applications can use [getReuseAddress()](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#getReuseAddress())to determine the initial setting of [SO_REUSEADDR](https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#SO_REUSEADDR:kotlin.Int). The behaviour when [SO_REUSEADDR](https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#SO_REUSEADDR:kotlin.Int) is enabled or disabled after a socket is bound (See [isBound()](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#isBound())) is not defined. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSoTimeout](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#setSoTimeout(kotlin.Int))`(`timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Enable/disable [SO_TIMEOUT](https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#SO_TIMEOUT:kotlin.Int) with the specified timeout, in milliseconds. With this option set to a non-zero timeout, a call to accept() for this ServerSocket will block for only this amount of time. If the timeout expires, a**java.net.SocketTimeoutException** is raised, though the ServerSocket is still valid. The option**must** be enabled prior to entering the blocking operation to have effect. The timeout must be`> 0`. A timeout of zero is interpreted as an infinite timeout. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSocketFactory](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#setSocketFactory(java.net.SocketImplFactory))`(`fac:` ` [SocketImplFactory](https://developer.android.com/reference/kotlin/java/net/SocketImplFactory.html#)!`)` <br /> Sets the server socket implementation factory for the application. The factory can be specified only once. When an application creates a new server socket, the socket implementation factory's`createSocketImpl`method is called to create the actual socket implementation. Passing`null`to the method is a no-op unless the factory was already set. If there is a security manager, this method first calls the security manager's`checkSetFactory`method to ensure the operation is allowed. This could result in a SecurityException. <br /> | | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [SocketOption](https://developer.android.com/reference/kotlin/java/net/SocketOption.html#)<*>!>! | [supportedOptions](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#supportedOptions())`()` <br /> Returns a set of the socket options supported by this server socket. This method will continue to return the set of options even after the socket has been closed. <br /> | ||

## Protected constructors

### SSLServerSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected SSLServerSocket()
```

Used only by subclasses.

Create an unbound TCP server socket using the default authentication context.

| Exceptions ||
|-----------------------|-------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs when creating the socket |

### SSLServerSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected SSLServerSocket(port: Int)
```

Used only by subclasses.

Create a TCP server socket on a port, using the default authentication context. The connection backlog defaults to fifty connections queued up before the system starts to reject new connection requests.

A port number of`0`creates a socket on any free port.

If there is a security manager, its`checkListen`method is called with the`port`argument as its argument to ensure the operation is allowed. This could result in a SecurityException.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------|
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the port on which to listen |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs when creating the socket |
| `java.lang.SecurityException` | if a security manager exists and its`checkListen`method doesn't allow the operation. |
| `java.lang.IllegalArgumentException` | if the port parameter is outside the specified range of valid port values, which is between 0 and 65535, inclusive. |

**See Also**

- [java.lang.SecurityManager#checkListen](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkListen(kotlin.Int)) 

### SSLServerSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected SSLServerSocket(
    port: Int, 
    backlog: Int)
```

Used only by subclasses.

Create a TCP server socket on a port, using the default authentication context and a specified backlog of connections.

A port number of`0`creates a socket on any free port.

The`backlog`argument is the requested maximum number of pending connections on the socket. Its exact semantics are implementation specific. In particular, an implementation may impose a maximum length or may choose to ignore the parameter altogther. The value provided should be greater than`0`. If it is less than or equal to`0`, then an implementation specific default will be used.

If there is a security manager, its`checkListen`method is called with the`port`argument as its argument to ensure the operation is allowed. This could result in a SecurityException.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the port on which to listen |
| `backlog` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):requested maximum length of the queue of incoming connections. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs when creating the socket |
| `java.lang.SecurityException` | if a security manager exists and its`checkListen`method doesn't allow the operation. |
| `java.lang.IllegalArgumentException` | if the port parameter is outside the specified range of valid port values, which is between 0 and 65535, inclusive. |

**See Also**

- [java.lang.SecurityManager#checkListen](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkListen(kotlin.Int)) 

### SSLServerSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected SSLServerSocket(
    port: Int, 
    backlog: Int, 
    address: InetAddress!)
```

Used only by subclasses.

Create a TCP server socket on a port, using the default authentication context and a specified backlog of connections as well as a particular specified network interface. This constructor is used on multihomed hosts, such as those used for firewalls or as routers, to control through which interface a network service is provided.

If there is a security manager, its`checkListen`method is called with the`port`argument as its argument to ensure the operation is allowed. This could result in a SecurityException.

A port number of`0`creates a socket on any free port.

The`backlog`argument is the requested maximum number of pending connections on the socket. Its exact semantics are implementation specific. In particular, an implementation may impose a maximum length or may choose to ignore the parameter altogther. The value provided should be greater than`0`. If it is less than or equal to`0`, then an implementation specific default will be used.

If*address*is null, it will default accepting connections on any/all local addresses.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the port on which to listen |
| `backlog` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):requested maximum length of the queue of incoming connections. |
| `address` | [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!:the address of the network interface through which connections will be accepted |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs when creating the socket |
| `java.lang.SecurityException` | if a security manager exists and its`checkListen`method doesn't allow the operation. |
| `java.lang.IllegalArgumentException` | if the port parameter is outside the specified range of valid port values, which is between 0 and 65535, inclusive. |

**See Also**

- [java.lang.SecurityManager#checkListen](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkListen(kotlin.Int))

## Public methods

### getEnableSessionCreation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getEnableSessionCreation(): Boolean
```

Returns true if new SSL sessions may be established by the sockets which are created from this server socket.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true indicates that sessions may be created; this is the default. false indicates that an existing session must be resumed |

**See Also**

- [#setEnableSessionCreation(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#setEnableSessionCreation(kotlin.Boolean)) 

### getEnabledCipherSuites

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getEnabledCipherSuites(): Array<String!>!
```

Returns the list of cipher suites which are currently enabled for use by newly accepted connections.

If this list has not been explicitly modified, a system-provided default guarantees a minimum quality of service in all enabled cipher suites.

There are several reasons why an enabled cipher suite might not actually be used. For example: the server socket might not have appropriate private keys available to it or the cipher suite might be anonymous, precluding the use of client authentication, while the server socket has been told to require that sort of authentication.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | an array of cipher suites enabled |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#getSupportedCipherSuites()> 

### getEnabledProtocols

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getEnabledProtocols(): Array<String!>!
```

Returns the names of the protocols which are currently enabled for use by the newly accepted connections.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | an array of protocol names |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#getSupportedProtocols()> 

### getNeedClientAuth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getNeedClientAuth(): Boolean
```

Returns true if client authentication will be*required* on newly`accept`ed server-mode`SSLSocket`s.

The initial inherited setting may be overridden by calling [SSLSocket.setNeedClientAuth(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setNeedClientAuth(kotlin.Boolean))or [SSLSocket.setWantClientAuth(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setWantClientAuth(kotlin.Boolean)).

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if client authentication is required, or false if no client authentication is desired. |

**See Also**

- [#setNeedClientAuth(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#setNeedClientAuth(kotlin.Boolean))
- [#setWantClientAuth(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#setWantClientAuth(kotlin.Boolean))
- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#getWantClientAuth()>
- [#setUseClientMode(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#setUseClientMode(kotlin.Boolean)) 

### getSSLParameters

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSSLParameters(): SSLParameters!
```

Returns the SSLParameters in effect for newly accepted connections. The ciphersuites and protocols of the returned SSLParameters are always non-null.

| Return ||
|----------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [SSLParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters)! | the SSLParameters in effect for newly accepted connections |

**See Also**

- [#setSSLParameters(SSLParameters)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#setSSLParameters(javax.net.ssl.SSLParameters)) 

### getSupportedCipherSuites

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSupportedCipherSuites(): Array<String!>!
```

Returns the names of the cipher suites which could be enabled for use on an SSL connection.

Normally, only a subset of these will actually be enabled by default, since this list may include cipher suites which do not meet quality of service requirements for those defaults. Such cipher suites are useful in specialized applications.

Applications should not blindly enable all supported cipher suites. The supported cipher suites can include signaling cipher suite values that can cause connection problems if enabled inappropriately.

The proper way to use this method is to either check if a specific cipher suite is supported via`Arrays.asList(getSupportedCipherSuites()).contains(...)`or to filter a desired list of cipher suites to only the supported ones via`desiredSuiteSet.retainAll(Arrays.asList(getSupportedCipherSuites()))`.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | an array of cipher suite names |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#getEnabledCipherSuites()> 

### getSupportedProtocols

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSupportedProtocols(): Array<String!>!
```

Returns the names of the protocols which could be enabled for use.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | an array of protocol names supported |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#getEnabledProtocols()> 

### getUseClientMode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getUseClientMode(): Boolean
```

Returns true if accepted connections will be in SSL client mode.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the connection should use SSL client mode. |

**See Also**

- [#setUseClientMode(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#setUseClientMode(kotlin.Boolean)) 

### getWantClientAuth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getWantClientAuth(): Boolean
```

Returns true if client authentication will be*requested*on newly accepted server-mode connections.

The initial inherited setting may be overridden by calling [SSLSocket.setNeedClientAuth(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setNeedClientAuth(kotlin.Boolean))or [SSLSocket.setWantClientAuth(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setWantClientAuth(kotlin.Boolean)).

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if client authentication is requested, or false if no client authentication is desired. |

**See Also**

- [#setWantClientAuth(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#setWantClientAuth(kotlin.Boolean))
- [#setNeedClientAuth(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#setNeedClientAuth(kotlin.Boolean))
- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#getNeedClientAuth()>
- [#setUseClientMode(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#setUseClientMode(kotlin.Boolean)) 

### setEnableSessionCreation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setEnableSessionCreation(flag: Boolean): Unit
```

Controls whether new SSL sessions may be established by the sockets which are created from this server socket.

`SSLSocket`s returned from`accept()`inherit this setting.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `flag` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true indicates that sessions may be created; this is the default. false indicates that an existing session must be resumed. |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#getEnableSessionCreation()> 

### setEnabledCipherSuites

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setEnabledCipherSuites(suites: Array<String!>!): Unit
```

Sets the cipher suites enabled for use by accepted connections.

The cipher suites must have been listed by getSupportedCipherSuites() as being supported. Following a successful call to this method, only suites listed in the`suites`parameter are enabled for use.

Suites that require authentication information which is not available in this ServerSocket's authentication context will not be used in any case, even if they are enabled.

`SSLSocket`s returned from`accept()`inherit this setting.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `suites` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:Names of all the cipher suites to enable |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | when one or more of ciphers named by the parameter is not supported, or when the parameter is null. |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#getSupportedCipherSuites()>
- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#getEnabledCipherSuites()> 

### setEnabledProtocols

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setEnabledProtocols(protocols: Array<String!>!): Unit
```

Controls which particular protocols are enabled for use by accepted connections.

The protocols must have been listed by getSupportedProtocols() as being supported. Following a successful call to this method, only protocols listed in the`protocols`parameter are enabled for use.

Because of the way the protocol version is negotiated, connections will only be able to use a member of the lowest set of contiguous enabled protocol versions. For example, enabling TLSv1.2 and TLSv1 will result in connections only being able to use TLSv1.

`SSLSocket`s returned from`accept()`inherit this setting.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `protocols` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:Names of all the protocols to enable. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | when one or more of the protocols named by the parameter is not supported or when the protocols parameter is null. |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#getEnabledProtocols()>
- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#getSupportedProtocols()> 

### setNeedClientAuth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setNeedClientAuth(need: Boolean): Unit
```

Controls whether`accept`ed server-mode`SSLSockets`will be initially configured to*require*client authentication.

A socket's client authentication setting is one of the following:

- client authentication required
- client authentication requested
- no client authentication desired

Unlike [setWantClientAuth(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#setWantClientAuth(kotlin.Boolean)), if the accepted socket's option is set and the client chooses not to provide authentication information about itself,*the negotiations will stop and the connection will be dropped*.

Calling this method overrides any previous setting made by this method or [setWantClientAuth(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#setWantClientAuth(kotlin.Boolean)).

The initial inherited setting may be overridden by calling [SSLSocket.setNeedClientAuth(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setNeedClientAuth(kotlin.Boolean))or [SSLSocket.setWantClientAuth(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setWantClientAuth(kotlin.Boolean)).

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `need` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):set to true if client authentication is required, or false if no client authentication is desired. |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#getNeedClientAuth()>
- [#setWantClientAuth(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#setWantClientAuth(kotlin.Boolean))
- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#getWantClientAuth()>
- [#setUseClientMode(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#setUseClientMode(kotlin.Boolean)) 

### setSSLParameters

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSSLParameters(params: SSLParameters!): Unit
```

Applies SSLParameters to newly accepted connections.

This means:

- If`params.getCipherSuites()`is non-null,`setEnabledCipherSuites()`is called with that value.
- If`params.getProtocols()`is non-null,`setEnabledProtocols()`is called with that value.
- If`params.getNeedClientAuth()`or`params.getWantClientAuth()`return`true`,`setNeedClientAuth(true)`and`setWantClientAuth(true)`are called, respectively; otherwise`setWantClientAuth(false)`is called.
- If`params.getServerNames()`is non-null, the socket will configure its server names with that value.
- If`params.getSNIMatchers()`is non-null, the socket will configure its SNI matchers with that value.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------|
| `params` | [SSLParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters)!:the parameters |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the setEnabledCipherSuites() or the setEnabledProtocols() call fails |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#getSSLParameters()> 

### setUseClientMode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setUseClientMode(mode: Boolean): Unit
```

Controls whether accepted connections are in the (default) SSL server mode, or the SSL client mode.

Servers normally authenticate themselves, and clients are not required to do so.

In rare cases, TCP servers need to act in the SSL client mode on newly accepted connections. For example, FTP clients acquire server sockets and listen there for reverse connections from the server. An FTP client would use an SSLServerSocket in "client" mode to accept the reverse connection while the FTP server uses an SSLSocket with "client" mode disabled to initiate the connection. During the resulting handshake, existing SSL sessions may be reused.

`SSLSocket`s returned from`accept()`inherit this setting.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if newly accepted connections should use SSL client mode. |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#getUseClientMode()> 

### setWantClientAuth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setWantClientAuth(want: Boolean): Unit
```

Controls whether`accept`ed server-mode`SSLSockets`will be initially configured to*request*client authentication.

A socket's client authentication setting is one of the following:

- client authentication required
- client authentication requested
- no client authentication desired

Unlike [setNeedClientAuth(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#setNeedClientAuth(kotlin.Boolean)), if the accepted socket's option is set and the client chooses not to provide authentication information about itself,*the negotiations will continue*.

Calling this method overrides any previous setting made by this method or [setNeedClientAuth(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#setNeedClientAuth(kotlin.Boolean)).

The initial inherited setting may be overridden by calling [SSLSocket.setNeedClientAuth(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setNeedClientAuth(kotlin.Boolean))or [SSLSocket.setWantClientAuth(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setWantClientAuth(kotlin.Boolean)).

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `want` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):set to true if client authentication is requested, or false if no client authentication is desired. |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#getWantClientAuth()>
- [#setNeedClientAuth(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#setNeedClientAuth(kotlin.Boolean))
- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#getNeedClientAuth()>
- [#setUseClientMode(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#setUseClientMode(kotlin.Boolean)) 

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of this socket. |
