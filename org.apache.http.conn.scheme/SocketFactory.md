# SocketFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SocketFactory

```
interface SocketFactory
```

| [org.apache.http.conn.scheme.SocketFactory](SocketFactory.md) |

| Known Direct Subclasses [LayeredSocketFactory](LayeredSocketFactory.md) |-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------| | [LayeredSocketFactory](LayeredSocketFactory.md) | A [SocketFactory](SocketFactory.md) for layered sockets (SSL/TLS). | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [SSLSocketFactory](../org.apache.http.conn.ssl/SSLSocketFactory.md) |--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------| | [SSLSocketFactory](../org.apache.http.conn.ssl/SSLSocketFactory.md) | Layered socket factory for TLS/SSL connections, based on JSSE. | |
| --- | --- | --- | --- | --- | --- | --- |

| **This interface was deprecated in API level 22.**
|
| Please use java.net.URL#openConnection instead. Please visit [this webpage](http://android-developers.blogspot.com/2011/09/androids-http-clients.html) for further details.

A factory for creating and connecting sockets. The factory encapsulates the logic for establishing a socket connection. 
Both [Object.equals()](../java.lang/Object.md))and [Object.hashCode()](../java.lang/Object.md))must be overridden for the correct operation of some connection managers.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Socket](../java.net/Socket.md)! | [connectSocket](SocketFactory.md))`(`sock:` ` [Socket](../java.net/Socket.md)!`, `host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `localAddress:` ` [InetAddress](../java.net/InetAddress.md)!`, `localPort:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `params:` ` [HttpParams](../org.apache.http.params/HttpParams.md)!`)` Connects a socket to the given host. |
| abstract [Socket](../java.net/Socket.md)! | [createSocket](SocketFactory.md))`()` Creates a new, unconnected socket. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSecure](SocketFactory.md))`(`sock:` ` [Socket](../java.net/Socket.md)!`)` Checks whether a socket provides a secure connection. |
| --- | --- |

## Public methods

### connectSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun connectSocket(
    sock: Socket!, 
    host: String!, 
    port: Int, 
    localAddress: InetAddress!, 
    localPort: Int, 
    params: HttpParams!
): Socket!
```

**Deprecated:** *Deprecated in Java.*

Connects a socket to the given host.

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sock` | [Socket](../java.net/Socket.md)!:the socket to connect, as obtained from [createSocket](SocketFactory.md)).`null`indicates that a new socket should be created and connected. |
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the host to connect to |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the port to connect to on the host |
| --- | --- |
| `localAddress` | [InetAddress](../java.net/InetAddress.md)!:the local address to bind the socket to, or`null`for any |
| `localPort` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the port on the local machine, 0 or a negative number for any |
| `params` | [HttpParams](../org.apache.http.params/HttpParams.md)!:additional [parameters](../org.apache.http.params/HttpParams.md) for connecting |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [Socket](../java.net/Socket.md)! | the connected socket. The returned object may be different from the`sock`argument if this factory supports a layered protocol. |

| Exceptions ||
|------------------------------------------------|--------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.net.UnknownHostException` | if the IP address of the target host can not be determined |
| `org.apache.http.conn.ConnectTimeoutException` | if the socket cannot be connected within the time limit defined in the`params` |
| --- | --- |

### createSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createSocket(): Socket!
```

**Deprecated:** *Deprecated in Java.*

Creates a new, unconnected socket. The socket should subsequently be passed to [connectSocket](SocketFactory.md)).

| Return ||
|---------------------------------------------------------------------------------|--------------|
| [Socket](../java.net/Socket.md)! | a new socket |

| Exceptions ||
|-----------------------|--------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs while creating the socket |

### isSecure

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isSecure(sock: Socket!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Checks whether a socket provides a secure connection. The socket must be [connected](SocketFactory.md))by this factory. The factory will*not* perform I/O operations in this method. 
As a rule of thumb, plain sockets are not secure and TLS/SSL sockets are secure. However, there may be application specific deviations. For example, a plain socket to a host in the same intranet ("trusted zone") could be considered secure. On the other hand, a TLS/SSL socket could be considered insecure based on the cypher suite chosen for the connection.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------|
| `sock` | [Socket](../java.net/Socket.md)!:the connected socket to check |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the connection of the socket should be considered secure, or`false`if it should not |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the argument is invalid, for example because it is not a connected socket or was created by a different socket factory. Note that socket factories are*not*required to check these conditions, they may simply return a default value when called with an invalid socket argument. |
