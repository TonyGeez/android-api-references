# LayeredSocketFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LayeredSocketFactory

```
interface LayeredSocketFactory : SocketFactory
```

| [org.apache.http.conn.scheme.LayeredSocketFactory](../org/apache/http/conn/scheme/LayeredSocketFactory.md) |

| Known Direct Subclasses [SSLSocketFactory](../org/apache/http/conn/ssl/SSLSocketFactory.md) |--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------| | [SSLSocketFactory](../org/apache/http/conn/ssl/SSLSocketFactory.md) | Layered socket factory for TLS/SSL connections, based on JSSE. | |
| --- | --- | --- | --- | --- | --- | --- |

| **This interface was deprecated in API level 22.**
|
| Please use java.net.URL#openConnection instead. Please visit [this webpage](http://android-developers.blogspot.com/2011/09/androids-http-clients.html) for further details.

A [SocketFactory](../org/apache/http/conn/scheme/SocketFactory.md) for layered sockets (SSL/TLS). See there for things to consider when implementing a socket factory.

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Socket](../java/net/Socket.md)! | [createSocket](../org/apache/http/conn/scheme/LayeredSocketFactory.md))`(`socket:` ` [Socket](../java/net/Socket.md)!`, `host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `autoClose:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Returns a socket connected to the given host that is layered over an existing socket. |

| Inherited functions ||
|---|---|
| From class [SocketFactory](../org/apache/http/conn/scheme/SocketFactory.md) |------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Socket](../java/net/Socket.md)! | [connectSocket](../org/apache/http/conn/scheme/SocketFactory.md))`(`sock:` ` [Socket](../java/net/Socket.md)!`, `host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `localAddress:` ` [InetAddress](../java/net/InetAddress.md)!`, `localPort:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `params:` ` [HttpParams](../org/apache/http/params/HttpParams.md)!`)` <br /> Connects a socket to the given host. <br /> | | [Socket](../java/net/Socket.md)! | [createSocket](../org/apache/http/conn/scheme/SocketFactory.md))`()` <br /> Creates a new, unconnected socket. The socket should subsequently be passed to [connectSocket](../org/apache/http/conn/scheme/SocketFactory.md)). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSecure](../org/apache/http/conn/scheme/SocketFactory.md))`(`sock:` ` [Socket](../java/net/Socket.md)!`)` <br /> Checks whether a socket provides a secure connection. The socket must be [connected](../org/apache/http/conn/scheme/SocketFactory.md))by this factory. The factory will*not* perform I/O operations in this method. As a rule of thumb, plain sockets are not secure and TLS/SSL sockets are secure. However, there may be application specific deviations. For example, a plain socket to a host in the same intranet ("trusted zone") could be considered secure. On the other hand, a TLS/SSL socket could be considered insecure based on the cypher suite chosen for the connection. <br /> | ||

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
| `socket` | [Socket](../java/net/Socket.md)!:the existing socket |
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the host name/IP |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the port on the host |
| --- | --- |
| `autoClose` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):a flag for closing the underling socket when the created socket is closed |

| Return ||
|---------------------------------------------------------------------------------|---------------------|
| [Socket](../java/net/Socket.md)! | Socket a new socket |

| Exceptions ||
|---------------------------------|----------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs while creating the socket |
| `java.net.UnknownHostException` | if the IP address of the host cannot be determined |
