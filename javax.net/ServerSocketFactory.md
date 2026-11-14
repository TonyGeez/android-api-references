Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ServerSocketFactory

```
abstract class ServerSocketFactory
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.net.ServerSocketFactory](https://developer.android.com/reference/kotlin/javax/net/ServerSocketFactory#) |

| Known Direct Subclasses [SSLServerSocketFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocketFactory) |---|---| | [SSLServerSocketFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocketFactory) | `SSLServerSocketFactory`s create `SSLServerSocket`s. | |
| --- | --- | --- | --- | --- | --- | --- |

This class creates server sockets. It may be subclassed by other factories, which create particular types of server sockets. This provides a general framework for the addition of public socket-level functionality. It is the server side analogue of a socket factory, and similarly provides a way to capture a variety of policies related to the sockets being constructed.

Like socket factories, server Socket factory instances have methods used to create sockets. There is also an environment specific default server socket factory; frameworks will often use their own customized factory.

## Summary

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/net/ServerSocketFactory#ServerSocketFactory()()` Creates a server socket factory. |

| Public methods ||
|---|---|
| open [ServerSocket](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#)! | `https://developer.android.com/reference/kotlin/javax/net/ServerSocketFactory#createServerSocket()()` Returns an unbound server socket. |
| abstract [ServerSocket](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#)! | `https://developer.android.com/reference/kotlin/javax/net/ServerSocketFactory#createServerSocket(kotlin.Int)(port: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a server socket bound to the specified port. |
| abstract [ServerSocket](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#)! | `https://developer.android.com/reference/kotlin/javax/net/ServerSocketFactory#createServerSocket(kotlin.Int,%20kotlin.Int)(port: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, backlog: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a server socket bound to the specified port, and uses the specified connection backlog. |
| --- | --- |
| abstract [ServerSocket](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#)! | `https://developer.android.com/reference/kotlin/javax/net/ServerSocketFactory#createServerSocket(kotlin.Int,%20kotlin.Int,%20java.net.InetAddress)(port: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, backlog: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, ifAddress: https://developer.android.com/reference/kotlin/java/net/InetAddress.html#!)` Returns a server socket bound to the specified port, with a specified listen backlog and local IP. |
| open static [ServerSocketFactory](https://developer.android.com/reference/kotlin/javax/net/ServerSocketFactory#)! | `https://developer.android.com/reference/kotlin/javax/net/ServerSocketFactory#getDefault()()` Returns a copy of the environment's default socket factory. |

## Protected constructors

### ServerSocketFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected ServerSocketFactory()
```

Creates a server socket factory.

## Public methods

### createServerSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createServerSocket(): ServerSocket!
```

Returns an unbound server socket. The socket is configured with the socket options (such as accept timeout) given to this factory.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#!` | the unbound socket |

| Exceptions ||
|---|---|
| `java.io.IOException` | if the socket cannot be created |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#bind(java.net.SocketAddress)`
- `https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#bind(java.net.SocketAddress,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#ServerSocket()`

### createServerSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun createServerSocket(port: Int): ServerSocket!
```

Returns a server socket bound to the specified port. The socket is configured with the socket options (such as accept timeout) given to this factory.

If there is a security manager, its `checkListen` method is called with the `port` argument as its argument to ensure the operation is allowed. This could result in a SecurityException.

| Parameters ||
|---|---|
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the port to listen to |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#!` | the `ServerSocket` |

| Exceptions ||
|---|---|
| `java.io.IOException` | for networking errors |
| `java.lang.IllegalArgumentException` | if the port parameter is outside the specified range of valid port values, which is between 0 and 65535, inclusive. |
| `java.lang.SecurityException` | if a security manager exists and its `checkListen` method doesn't allow the operation. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkListen(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#ServerSocket(kotlin.Int)`

### createServerSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun createServerSocket(
    port: Int, 
    backlog: Int
): ServerSocket!
```

Returns a server socket bound to the specified port, and uses the specified connection backlog. The socket is configured with the socket options (such as accept timeout) given to this factory.

The `backlog` argument must be a positive value greater than 0. If the value passed if equal or less than 0, then the default value will be assumed.

If there is a security manager, its `checkListen` method is called with the `port` argument as its argument to ensure the operation is allowed. This could result in a SecurityException.

| Parameters ||
|---|---|
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the port to listen to |
| `backlog` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): how many connections are queued |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#!` | the `ServerSocket` |

| Exceptions ||
|---|---|
| `java.io.IOException` | for networking errors |
| `java.lang.IllegalArgumentException` | if the port parameter is outside the specified range of valid port values, which is between 0 and 65535, inclusive. |
| `java.lang.SecurityException` | if a security manager exists and its `checkListen` method doesn't allow the operation. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkListen(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#ServerSocket(kotlin.Int,%20kotlin.Int)`

### createServerSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun createServerSocket(
    port: Int, 
    backlog: Int, 
    ifAddress: InetAddress!
): ServerSocket!
```

Returns a server socket bound to the specified port, with a specified listen backlog and local IP.

The `ifAddress` argument can be used on a multi-homed host for a `ServerSocket` that will only accept connect requests to one of its addresses. If `ifAddress` is null, it will accept connections on all local addresses. The socket is configured with the socket options (such as accept timeout) given to this factory.

The `backlog` argument must be a positive value greater than 0. If the value passed if equal or less than 0, then the default value will be assumed.

If there is a security manager, its `checkListen` method is called with the `port` argument as its argument to ensure the operation is allowed. This could result in a SecurityException.

| Parameters ||
|---|---|
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the port to listen to |
| `backlog` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): how many connections are queued |
| `ifAddress` | [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!: the network interface address to use |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#!` | the `ServerSocket` |

| Exceptions ||
|---|---|
| `java.io.IOException` | for networking errors |
| `java.lang.IllegalArgumentException` | if the port parameter is outside the specified range of valid port values, which is between 0 and 65535, inclusive. |
| `java.lang.SecurityException` | if a security manager exists and its `checkListen` method doesn't allow the operation. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkListen(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#ServerSocket(kotlin.Int,%20kotlin.Int,%20java.net.InetAddress)`

### getDefault

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getDefault(): ServerSocketFactory!
```

Returns a copy of the environment's default socket factory.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/net/ServerSocketFactory#!` | the `ServerSocketFactory` |
