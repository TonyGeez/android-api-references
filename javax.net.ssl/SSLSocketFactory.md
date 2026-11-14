# SSLSocketFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SSLSocketFactory

```
abstract class SSLSocketFactory : SocketFactory
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [javax.net.SocketFactory](https://developer.android.com/reference/kotlin/javax/net/SocketFactory.html#) ||
| | ↳ | [javax.net.ssl.SSLSocketFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocketFactory#) |

| Known Direct Subclasses [SSLCertificateSocketFactory](https://developer.android.com/reference/kotlin/android/net/SSLCertificateSocketFactory.html#) |-----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [SSLCertificateSocketFactory](https://developer.android.com/reference/kotlin/android/net/SSLCertificateSocketFactory.html#) | SSLSocketFactory implementation with several extra features: - Timeout specification for SSL handshake operations - Hostname verification in most cases (see WARNINGs below) - Optional SSL session caching with [SSLSessionCache](https://developer.android.com/reference/kotlin/android/net/SSLSessionCache.html#) - Optionally bypass all SSL certificate checks The handshake timeout does not apply to actual TCP socket connection. <br /> | |

`SSLSocketFactory`s create`SSLSocket`s.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SSLSocketFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocketFactory#SSLSocketFactory())`()` Constructor is used only by subclasses. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | [createSocket](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocketFactory#createSocket(java.net.Socket,%20kotlin.String,%20kotlin.Int,%20kotlin.Boolean))`(`s:` ` [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)!`, `host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `autoClose:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Returns a socket layered over an existing socket connected to the named host, at the given port. |
| openstatic [SocketFactory](https://developer.android.com/reference/kotlin/javax/net/SocketFactory.html#)! | [getDefault](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocketFactory#getDefault())`()` Returns the default SSL socket factory. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getDefaultCipherSuites](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocketFactory#getDefaultCipherSuites())`()` Returns the list of cipher suites which are enabled by default. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getSupportedCipherSuites](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocketFactory#getSupportedCipherSuites())`()` Returns the names of the cipher suites which could be enabled for use on an SSL connection. |

| Inherited functions ||
|---|---|
| From class [SocketFactory](https://developer.android.com/reference/kotlin/javax/net/SocketFactory.html#) |---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | [createSocket](https://developer.android.com/reference/kotlin/javax/net/SocketFactory.html#createSocket())`()` <br /> Creates an unconnected socket. <br /> | | [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | [createSocket](https://developer.android.com/reference/kotlin/javax/net/SocketFactory.html#createSocket(kotlin.String,%20kotlin.Int))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Creates a socket and connects it to the specified remote host at the specified remote port. This socket is configured using the socket options established for this factory. If there is a security manager, its`checkConnect`method is called with the host address and`port`as its arguments. This could result in a SecurityException. <br /> | | [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | [createSocket](https://developer.android.com/reference/kotlin/javax/net/SocketFactory.html#createSocket(kotlin.String,%20kotlin.Int,%20java.net.InetAddress,%20kotlin.Int))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `localHost:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!`, `localPort:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Creates a socket and connects it to the specified remote host on the specified remote port. The socket will also be bound to the local address and port supplied. This socket is configured using the socket options established for this factory. If there is a security manager, its`checkConnect`method is called with the host address and`port`as its arguments. This could result in a SecurityException. <br /> | | [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | [createSocket](https://developer.android.com/reference/kotlin/javax/net/SocketFactory.html#createSocket(java.net.InetAddress,%20kotlin.Int))`(`host:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Creates a socket and connects it to the specified port number at the specified address. This socket is configured using the socket options established for this factory. If there is a security manager, its`checkConnect`method is called with the host address and`port`as its arguments. This could result in a SecurityException. <br /> | | [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | [createSocket](https://developer.android.com/reference/kotlin/javax/net/SocketFactory.html#createSocket(java.net.InetAddress,%20kotlin.Int,%20java.net.InetAddress,%20kotlin.Int))`(`address:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `localAddress:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!`, `localPort:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Creates a socket and connect it to the specified remote address on the specified remote port. The socket will also be bound to the local address and port suplied. The socket is configured using the socket options established for this factory. If there is a security manager, its`checkConnect`method is called with the host address and`port`as its arguments. This could result in a SecurityException. <br /> | ||

## Public constructors

### SSLSocketFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SSLSocketFactory()
```

Constructor is used only by subclasses.

## Public methods

### createSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createSocket(
    s: Socket!, 
    host: String!, 
    port: Int, 
    autoClose: Boolean
): Socket!
```

Returns a socket layered over an existing socket connected to the named host, at the given port. This constructor can be used when tunneling SSL through a proxy or when negotiating the use of SSL over an existing socket. The host and port refer to the logical peer destination. This socket is configured using the socket options established for this factory.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)!:the existing socket |
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the server host |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the server port |
| `autoClose` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):close the underlying socket when this socket is closed |

| Return ||
|---------------------------------------------------------------------------------|---------------------------------------------------|
| [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | a socket connected to the specified host and port |

| Exceptions ||
|----------------------------------|-------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs when creating the socket |
| `java.lang.NullPointerException` | if the parameter s is null |

### getDefault

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getDefault(): SocketFactory!
```

Returns the default SSL socket factory.

The first time this method is called, the security property "ssl.SocketFactory.provider" is examined. If it is non-null, a class by that name is loaded and instantiated. If that is successful and the object is an instance of SSLSocketFactory, it is made the default SSL socket factory.

Otherwise, this method returns`SSLContext.getDefault().getSocketFactory()`. If that call fails, an inoperative factory is returned.

| Return ||
|------------------------------------------------------------------------------------------------|----------------------------|
| [SocketFactory](https://developer.android.com/reference/kotlin/javax/net/SocketFactory.html#)! | the default`SocketFactory` |

**See Also**

- [javax.net.ssl.SSLContext#getDefault](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#getDefault()) 

### getDefaultCipherSuites

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDefaultCipherSuites(): Array<String!>!
```

Returns the list of cipher suites which are enabled by default. Unless a different list is enabled, handshaking on an SSL connection will use one of these cipher suites. The minimum quality of service for these defaults requires confidentiality protection and server authentication (that is, no anonymous cipher suites).

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | array of the cipher suites enabled by default |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocketFactory#getSupportedCipherSuites()> 

### getSupportedCipherSuites

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSupportedCipherSuites(): Array<String!>!
```

Returns the names of the cipher suites which could be enabled for use on an SSL connection. Normally, only a subset of these will actually be enabled by default, since this list may include cipher suites which do not meet quality of service requirements for those defaults. Such cipher suites are useful in specialized applications.

Applications should not blindly enable all supported cipher suites. The supported cipher suites can include signaling cipher suite values that can cause connection problems if enabled inappropriately.

The proper way to use this method is to either check if a specific cipher suite is supported via`Arrays.asList(getSupportedCipherSuites()).contains(...)`or to filter a desired list of cipher suites to only the supported ones via`desiredSuiteSet.retainAll(Arrays.asList(getSupportedCipherSuites()))`.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | an array of cipher suite names |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocketFactory#getDefaultCipherSuites()>
