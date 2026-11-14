# SocketFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SocketFactory

```
abstract class SocketFactory
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.net.SocketFactory](../javax/net/SocketFactory.md) |

| Known Direct Subclasses [SSLSocketFactory](../javax/net/ssl/SSLSocketFactory.md) |---------------------------------------------------------------------------------------------------|-----------------------------------------| | [SSLSocketFactory](../javax/net/ssl/SSLSocketFactory.md) | `SSLSocketFactory`s create`SSLSocket`s. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [SSLCertificateSocketFactory](../android/net/SSLCertificateSocketFactory.md) |-----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [SSLCertificateSocketFactory](../android/net/SSLCertificateSocketFactory.md) | SSLSocketFactory implementation with several extra features: - Timeout specification for SSL handshake operations - Hostname verification in most cases (see WARNINGs below) - Optional SSL session caching with [SSLSessionCache](../android/net/SSLSessionCache.md) - Optionally bypass all SSL certificate checks The handshake timeout does not apply to actual TCP socket connection. <br /> | |
| --- | --- | --- | --- | --- | --- | --- |

This class creates sockets. It may be subclassed by other factories, which create particular subclasses of sockets and thus provide a general framework for the addition of public socket-level functionality.

Socket factories are a simple way to capture a variety of policies related to the sockets being constructed, producing such sockets in a way which does not require special configuration of the code which asks for the sockets:

- Due to polymorphism of both factories and sockets, different kinds of sockets can be used by the same application code just by passing it different kinds of factories.
- Factories can themselves be customized with parameters used in socket construction. So for example, factories could be customized to return sockets with different networking timeouts or security parameters already configured.
- The sockets returned to the application can be subclasses of java.net.Socket, so that they can directly expose new APIs for features such as compression, security, record marking, statistics collection, or firewall tunneling.

Factory classes are specified by environment-specific configuration mechanisms. For example, the*getDefault*method could return a factory that was appropriate for a particular user or applet, and a framework could use a factory customized to its own purposes.

## Summary

| Protected constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------|---|
| [SocketFactory](../javax/net/SocketFactory.md))`()` Creates a`SocketFactory`. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Socket](../java/net/Socket.md)! | [createSocket](../javax/net/SocketFactory.md))`()` Creates an unconnected socket. |
| abstract [Socket](../java/net/Socket.md)! | [createSocket](../javax/net/SocketFactory.md))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a socket and connects it to the specified remote host at the specified remote port. |
| abstract [Socket](../java/net/Socket.md)! | [createSocket](../javax/net/SocketFactory.md))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `localHost:` ` [InetAddress](../java/net/InetAddress.md)!`, `localPort:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a socket and connects it to the specified remote host on the specified remote port. |
| --- | --- |
| abstract [Socket](../java/net/Socket.md)! | [createSocket](../javax/net/SocketFactory.md))`(`host:` ` [InetAddress](../java/net/InetAddress.md)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a socket and connects it to the specified port number at the specified address. |
| abstract [Socket](../java/net/Socket.md)! | [createSocket](../javax/net/SocketFactory.md))`(`address:` ` [InetAddress](../java/net/InetAddress.md)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `localAddress:` ` [InetAddress](../java/net/InetAddress.md)!`, `localPort:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a socket and connect it to the specified remote address on the specified remote port. |
| openstatic [SocketFactory](../javax/net/SocketFactory.md)! | [getDefault](../javax/net/SocketFactory.md))`()` Returns a copy of the environment's default socket factory. |
| --- | --- |

## Protected constructors

### SocketFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected SocketFactory()
```

Creates a`SocketFactory`.

## Public methods

### createSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createSocket(): Socket!
```

Creates an unconnected socket.

| Return ||
|---------------------------------------------------------------------------------|------------------------|
| [Socket](../java/net/Socket.md)! | the unconnected socket |

| Exceptions ||
|-----------------------|---------------------------------|
| `java.io.IOException` | if the socket cannot be created |

**See Also**

- [java.net.Socket#connect(java.net.SocketAddress)](../java/net/Socket.md))
- [java.net.Socket#connect(java.net.SocketAddress, int)](../java/net/Socket.md))
- [java.net.Socket#Socket()](../java/net/Socket.md)) 

### createSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createSocket(
    host: String!, 
    port: Int
): Socket!
```

Creates a socket and connects it to the specified remote host at the specified remote port. This socket is configured using the socket options established for this factory.

If there is a security manager, its`checkConnect`method is called with the host address and`port`as its arguments. This could result in a SecurityException.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the server host name with which to connect, or`null`for the loopback address. |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the server port |

| Return ||
|---------------------------------------------------------------------------------|-------------|
| [Socket](../java/net/Socket.md)! | the`Socket` |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs when creating the socket |
| `java.lang.SecurityException` | if a security manager exists and its`checkConnect`method doesn't allow the operation. |
| `java.net.UnknownHostException` | if the host is not known |
| --- | --- |
| `java.lang.IllegalArgumentException` | if the port parameter is outside the specified range of valid port values, which is between 0 and 65535, inclusive. |

**See Also**

- [java.net.Socket#Socket(String, int)](../java/net/Socket.md)) 

### createSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createSocket(
    host: String!, 
    port: Int, 
    localHost: InetAddress!, 
    localPort: Int
): Socket!
```

Creates a socket and connects it to the specified remote host on the specified remote port. The socket will also be bound to the local address and port supplied. This socket is configured using the socket options established for this factory.

If there is a security manager, its`checkConnect`method is called with the host address and`port`as its arguments. This could result in a SecurityException.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the server host name with which to connect, or`null`for the loopback address. |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the server port |
| `localHost` | [InetAddress](../java/net/InetAddress.md)!:the local address the socket is bound to |
| --- | --- |
| `localPort` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the local port the socket is bound to |

| Return ||
|---------------------------------------------------------------------------------|-------------|
| [Socket](../java/net/Socket.md)! | the`Socket` |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs when creating the socket |
| `java.lang.SecurityException` | if a security manager exists and its`checkConnect`method doesn't allow the operation. |
| `java.net.UnknownHostException` | if the host is not known |
| --- | --- |
| `java.lang.IllegalArgumentException` | if the port parameter or localPort parameter is outside the specified range of valid port values, which is between 0 and 65535, inclusive. |

**See Also**

- [java.net.Socket#Socket(String, int, java.net.InetAddress, int)](../java/net/Socket.md)) 

### createSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createSocket(
    host: InetAddress!, 
    port: Int
): Socket!
```

Creates a socket and connects it to the specified port number at the specified address. This socket is configured using the socket options established for this factory.

If there is a security manager, its`checkConnect`method is called with the host address and`port`as its arguments. This could result in a SecurityException.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------|
| `host` | [InetAddress](../java/net/InetAddress.md)!:the server host |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the server port |

| Return ||
|---------------------------------------------------------------------------------|-------------|
| [Socket](../java/net/Socket.md)! | the`Socket` |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs when creating the socket |
| `java.lang.SecurityException` | if a security manager exists and its`checkConnect`method doesn't allow the operation. |
| `java.lang.IllegalArgumentException` | if the port parameter is outside the specified range of valid port values, which is between 0 and 65535, inclusive. |
| --- | --- |
| `java.lang.NullPointerException` | if`host`is null. |

**See Also**

- [java.net.Socket#Socket(java.net.InetAddress, int)](../java/net/Socket.md)) 

### createSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createSocket(
    address: InetAddress!, 
    port: Int, 
    localAddress: InetAddress!, 
    localPort: Int
): Socket!
```

Creates a socket and connect it to the specified remote address on the specified remote port. The socket will also be bound to the local address and port suplied. The socket is configured using the socket options established for this factory.

If there is a security manager, its`checkConnect`method is called with the host address and`port`as its arguments. This could result in a SecurityException.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------|
| `address` | [InetAddress](../java/net/InetAddress.md)!:the server network address |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the server port |
| `localAddress` | [InetAddress](../java/net/InetAddress.md)!:the client network address |
| --- | --- |
| `localPort` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the client port |

| Return ||
|---------------------------------------------------------------------------------|-------------|
| [Socket](../java/net/Socket.md)! | the`Socket` |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs when creating the socket |
| `java.lang.SecurityException` | if a security manager exists and its`checkConnect`method doesn't allow the operation. |
| `java.lang.IllegalArgumentException` | if the port parameter or localPort parameter is outside the specified range of valid port values, which is between 0 and 65535, inclusive. |
| --- | --- |
| `java.lang.NullPointerException` | if`address`is null. |

**See Also**

- [java.net.Socket#Socket(java.net.InetAddress, int,
* java.net.InetAddress, int)](../java/net/Socket.md)) 

### getDefault

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getDefault(): SocketFactory!
```

Returns a copy of the environment's default socket factory.

| Return ||
|-------------------------------------------------------------------------------------------|----------------------------|
| [SocketFactory](../javax/net/SocketFactory.md)! | the default`SocketFactory` |
