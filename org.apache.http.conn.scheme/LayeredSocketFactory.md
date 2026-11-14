# LayeredSocketFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LayeredSocketFactory

```
interface LayeredSocketFactory : SocketFactory
```

| [org.apache.http.conn.scheme.LayeredSocketFactory](https://developer.android.com/reference/kotlin/org/apache/http/conn/scheme/LayeredSocketFactory#) |

| Known Direct Subclasses [SSLSocketFactory](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/SSLSocketFactory.html#) |--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------| | [SSLSocketFactory](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/SSLSocketFactory.html#) | Layered socket factory for TLS/SSL connections, based on JSSE. | |
| --- | --- | --- | --- | --- | --- | --- |

| **This interface was deprecated in API level 22.**
|
| Please use java.net.URL#openConnection instead. Please visit [this webpage](http://android-developers.blogspot.com/2011/09/androids-http-clients.html) for further details.

A [SocketFactory](https://developer.android.com/reference/kotlin/org/apache/http/conn/scheme/SocketFactory) for layered sockets (SSL/TLS). See there for things to consider when implementing a socket factory.

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | [createSocket](https://developer.android.com/reference/kotlin/org/apache/http/conn/scheme/LayeredSocketFactory#createSocket(java.net.Socket,%20kotlin.String,%20kotlin.Int,%20kotlin.Boolean))`(`socket:` ` [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)!`, `host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `autoClose:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Returns a socket connected to the given host that is layered over an existing socket. |

| Inherited functions ||
|---|---|
| From class [SocketFactory](https://developer.android.com/reference/kotlin/org/apache/http/conn/scheme/SocketFactory) |------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | [connectSocket](https://developer.android.com/reference/kotlin/org/apache/http/conn/scheme/SocketFactory#connectSocket(java.net.Socket,%20kotlin.String,%20kotlin.Int,%20java.net.InetAddress,%20kotlin.Int,%20org.apache.http.params.HttpParams))`(`sock:` ` [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)!`, `host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `localAddress:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!`, `localPort:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `params:` ` [HttpParams](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams.html#)!`)` <br /> Connects a socket to the given host. <br /> | | [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | [createSocket](https://developer.android.com/reference/kotlin/org/apache/http/conn/scheme/SocketFactory#createSocket())`()` <br /> Creates a new, unconnected socket. The socket should subsequently be passed to [connectSocket](https://developer.android.com/reference/kotlin/org/apache/http/conn/scheme/SocketFactory#connectSocket(java.net.Socket,%20kotlin.String,%20kotlin.Int,%20java.net.InetAddress,%20kotlin.Int,%20org.apache.http.params.HttpParams)). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSecure](https://developer.android.com/reference/kotlin/org/apache/http/conn/scheme/SocketFactory#isSecure(java.net.Socket))`(`sock:` ` [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)!`)` <br /> Checks whether a socket provides a secure connection. The socket must be [connected](https://developer.android.com/reference/kotlin/org/apache/http/conn/scheme/SocketFactory#connectSocket(java.net.Socket,%20kotlin.String,%20kotlin.Int,%20java.net.InetAddress,%20kotlin.Int,%20org.apache.http.params.HttpParams))by this factory. The factory will*not* perform I/O operations in this method. As a rule of thumb, plain sockets are not secure and TLS/SSL sockets are secure. However, there may be application specific deviations. For example, a plain socket to a host in the same intranet ("trusted zone") could be considered secure. On the other hand, a TLS/SSL socket could be considered insecure based on the cypher suite chosen for the connection. <br /> | ||

## Public methods

### createSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createSocket(
    socket: Socket!, 
    host: String!, 
    port: Int, 
    autoClose: Boolean
): Socket!
```

**Deprecated:** *Deprecated in Java.*

Returns a socket connected to the given host that is layered over an existing socket. Used primarily for creating secure sockets through proxies.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `socket` | [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)!:the existing socket |
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the host name/IP |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the port on the host |
| --- | --- |
| `autoClose` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):a flag for closing the underling socket when the created socket is closed |

| Return ||
|---------------------------------------------------------------------------------|---------------------|
| [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | Socket a new socket |

| Exceptions ||
|---------------------------------|----------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs while creating the socket |
| `java.net.UnknownHostException` | if the IP address of the host cannot be determined |
