# ServerSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ServerSocket

```
open class ServerSocket : Closeable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.net.ServerSocket](../java/net/ServerSocket.md) |

| Known Direct Subclasses [SSLServerSocket](../javax/net/ssl/SSLServerSocket.md) |-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [SSLServerSocket](../javax/net/ssl/SSLServerSocket.md) | This class extends`ServerSocket`s and provides secure server sockets using protocols such as the Secure Sockets Layer (SSL) or Transport Layer Security (TLS) protocols. | |
| --- | --- | --- | --- | --- | --- | --- |

This class implements server sockets. A server socket waits for requests to come in over the network. It performs some operation based on that request, and then possibly returns a result to the requester.

The actual work of the server socket is performed by an instance of the`SocketImpl`class. An application can change the socket factory that creates the socket implementation to configure itself to create sockets appropriate to the local firewall.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ServerSocket](../java/net/ServerSocket.md))`()` Creates an unbound server socket. |
| [ServerSocket](../java/net/ServerSocket.md))`(`port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a server socket, bound to the specified port. |
| [ServerSocket](../java/net/ServerSocket.md))`(`port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `backlog:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a server socket and binds it to the specified local port number, with the specified backlog. |
| [ServerSocket](../java/net/ServerSocket.md))`(`port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `backlog:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bindAddr:` ` [InetAddress](../java/net/InetAddress.md)!`)` Create a server with the specified port, listen backlog, and local IP address to bind to. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Socket](../java/net/Socket.md)! | [accept](../java/net/ServerSocket.md))`()` Listens for a connection to be made to this socket and accepts it. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bind](../java/net/ServerSocket.md))`(`endpoint:` ` [SocketAddress](../java/net/SocketAddress.md)!`)` Binds the`ServerSocket`to a specific address (IP address and port number). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bind](../java/net/ServerSocket.md))`(`endpoint:` ` [SocketAddress](../java/net/SocketAddress.md)!`, `backlog:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Binds the`ServerSocket`to a specific address (IP address and port number). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../java/net/ServerSocket.md))`()` Closes this socket. |
| open [ServerSocketChannel](../java/nio/channels/ServerSocketChannel.md)! | [getChannel](../java/net/ServerSocket.md))`()` Returns the unique [java.nio.channels.ServerSocketChannel](../java/nio/channels/ServerSocketChannel.md) object associated with this socket, if any. |
| open [InetAddress](../java/net/InetAddress.md)! | [getInetAddress](../java/net/ServerSocket.md))`()` Returns the local address of this server socket. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLocalPort](../java/net/ServerSocket.md))`()` Returns the port number on which this socket is listening. |
| open [SocketAddress](../java/net/SocketAddress.md)! | [getLocalSocketAddress](../java/net/ServerSocket.md))`()` Returns the address of the endpoint this socket is bound to. |
| openT | [getOption](../java/net/ServerSocket.md))`(`name:` ` [SocketOption](../java/net/SocketOption.md)<T>!`)` Returns the value of a socket option. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getReceiveBufferSize](../java/net/ServerSocket.md))`()` Gets the value of the [SO_RCVBUF](../java/net/SocketOptions.md) option for this`ServerSocket`, that is the proposed buffer size that will be used for Sockets accepted from this`ServerSocket`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getReuseAddress](../java/net/ServerSocket.md))`()` Tests if [SO_REUSEADDR](../java/net/SocketOptions.md) is enabled. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSoTimeout](../java/net/ServerSocket.md))`()` Retrieve setting for [SO_TIMEOUT](../java/net/SocketOptions.md). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBound](../java/net/ServerSocket.md))`()` Returns the binding state of the ServerSocket. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isClosed](../java/net/ServerSocket.md))`()` Returns the closed state of the ServerSocket. |
| open [ServerSocket](../java/net/ServerSocket.md)! | [setOption](../java/net/ServerSocket.md))`(`name:` ` [SocketOption](../java/net/SocketOption.md)<T>!`, `value:` `T`)` Sets the value of a socket option. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPerformancePreferences](../java/net/ServerSocket.md))`(`connectionTime:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `latency:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bandwidth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets performance preferences for this ServerSocket. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setReceiveBufferSize](../java/net/ServerSocket.md))`(`size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets a default proposed value for the [SO_RCVBUF](../java/net/SocketOptions.md) option for sockets accepted from this`ServerSocket`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setReuseAddress](../java/net/ServerSocket.md))`(`on:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Enable/disable the [SO_REUSEADDR](../java/net/SocketOptions.md) socket option. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSoTimeout](../java/net/ServerSocket.md))`(`timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Enable/disable [SO_TIMEOUT](../java/net/SocketOptions.md) with the specified timeout, in milliseconds. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSocketFactory](../java/net/ServerSocket.md))`(`fac:` ` [SocketImplFactory](../java/net/SocketImplFactory.md)!`)` Sets the server socket implementation factory for the application. |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [SocketOption](../java/net/SocketOption.md)\<\*\>!\>! | [supportedOptions](../java/net/ServerSocket.md))`()` Returns a set of the socket options supported by this server socket. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/net/ServerSocket.md))`()` Returns the implementation address and implementation port of this socket as a`String`. |

| Protected methods ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [implAccept](../java/net/ServerSocket.md))`(`s:` ` [Socket](../java/net/Socket.md)!`)` Subclasses of ServerSocket use this method to override accept() to return their own subclass of socket. |

## Public constructors

### ServerSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ServerSocket()
```

Creates an unbound server socket.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.io.IOException` | IO error when opening the socket. |

### ServerSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ServerSocket(port: Int)
```

Creates a server socket, bound to the specified port. A port number of`0`means that the port number is automatically allocated, typically from an ephemeral port range. This port number can then be retrieved by calling [getLocalPort](../java/net/ServerSocket.md)).

The maximum queue length for incoming connection indications (a request to connect) is set to`50`. If a connection indication arrives when the queue is full, the connection is refused.

If the application has specified a server socket factory, that factory's`createSocketImpl`method is called to create the actual socket implementation. Otherwise a "plain" socket is created.

If there is a security manager, its`checkListen`method is called with the`port`argument as its argument to ensure the operation is allowed. This could result in a SecurityException.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the port number, or`0`to use a port number that is automatically allocated. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs when opening the socket. |
| `java.lang.SecurityException` | if a security manager exists and its`checkListen`method doesn't allow the operation. |
| `java.lang.IllegalArgumentException` | if the port parameter is outside the specified range of valid port values, which is between 0 and 65535, inclusive. |
| --- | --- |

**See Also**

- [java.net.SocketImpl](../java/net/SocketImpl.md)
- [java.net.SocketImplFactory#createSocketImpl()](../java/net/SocketImplFactory.md))
- [java.net.ServerSocket#setSocketFactory(java.net.SocketImplFactory)](../java/net/ServerSocket.md))
- [java.lang.SecurityManager#checkListen](../java/lang/SecurityManager.md)) 

### ServerSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ServerSocket(
    port: Int, 
    backlog: Int)
```

Creates a server socket and binds it to the specified local port number, with the specified backlog. A port number of`0`means that the port number is automatically allocated, typically from an ephemeral port range. This port number can then be retrieved by calling [getLocalPort](../java/net/ServerSocket.md)).

The maximum queue length for incoming connection indications (a request to connect) is set to the`backlog`parameter. If a connection indication arrives when the queue is full, the connection is refused.

If the application has specified a server socket factory, that factory's`createSocketImpl`method is called to create the actual socket implementation. Otherwise a "plain" socket is created.

If there is a security manager, its`checkListen`method is called with the`port`argument as its argument to ensure the operation is allowed. This could result in a SecurityException. The`backlog`argument is the requested maximum number of pending connections on the socket. Its exact semantics are implementation specific. In particular, an implementation may impose a maximum length or may choose to ignore the parameter altogther. The value provided should be greater than`0`. If it is less than or equal to`0`, then an implementation specific default will be used.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the port number, or`0`to use a port number that is automatically allocated. |
| `backlog` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):requested maximum length of the queue of incoming connections. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs when opening the socket. |
| `java.lang.SecurityException` | if a security manager exists and its`checkListen`method doesn't allow the operation. |
| `java.lang.IllegalArgumentException` | if the port parameter is outside the specified range of valid port values, which is between 0 and 65535, inclusive. |
| --- | --- |

**See Also**

- [java.net.SocketImpl](../java/net/SocketImpl.md)
- [java.net.SocketImplFactory#createSocketImpl()](../java/net/SocketImplFactory.md))
- [java.net.ServerSocket#setSocketFactory(java.net.SocketImplFactory)](../java/net/ServerSocket.md))
- [java.lang.SecurityManager#checkListen](../java/lang/SecurityManager.md)) 

### ServerSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ServerSocket(
    port: Int, 
    backlog: Int, 
    bindAddr: InetAddress!)
```

Create a server with the specified port, listen backlog, and local IP address to bind to. The*bindAddr* argument can be used on a multi-homed host for a ServerSocket that will only accept connect requests to one of its addresses. If*bindAddr* is null, it will default accepting connections on any/all local addresses. The port must be between 0 and 65535, inclusive. A port number of`0`means that the port number is automatically allocated, typically from an ephemeral port range. This port number can then be retrieved by calling [getLocalPort](../java/net/ServerSocket.md)).

If there is a security manager, this method calls its`checkListen`method with the`port`argument as its argument to ensure the operation is allowed. This could result in a SecurityException. The`backlog`argument is the requested maximum number of pending connections on the socket. Its exact semantics are implementation specific. In particular, an implementation may impose a maximum length or may choose to ignore the parameter altogther. The value provided should be greater than`0`. If it is less than or equal to`0`, then an implementation specific default will be used.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the port number, or`0`to use a port number that is automatically allocated. |
| `backlog` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):requested maximum length of the queue of incoming connections. |
| `bindAddr` | [InetAddress](../java/net/InetAddress.md)!:the local InetAddress the server will bind to |
| --- | --- |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and its`checkListen`method doesn't allow the operation. |
| `java.io.IOException` | if an I/O error occurs when opening the socket. |
| `java.lang.IllegalArgumentException` | if the port parameter is outside the specified range of valid port values, which is between 0 and 65535, inclusive. |
| --- | --- |

**See Also**

- [java.net.SocketOptions](../java/net/SocketOptions.md)
- [java.net.SocketImpl](../java/net/SocketImpl.md)
- [java.lang.SecurityManager#checkListen](../java/lang/SecurityManager.md))

## Public methods

### accept

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun accept(): Socket!
```

Listens for a connection to be made to this socket and accepts it. The method blocks until a connection is made.

A new Socket`s`is created and, if there is a security manager, the security manager's`checkAccept`method is called with`s.getInetAddress().getHostAddress()`and`s.getPort()`as its arguments to ensure the operation is allowed. This could result in a SecurityException.

| Return ||
|---------------------------------------------------------------------------|----------------|
| [Socket](../java/net/Socket.md)! | the new Socket |

| Exceptions ||
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs when waiting for a connection. |
| `java.lang.SecurityException` | if a security manager exists and its`checkAccept`method doesn't allow the operation. |
| `java.net.SocketTimeoutException` | if a timeout was previously set with setSoTimeout and the timeout has been reached. |
| --- | --- |
| `java.nio.channels.IllegalBlockingModeException` | if this socket has an associated channel, the channel is in non-blocking mode, and there is no connection ready to be accepted |

**See Also**

- [java.lang.SecurityManager#checkAccept](../java/lang/SecurityManager.md)) 

### bind

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun bind(endpoint: SocketAddress!): Unit
```

Binds the`ServerSocket`to a specific address (IP address and port number).

If the address is`null`, then the system will pick up an ephemeral port and a valid local address to bind the socket.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------|
| `endpoint` | [SocketAddress](../java/net/SocketAddress.md)!:The IP address and port number to bind to. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------|
| `java.io.IOException` | if the bind operation fails, or if the socket is already bound. |
| `java.lang.SecurityException` | if a`SecurityManager`is present and its`checkListen`method doesn't allow the operation. |
| `java.lang.IllegalArgumentException` | if endpoint is a SocketAddress subclass not supported by this socket |
| --- | --- |

### bind

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun bind(
    endpoint: SocketAddress!, 
    backlog: Int
): Unit
```

Binds the`ServerSocket`to a specific address (IP address and port number).

If the address is`null`, then the system will pick up an ephemeral port and a valid local address to bind the socket.

The`backlog`argument is the requested maximum number of pending connections on the socket. Its exact semantics are implementation specific. In particular, an implementation may impose a maximum length or may choose to ignore the parameter altogther. The value provided should be greater than`0`. If it is less than or equal to`0`, then an implementation specific default will be used.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `endpoint` | [SocketAddress](../java/net/SocketAddress.md)!:The IP address and port number to bind to. |
| `backlog` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):requested maximum length of the queue of incoming connections. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------|
| `java.io.IOException` | if the bind operation fails, or if the socket is already bound. |
| `java.lang.SecurityException` | if a`SecurityManager`is present and its`checkListen`method doesn't allow the operation. |
| `java.lang.IllegalArgumentException` | if endpoint is a SocketAddress subclass not supported by this socket |
| --- | --- |

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Closes this socket. Any thread currently blocked in [accept()](../java/net/ServerSocket.md))will throw a [SocketException](../java/net/SocketException.md).

If this socket has an associated channel then the channel is closed as well.

| Exceptions ||
|-----------------------|-------------------------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs |
| `java.io.IOException` | if an I/O error occurs when closing the socket. |
| --- | --- |

### getChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getChannel(): ServerSocketChannel!
```

Returns the unique [java.nio.channels.ServerSocketChannel](../java/nio/channels/ServerSocketChannel.md) object associated with this socket, if any.

A server socket will have a channel if, and only if, the channel itself was created via the [ServerSocketChannel.open](../java/nio/channels/ServerSocketChannel.md))method.

| Return ||
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [ServerSocketChannel](../java/nio/channels/ServerSocketChannel.md)! | the server-socket channel associated with this socket, or`null`if this socket was not created for a channel |

### getInetAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInetAddress(): InetAddress!
```

Returns the local address of this server socket.

If the socket was bound prior to being #close, then this method will continue to return the local address after the socket is closed.

If there is a security manager set, its`checkConnect`method is called with the local address and`-1`as its arguments to see if the operation is allowed. If the operation is not allowed, the [loopback](../java/net/InetAddress.md))address is returned.

| Return ||
|-------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [InetAddress](../java/net/InetAddress.md)! | the address to which this socket is bound, or the loopback address if denied by the security manager, or`null`if the socket is unbound. |

**See Also**

### getLocalPort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLocalPort(): Int
```

Returns the port number on which this socket is listening.

If the socket was bound prior to being #close, then this method will continue to return the port number after the socket is closed.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the port number to which this socket is listening or -1 if the socket is not bound yet. |

### getLocalSocketAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLocalSocketAddress(): SocketAddress!
```

Returns the address of the endpoint this socket is bound to.

If the socket was bound prior to being #close, then this method will continue to return the address of the endpoint after the socket is closed.

If there is a security manager set, its`checkConnect`method is called with the local address and`-1`as its arguments to see if the operation is allowed. If the operation is not allowed, a`SocketAddress`representing the [loopback](../java/net/InetAddress.md))address and the local port to which the socket is bound is returned.

| Return ||
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SocketAddress](../java/net/SocketAddress.md)! | a`SocketAddress`representing the local endpoint of this socket, or a`SocketAddress`representing the loopback address if denied by the security manager, or`null`if the socket is not bound yet. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/ServerSocket#getInetAddress()>
- <https://developer.android.com/reference/kotlin/java/net/ServerSocket#getLocalPort()>
- [#bind(SocketAddress)](../java/net/ServerSocket.md)) 

### getOption

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Any!> getOption(name: SocketOption<T>!): T
```

Returns the value of a socket option.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------|
| `<T>` | The type of the socket option value |
| `name` | [SocketOption](../java/net/SocketOption.md)\<T\>!:The socket option |

| Return ||
|---|---------------------------------|
| T | The value of the socket option. |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the server socket does not support the option. |
| `java.io.IOException` | if an I/O error occurs, or if the socket is closed. |
| `java.lang.NullPointerException` | if name is`null` |
| --- | --- |
| `java.lang.SecurityException` | if a security manager is set and if the socket option requires a security permission and if the caller does not have the required permission. [StandardSocketOptions](../java/net/StandardSocketOptions.md) do not require any security permission. |

### getReceiveBufferSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getReceiveBufferSize(): Int
```

Gets the value of the [SO_RCVBUF](../java/net/SocketOptions.md) option for this`ServerSocket`, that is the proposed buffer size that will be used for Sockets accepted from this`ServerSocket`.

Note, the value actually set in the accepted socket is determined by calling [Socket.getReceiveBufferSize()](../java/net/Socket.md)).

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value of the [SO_RCVBUF](../java/net/SocketOptions.md) option for this`Socket`. |

| Exceptions ||
|----------------------------|-----------------------------------------------------------------------|
| `java.net.SocketException` | if there is an error in the underlying protocol, such as a TCP error. |

**See Also**

- [#setReceiveBufferSize(int)](../java/net/ServerSocket.md)) 

### getReuseAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getReuseAddress(): Boolean
```

Tests if [SO_REUSEADDR](../java/net/SocketOptions.md) is enabled.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a`boolean`indicating whether or not [SO_REUSEADDR](../java/net/SocketOptions.md) is enabled. |

| Exceptions ||
|----------------------------|-----------------------------------------------------------------------|
| `java.net.SocketException` | if there is an error in the underlying protocol, such as a TCP error. |

**See Also**

- [#setReuseAddress(boolean)](../java/net/ServerSocket.md)) 

### getSoTimeout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSoTimeout(): Int
```

Retrieve setting for [SO_TIMEOUT](../java/net/SocketOptions.md). 0 returns implies that the option is disabled (i.e., timeout of infinity).

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the [SO_TIMEOUT](../java/net/SocketOptions.md) value |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | if an I/O error occurs |

**See Also**

- [#setSoTimeout(int)](../java/net/ServerSocket.md)) 

### isBound

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isBound(): Boolean
```

Returns the binding state of the ServerSocket.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the ServerSocket successfully bound to an address |

### isClosed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isClosed(): Boolean
```

Returns the closed state of the ServerSocket.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the socket has been closed |

### setOption

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Any!> setOption(
    name: SocketOption<T>!, 
    value: T
): ServerSocket!
```

Sets the value of a socket option.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `<T>` | The type of the socket option value |
| `name` | [SocketOption](../java/net/SocketOption.md)\<T\>!:The socket option |
| `value` | T:The value of the socket option. A value of`null`may be valid for some options. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------|-------------------|
| [ServerSocket](../java/net/ServerSocket.md)! | this ServerSocket |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the server socket does not support the option. |
| `java.lang.IllegalArgumentException` | if the value is not valid for the option. |
| `java.io.IOException` | if an I/O error occurs, or if the socket is closed. |
| --- | --- |
| `java.lang.NullPointerException` | if name is`null` |
| `java.lang.SecurityException` | if a security manager is set and if the socket option requires a security permission and if the caller does not have the required permission. [StandardSocketOptions](../java/net/StandardSocketOptions.md) do not require any security permission. |

### setPerformancePreferences

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPerformancePreferences(
    connectionTime: Int, 
    latency: Int, 
    bandwidth: Int
): Unit
```

Sets performance preferences for this ServerSocket.

Sockets use the TCP/IP protocol by default. Some implementations may offer alternative protocols which have different performance characteristics than TCP/IP. This method allows the application to express its own preferences as to how these tradeoffs should be made when the implementation chooses from the available protocols.

Performance preferences are described by three integers whose values indicate the relative importance of short connection time, low latency, and high bandwidth. The absolute values of the integers are irrelevant; in order to choose a protocol the values are simply compared, with larger values indicating stronger preferences. If the application prefers short connection time over both low latency and high bandwidth, for example, then it could invoke this method with the values`(1, 0, 0)`. If the application prefers high bandwidth above low latency, and low latency above short connection time, then it could invoke this method with the values`(0, 1, 2)`.

Invoking this method after this socket has been bound will have no effect. This implies that in order to use this capability requires the socket to be created with the no-argument constructor.

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

Sets a default proposed value for the [SO_RCVBUF](../java/net/SocketOptions.md) option for sockets accepted from this`ServerSocket`. The value actually set in the accepted socket must be determined by calling [Socket.getReceiveBufferSize()](../java/net/Socket.md))after the socket is returned by [accept()](../java/net/ServerSocket.md)).

The value of [SO_RCVBUF](../java/net/SocketOptions.md) is used both to set the size of the internal socket receive buffer, and to set the size of the TCP receive window that is advertized to the remote peer.

It is possible to change the value subsequently, by calling [Socket.setReceiveBufferSize(int)](../java/net/Socket.md)). However, if the application wishes to allow a receive window larger than 64K bytes, as defined by RFC1323 then the proposed value must be set in the ServerSocket**before**it is bound to a local address. This implies, that the ServerSocket must be created with the no-argument constructor, then setReceiveBufferSize() must be called and lastly the ServerSocket is bound to an address by calling bind().

Failure to do this will not cause an error, and the buffer size may be set to the requested value but the TCP receive window in sockets accepted from this ServerSocket will be no larger than 64K bytes.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the size to which to set the receive buffer size. This value must be greater than 0. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------|
| `java.net.SocketException` | if there is an error in the underlying protocol, such as a TCP error. |
| `java.lang.IllegalArgumentException` | if the value is 0 or is negative. |

**See Also**

- [#getReceiveBufferSize](../java/net/ServerSocket.md)) 

### setReuseAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setReuseAddress(on: Boolean): Unit
```

Enable/disable the [SO_REUSEADDR](../java/net/SocketOptions.md) socket option.

When a TCP connection is closed the connection may remain in a timeout state for a period of time after the connection is closed (typically known as the`TIME_WAIT`state or`2MSL`wait state). For applications using a well known socket address or port it may not be possible to bind a socket to the required`SocketAddress`if there is a connection in the timeout state involving the socket address or port.

Enabling [SO_REUSEADDR](../java/net/SocketOptions.md) prior to binding the socket using [bind(java.net.SocketAddress)](../java/net/ServerSocket.md))allows the socket to be bound even though a previous connection is in a timeout state.

When a`ServerSocket`is created the initial setting of [SO_REUSEADDR](../java/net/SocketOptions.md) is not defined. Applications can use [getReuseAddress()](../java/net/ServerSocket.md))to determine the initial setting of [SO_REUSEADDR](../java/net/SocketOptions.md).

The behaviour when [SO_REUSEADDR](../java/net/SocketOptions.md) is enabled or disabled after a socket is bound (See [isBound()](../java/net/ServerSocket.md))) is not defined.

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------------------|
| `on` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether to enable or disable the socket option |

| Exceptions ||
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.net.SocketException` | if an error occurs enabling or disabling the [SO_REUSEADDR](../java/net/SocketOptions.md) socket option, or the socket is closed. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/ServerSocket#getReuseAddress()>
- [#bind(SocketAddress)](../java/net/ServerSocket.md))
- <https://developer.android.com/reference/kotlin/java/net/ServerSocket#isBound()>
- <https://developer.android.com/reference/kotlin/java/net/ServerSocket#isClosed()> 

### setSoTimeout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSoTimeout(timeout: Int): Unit
```

Enable/disable [SO_TIMEOUT](../java/net/SocketOptions.md) with the specified timeout, in milliseconds. With this option set to a non-zero timeout, a call to accept() for this ServerSocket will block for only this amount of time. If the timeout expires, a**java.net.SocketTimeoutException** is raised, though the ServerSocket is still valid. The option**must** be enabled prior to entering the blocking operation to have effect. The timeout must be`> 0`. A timeout of zero is interpreted as an infinite timeout.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the specified timeout, in milliseconds |

| Exceptions ||
|----------------------------|-----------------------------------------------------------------------|
| `java.net.SocketException` | if there is an error in the underlying protocol, such as a TCP error. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/ServerSocket#getSoTimeout()> 

### setSocketFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun setSocketFactory(fac: SocketImplFactory!): Unit
```

Sets the server socket implementation factory for the application. The factory can be specified only once.

When an application creates a new server socket, the socket implementation factory's`createSocketImpl`method is called to create the actual socket implementation.

Passing`null`to the method is a no-op unless the factory was already set.

If there is a security manager, this method first calls the security manager's`checkSetFactory`method to ensure the operation is allowed. This could result in a SecurityException.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------|
| `fac` | [SocketImplFactory](../java/net/SocketImplFactory.md)!:the desired factory. |

| Exceptions ||
|-------------------------------|------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs when setting the socket factory. |
| `java.net.SocketException` | if the factory has already been defined. |
| `java.lang.SecurityException` | if a security manager exists and its`checkSetFactory`method doesn't allow the operation. |
| --- | --- |

**See Also**

- [java.net.SocketImplFactory#createSocketImpl()](../java/net/SocketImplFactory.md))
- [java.lang.SecurityManager#checkSetFactory](../java/lang/SecurityManager.md)) 

### supportedOptions

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun supportedOptions(): MutableSet<SocketOption<*>!>!
```

Returns a set of the socket options supported by this server socket. This method will continue to return the set of options even after the socket has been closed.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [SocketOption](../java/net/SocketOption.md)<*>!>! | A set of the socket options supported by this socket. This set may be empty if the socket's SocketImpl cannot be created. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns the implementation address and implementation port of this socket as a`String`.

If there is a security manager set, its`checkConnect`method is called with the local address and`-1`as its arguments to see if the operation is allowed. If the operation is not allowed, an`InetAddress`representing the [loopback](../java/net/InetAddress.md))address is returned as the implementation address.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of this socket. |

## Protected methods

### implAccept

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun implAccept(s: Socket!): Unit
```

Subclasses of ServerSocket use this method to override accept() to return their own subclass of socket. So a FooServerSocket will typically hand this method an*empty*FooSocket. On return from implAccept the FooSocket will be connected to a client.

| Parameters ||
|-----|--------------------------------------------------------------------------------------|
| `s` | [Socket](../java/net/Socket.md)!:the Socket |

| Exceptions ||
|--------------------------------------------------|-----------------------------------------------------------------------------------|
| `java.nio.channels.IllegalBlockingModeException` | if this socket has an associated channel, and the channel is in non-blocking mode |
| `java.io.IOException` | if an I/O error occurs when waiting for a connection. |
