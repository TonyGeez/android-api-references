# SocketFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SocketFactory

```
abstract class SocketFactory
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.net.SocketFactory](https://developer.android.com/reference/kotlin/javax/net/SocketFactory#) |

| Known Direct Subclasses [SSLSocketFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocketFactory) |---------------------------------------------------------------------------------------------------|-----------------------------------------| | [SSLSocketFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocketFactory) | `SSLSocketFactory`s create`SSLSocket`s. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [SSLCertificateSocketFactory](https://developer.android.com/reference/kotlin/android/net/SSLCertificateSocketFactory.html#) |-----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [SSLCertificateSocketFactory](https://developer.android.com/reference/kotlin/android/net/SSLCertificateSocketFactory.html#) | SSLSocketFactory implementation with several extra features: - Timeout specification for SSL handshake operations - Hostname verification in most cases (see WARNINGs below) - Optional SSL session caching with [SSLSessionCache](https://developer.android.com/reference/kotlin/android/net/SSLSessionCache.html#) - Optionally bypass all SSL certificate checks The handshake timeout does not apply to actual TCP socket connection. <br /> | |
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
| [SocketFactory](https://developer.android.com/reference/kotlin/javax/net/SocketFactory#SocketFactory())`()` Creates a`SocketFactory`. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | [createSocket](https://developer.android.com/reference/kotlin/javax/net/SocketFactory#createSocket())`()` Creates an unconnected socket. |
| abstract [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | [createSocket](https://developer.android.com/reference/kotlin/javax/net/SocketFactory#createSocket(kotlin.String,%20kotlin.Int))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a socket and connects it to the specified remote host at the specified remote port. |
| abstract [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | [createSocket](https://developer.android.com/reference/kotlin/javax/net/SocketFactory#createSocket(kotlin.String,%20kotlin.Int,%20java.net.InetAddress,%20kotlin.Int))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `localHost:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!`, `localPort:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a socket and connects it to the specified remote host on the specified remote port. |
| --- | --- |
| abstract [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | [createSocket](https://developer.android.com/reference/kotlin/javax/net/SocketFactory#createSocket(java.net.InetAddress,%20kotlin.Int))`(`host:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a socket and connects it to the specified port number at the specified address. |
| abstract [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | [createSocket](https://developer.android.com/reference/kotlin/javax/net/SocketFactory#createSocket(java.net.InetAddress,%20kotlin.Int,%20java.net.InetAddress,%20kotlin.Int))`(`address:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `localAddress:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!`, `localPort:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a socket and connect it to the specified remote address on the specified remote port. |
| openstatic [SocketFactory](https://developer.android.com/reference/kotlin/javax/net/SocketFactory#)! | [getDefault](https://developer.android.com/reference/kotlin/javax/net/SocketFactory#getDefault())`()` Returns a copy of the environment's default socket factory. |
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
| [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | the unconnected socket |

| Exceptions ||
|-----------------------|---------------------------------|
| `java.io.IOException` | if the socket cannot be created |

**See Also**

- [java.net.Socket#connect(java.net.SocketAddress)](https://developer.android.com/reference/kotlin/java/net/Socket.html#connect(java.net.SocketAddress))
- [java.net.Socket#connect(java.net.SocketAddress, int)](https://developer.android.com/reference/kotlin/java/net/Socket.html#connect(java.net.SocketAddress,%20kotlin.Int))
- [java.net.Socket#Socket()](https://developer.android.com/reference/kotlin/java/net/Socket.html#Socket()) 

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
| [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | the`Socket` |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs when creating the socket |
| `java.lang.SecurityException` | if a security manager exists and its`checkConnect`method doesn't allow the operation. |
| `java.net.UnknownHostException` | if the host is not known |
| --- | --- |
| `java.lang.IllegalArgumentException` | if the port parameter is outside the specified range of valid port values, which is between 0 and 65535, inclusive. |

**See Also**

- [java.net.Socket#Socket(String, int)](https://developer.android.com/reference/kotlin/java/net/Socket.html#Socket(kotlin.String,%20kotlin.Int)) 

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
| `localHost` | [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!:the local address the socket is bound to |
| --- | --- |
| `localPort` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the local port the socket is bound to |

| Return ||
|---------------------------------------------------------------------------------|-------------|
| [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | the`Socket` |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs when creating the socket |
| `java.lang.SecurityException` | if a security manager exists and its`checkConnect`method doesn't allow the operation. |
| `java.net.UnknownHostException` | if the host is not known |
| --- | --- |
| `java.lang.IllegalArgumentException` | if the port parameter or localPort parameter is outside the specified range of valid port values, which is between 0 and 65535, inclusive. |

**See Also**

- [java.net.Socket#Socket(String, int, java.net.InetAddress, int)](https://developer.android.com/reference/kotlin/java/net/Socket.html#Socket(kotlin.String,%20kotlin.Int,%20java.net.InetAddress,%20kotlin.Int)) 

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
| `host` | [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!:the server host |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the server port |

| Return ||
|---------------------------------------------------------------------------------|-------------|
| [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | the`Socket` |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs when creating the socket |
| `java.lang.SecurityException` | if a security manager exists and its`checkConnect`method doesn't allow the operation. |
| `java.lang.IllegalArgumentException` | if the port parameter is outside the specified range of valid port values, which is between 0 and 65535, inclusive. |
| --- | --- |
| `java.lang.NullPointerException` | if`host`is null. |

**See Also**

- [java.net.Socket#Socket(java.net.InetAddress, int)](https://developer.android.com/reference/kotlin/java/net/Socket.html#Socket(java.net.InetAddress,%20kotlin.Int)) 

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
| `address` | [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!:the server network address |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the server port |
| `localAddress` | [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!:the client network address |
| --- | --- |
| `localPort` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the client port |

| Return ||
|---------------------------------------------------------------------------------|-------------|
| [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | the`Socket` |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs when creating the socket |
| `java.lang.SecurityException` | if a security manager exists and its`checkConnect`method doesn't allow the operation. |
| `java.lang.IllegalArgumentException` | if the port parameter or localPort parameter is outside the specified range of valid port values, which is between 0 and 65535, inclusive. |
| --- | --- |
| `java.lang.NullPointerException` | if`address`is null. |

**See Also**

- [java.net.Socket#Socket(java.net.InetAddress, int,
* java.net.InetAddress, int)](https://developer.android.com/reference/kotlin/java/net/Socket.html#Socket(java.net.InetAddress,%20kotlin.Int,%20java.net.InetAddress,%20kotlin.Int)) 

### getDefault

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getDefault(): SocketFactory!
```

Returns a copy of the environment's default socket factory.

| Return ||
|-------------------------------------------------------------------------------------------|----------------------------|
| [SocketFactory](https://developer.android.com/reference/kotlin/javax/net/SocketFactory#)! | the default`SocketFactory` |
