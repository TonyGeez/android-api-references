# SSLCertificateSocketFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SSLCertificateSocketFactory

Kotlin| [Java](https://developer.android.com/reference/android/net/SSLCertificateSocketFactory "View this page in Java") 

```
open class SSLCertificateSocketFactory : SSLSocketFactory
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [javax.net.SocketFactory](https://developer.android.com/reference/kotlin/javax/net/SocketFactory.html#) |||
| | ↳ | [javax.net.ssl.SSLSocketFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocketFactory.html#) ||
| | | ↳ | [android.net.SSLCertificateSocketFactory](https://developer.android.com/reference/kotlin/android/net/SSLCertificateSocketFactory#) |

| **This class was deprecated in API level 29.**
|
| This class has less error-prone replacements using standard APIs. To create an`SSLSocket`, obtain an [SSLSocketFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocketFactory.html#) from [SSLSocketFactory.getDefault()](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocketFactory.html#getDefault())or [javax.net.ssl.SSLContext#getSocketFactory()](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext.html#getSocketFactory()). To verify hostnames, pass`"HTTPS"`to [javax.net.ssl.SSLParameters#setEndpointIdentificationAlgorithm(String)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters.html#setEndpointIdentificationAlgorithm(kotlin.String)). To enable ALPN, use[javax.net.ssl.SSLParameters#setApplicationProtocols(String[])](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters.html#setApplicationProtocols(kotlin.Array)). To enable SNI, use [javax.net.ssl.SSLParameters#setServerNames(java.util.List)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters.html#setServerNames(kotlin.collections.MutableList)).

SSLSocketFactory implementation with several extra features:

- Timeout specification for SSL handshake operations
- Hostname verification in most cases (see WARNINGs below)
- Optional SSL session caching with [SSLSessionCache](https://developer.android.com/reference/kotlin/android/net/SSLSessionCache)
- Optionally bypass all SSL certificate checks

The handshake timeout does not apply to actual TCP socket connection. If you want a connection timeout as well, use [createSocket()](https://developer.android.com/reference/kotlin/android/net/SSLCertificateSocketFactory#createSocket())and [Socket.connect(java.net.SocketAddress, int)](https://developer.android.com/reference/kotlin/java/net/Socket.html#connect(java.net.SocketAddress,%20kotlin.Int)), after which you must verify the identity of the server you are connected to.

<br />

**Most [SSLSocketFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocketFactory.html#) implementations do not verify the server's identity, allowing person-in-the-middle attacks.** This implementation does check the server's certificate hostname, but only for createSocket variants that specify a hostname. When using methods that use [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#) or which return an unconnected socket, you MUST verify the server's identity yourself to ensure a secure connection. Refer to [Updating Your Security Provider to Protect Against SSL Exploits](https://developer.android.com/training/articles/security-gms-provider.html) for further information.

The recommended way to verify the server's identity is to use [HttpsURLConnection.getDefaultHostnameVerifier()](https://developer.android.com/reference/kotlin/javax/net/ssl/HttpsURLConnection.html#getDefaultHostnameVerifier())to get a [HostnameVerifier](https://developer.android.com/reference/kotlin/javax/net/ssl/HostnameVerifier.html#) to verify the certificate hostname.

**Warning**: Some methods on this class return connected sockets and some return unconnected sockets. For the methods that return connected sockets, setting connection- or handshake-related properties on those sockets will have no effect.

On development devices, "setprop socket.relaxsslcheck yes" bypasses all SSL certificate and hostname checks for testing purposes. This setting requires root access.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SSLCertificateSocketFactory](https://developer.android.com/reference/kotlin/android/net/SSLCertificateSocketFactory#SSLCertificateSocketFactory(kotlin.Int))`(`handshakeTimeoutMillis:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | [createSocket](https://developer.android.com/reference/kotlin/android/net/SSLCertificateSocketFactory#createSocket())`()` Creates a new socket which is*not connected*to any remote host. |
| open [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | [createSocket](https://developer.android.com/reference/kotlin/android/net/SSLCertificateSocketFactory#createSocket(kotlin.String,%20kotlin.Int))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a socket and connects it to the specified remote host at the specified remote port. |
| open [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | [createSocket](https://developer.android.com/reference/kotlin/android/net/SSLCertificateSocketFactory#createSocket(kotlin.String,%20kotlin.Int,%20java.net.InetAddress,%20kotlin.Int))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `localAddr:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!`, `localPort:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a socket and connects it to the specified remote host on the specified remote port. |
| open [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | [createSocket](https://developer.android.com/reference/kotlin/android/net/SSLCertificateSocketFactory#createSocket(java.net.InetAddress,%20kotlin.Int))`(`addr:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a socket and connects it to the specified port number at the specified address. |
| open [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | [createSocket](https://developer.android.com/reference/kotlin/android/net/SSLCertificateSocketFactory#createSocket(java.net.InetAddress,%20kotlin.Int,%20java.net.InetAddress,%20kotlin.Int))`(`addr:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `localAddr:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!`, `localPort:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a socket and connect it to the specified remote address on the specified remote port. |
| open [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | [createSocket](https://developer.android.com/reference/kotlin/android/net/SSLCertificateSocketFactory#createSocket(java.net.Socket,%20kotlin.String,%20kotlin.Int,%20kotlin.Boolean))`(`k:` ` [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)!`, `host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `close:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Returns a socket layered over an existing socket connected to the named host, at the given port. |
| openstatic [SocketFactory](https://developer.android.com/reference/kotlin/javax/net/SocketFactory.html#)! | [getDefault](https://developer.android.com/reference/kotlin/android/net/SSLCertificateSocketFactory#getDefault(kotlin.Int))`(`handshakeTimeoutMillis:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a new socket factory instance with an optional handshake timeout. |
| openstatic [SSLSocketFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocketFactory.html#)! | [getDefault](https://developer.android.com/reference/kotlin/android/net/SSLCertificateSocketFactory#getDefault(kotlin.Int,%20android.net.SSLSessionCache))`(`handshakeTimeoutMillis:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cache:` ` [SSLSessionCache](https://developer.android.com/reference/kotlin/android/net/SSLSessionCache)!`)` Returns a new socket factory instance with an optional handshake timeout and SSL session cache. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getDefaultCipherSuites](https://developer.android.com/reference/kotlin/android/net/SSLCertificateSocketFactory#getDefaultCipherSuites())`()` <br /> |
| openstatic [SSLSocketFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocketFactory.html#)! | [getInsecure](https://developer.android.com/reference/kotlin/android/net/SSLCertificateSocketFactory#getInsecure(kotlin.Int,%20android.net.SSLSessionCache))`(`handshakeTimeoutMillis:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cache:` ` [SSLSessionCache](https://developer.android.com/reference/kotlin/android/net/SSLSessionCache)!`)` Returns a new instance of a socket factory with all SSL security checks disabled, using an optional handshake timeout and SSL session cache. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getNpnSelectedProtocol](https://developer.android.com/reference/kotlin/android/net/SSLCertificateSocketFactory#getNpnSelectedProtocol(java.net.Socket))`(`socket:` ` [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)!`)` Returns the [Next Protocol Negotiation (NPN)](http://technotes.googlecode.com/git/nextprotoneg.html) protocol selected by client and server, or null if no protocol was negotiated. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getSupportedCipherSuites](https://developer.android.com/reference/kotlin/android/net/SSLCertificateSocketFactory#getSupportedCipherSuites())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHostname](https://developer.android.com/reference/kotlin/android/net/SSLCertificateSocketFactory#setHostname(java.net.Socket,%20kotlin.String))`(`socket:` ` [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)!`, `hostName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Turns on [Server Name Indication (SNI)](http://tools.ietf.org/html/rfc6066#section-3) on a given socket. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setKeyManagers](https://developer.android.com/reference/kotlin/android/net/SSLCertificateSocketFactory#setKeyManagers(kotlin.Array))`(`keyManagers:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [KeyManager](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyManager.html#)!>!`)` Sets the [KeyManager](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyManager.html#) s to be used for connections made by this factory. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNpnProtocols](https://developer.android.com/reference/kotlin/android/net/SSLCertificateSocketFactory#setNpnProtocols(kotlin.Array))`(`npnProtocols:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!>!`)` Sets the [Next Protocol Negotiation (NPN)](https://tools.ietf.org/id/draft-agl-tls-nextprotoneg-03.html) protocols that this peer is interested in. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTrustManagers](https://developer.android.com/reference/kotlin/android/net/SSLCertificateSocketFactory#setTrustManagers(kotlin.Array))`(`trustManager:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [TrustManager](https://developer.android.com/reference/kotlin/javax/net/ssl/TrustManager.html#)!>!`)` Sets the [TrustManager](https://developer.android.com/reference/kotlin/javax/net/ssl/TrustManager.html#) s to be used for connections made by this factory. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUseSessionTickets](https://developer.android.com/reference/kotlin/android/net/SSLCertificateSocketFactory#setUseSessionTickets(java.net.Socket,%20kotlin.Boolean))`(`socket:` ` [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)!`, `useSessionTickets:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Enables [session ticket](http://tools.ietf.org/html/rfc5077#section-3.2) support on the given socket. |

| Inherited functions ||
|---|---|
| From class [SocketFactory](https://developer.android.com/reference/kotlin/javax/net/SocketFactory.html#) |---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | [createSocket](https://developer.android.com/reference/kotlin/javax/net/SocketFactory.html#createSocket())`()` <br /> Creates an unconnected socket. <br /> | | [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | [createSocket](https://developer.android.com/reference/kotlin/javax/net/SocketFactory.html#createSocket(kotlin.String,%20kotlin.Int))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Creates a socket and connects it to the specified remote host at the specified remote port. This socket is configured using the socket options established for this factory. If there is a security manager, its`checkConnect`method is called with the host address and`port`as its arguments. This could result in a SecurityException. <br /> | | [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | [createSocket](https://developer.android.com/reference/kotlin/javax/net/SocketFactory.html#createSocket(kotlin.String,%20kotlin.Int,%20java.net.InetAddress,%20kotlin.Int))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `localHost:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!`, `localPort:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Creates a socket and connects it to the specified remote host on the specified remote port. The socket will also be bound to the local address and port supplied. This socket is configured using the socket options established for this factory. If there is a security manager, its`checkConnect`method is called with the host address and`port`as its arguments. This could result in a SecurityException. <br /> | | [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | [createSocket](https://developer.android.com/reference/kotlin/javax/net/SocketFactory.html#createSocket(java.net.InetAddress,%20kotlin.Int))`(`host:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Creates a socket and connects it to the specified port number at the specified address. This socket is configured using the socket options established for this factory. If there is a security manager, its`checkConnect`method is called with the host address and`port`as its arguments. This could result in a SecurityException. <br /> | | [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | [createSocket](https://developer.android.com/reference/kotlin/javax/net/SocketFactory.html#createSocket(java.net.InetAddress,%20kotlin.Int,%20java.net.InetAddress,%20kotlin.Int))`(`address:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `localAddress:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!`, `localPort:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Creates a socket and connect it to the specified remote address on the specified remote port. The socket will also be bound to the local address and port suplied. The socket is configured using the socket options established for this factory. If there is a security manager, its`checkConnect`method is called with the host address and`port`as its arguments. This could result in a SecurityException. <br /> | ||
| From class [SSLSocketFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocketFactory.html#) |------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [SocketFactory](https://developer.android.com/reference/kotlin/javax/net/SocketFactory.html#)! | [getDefault](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocketFactory.html#getDefault())`()` <br /> Returns the default SSL socket factory. The first time this method is called, the security property "ssl.SocketFactory.provider" is examined. If it is non-null, a class by that name is loaded and instantiated. If that is successful and the object is an instance of SSLSocketFactory, it is made the default SSL socket factory. Otherwise, this method returns`SSLContext.getDefault().getSocketFactory()`. If that call fails, an inoperative factory is returned. <br /> | ||

## Public constructors

### SSLCertificateSocketFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SSLCertificateSocketFactory(handshakeTimeoutMillis: Int)
```

**Deprecated:** *Use [getDefault(int)](https://developer.android.com/reference/kotlin/android/net/SSLCertificateSocketFactory#getDefault(kotlin.Int))instead.*

## Public methods

### createSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createSocket(): Socket!
```

**Deprecated:** *Deprecated in Java.*

Creates a new socket which is*not connected*to any remote host. You must use java.net.Socket#connect to connect the socket.

**Warning:**Hostname verification is not performed with this method. You MUST verify the server's identity after connecting the socket to avoid person-in-the-middle attacks.

| Return ||
|---------------------------------------------------------------------------------|------------------------|
| [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | the unconnected socket |

| Exceptions ||
|-----------------------|---------------------------------|
| `java.io.IOException` | if the socket cannot be created |

### createSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createSocket(
    host: String!, 
    port: Int
): Socket!
```

**Deprecated:** *Deprecated in Java.*

Creates a socket and connects it to the specified remote host at the specified remote port. This socket is configured using the socket options established for this factory.

If there is a security manager, its`checkConnect`method is called with the host address and`port`as its arguments. This could result in a SecurityException.

By default, this method returns a*connected* socket and verifies the peer's certificate hostname after connecting using the [HostnameVerifier](https://developer.android.com/reference/kotlin/javax/net/ssl/HostnameVerifier.html#) obtained from`HttpsURLConnection.getDefaultHostnameVerifier()`; if this instance was created with [getInsecure(int,android.net.SSLSessionCache)](https://developer.android.com/reference/kotlin/android/net/SSLCertificateSocketFactory#getInsecure(kotlin.Int,%20android.net.SSLSessionCache)), it returns a socket that is*not connected*instead.

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
| `java.lang.IllegalArgumentException` | if the port parameter is outside the specified range of valid port values, which is between 0 and 65535, inclusive. |

### createSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createSocket(
    host: String!, 
    port: Int, 
    localAddr: InetAddress!, 
    localPort: Int
): Socket!
```

**Deprecated:** *Deprecated in Java.*

Creates a socket and connects it to the specified remote host on the specified remote port. The socket will also be bound to the local address and port supplied. This socket is configured using the socket options established for this factory.

If there is a security manager, its`checkConnect`method is called with the host address and`port`as its arguments. This could result in a SecurityException.

By default, this method returns a*connected* socket and verifies the peer's certificate hostname after connecting using the [HostnameVerifier](https://developer.android.com/reference/kotlin/javax/net/ssl/HostnameVerifier.html#) obtained from`HttpsURLConnection.getDefaultHostnameVerifier()`; if this instance was created with [getInsecure(int,android.net.SSLSessionCache)](https://developer.android.com/reference/kotlin/android/net/SSLCertificateSocketFactory#getInsecure(kotlin.Int,%20android.net.SSLSessionCache)), it returns a socket that is*not connected*instead.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the server host name with which to connect, or`null`for the loopback address. |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the server port |
| `localHost` | the local address the socket is bound to |
| `localPort` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the local port the socket is bound to |

| Return ||
|---------------------------------------------------------------------------------|-------------|
| [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | the`Socket` |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs when creating the socket |
| `java.lang.SecurityException` | if a security manager exists and its`checkConnect`method doesn't allow the operation. |
| `java.net.UnknownHostException` | if the host is not known |
| `java.lang.IllegalArgumentException` | if the port parameter or localPort parameter is outside the specified range of valid port values, which is between 0 and 65535, inclusive. |

### createSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createSocket(
    addr: InetAddress!, 
    port: Int
): Socket!
```

**Deprecated:** *Deprecated in Java.*

Creates a socket and connects it to the specified port number at the specified address. This socket is configured using the socket options established for this factory.

If there is a security manager, its`checkConnect`method is called with the host address and`port`as its arguments. This could result in a SecurityException.

This method returns a socket that is*not connected*.

**Warning:**Hostname verification is not performed with this method. You MUST verify the server's identity after connecting the socket to avoid person-in-the-middle attacks.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------|
| `host` | the server host |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the server port |

| Return ||
|---------------------------------------------------------------------------------|-------------|
| [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | the`Socket` |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs when creating the socket |
| `java.lang.SecurityException` | if a security manager exists and its`checkConnect`method doesn't allow the operation. |
| `java.lang.IllegalArgumentException` | if the port parameter is outside the specified range of valid port values, which is between 0 and 65535, inclusive. |
| `java.lang.NullPointerException` | if`host`is null. |

### createSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createSocket(
    addr: InetAddress!, 
    port: Int, 
    localAddr: InetAddress!, 
    localPort: Int
): Socket!
```

**Deprecated:** *Deprecated in Java.*

Creates a socket and connect it to the specified remote address on the specified remote port. The socket will also be bound to the local address and port suplied. The socket is configured using the socket options established for this factory.

If there is a security manager, its`checkConnect`method is called with the host address and`port`as its arguments. This could result in a SecurityException.

This method returns a socket that is*not connected*.

**Warning:**Hostname verification is not performed with this method. You MUST verify the server's identity after connecting the socket to avoid person-in-the-middle attacks.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------|
| `address` | the server network address |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the server port |
| `localAddress` | the client network address |
| `localPort` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the client port |

| Return ||
|---------------------------------------------------------------------------------|-------------|
| [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | the`Socket` |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs when creating the socket |
| `java.lang.SecurityException` | if a security manager exists and its`checkConnect`method doesn't allow the operation. |
| `java.lang.IllegalArgumentException` | if the port parameter or localPort parameter is outside the specified range of valid port values, which is between 0 and 65535, inclusive. |
| `java.lang.NullPointerException` | if`address`is null. |

### createSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createSocket(
    k: Socket!, 
    host: String!, 
    port: Int, 
    close: Boolean
): Socket!
```

**Deprecated:** *Deprecated in Java.*

Returns a socket layered over an existing socket connected to the named host, at the given port. This constructor can be used when tunneling SSL through a proxy or when negotiating the use of SSL over an existing socket. The host and port refer to the logical peer destination. This socket is configured using the socket options established for this factory.

By default, this method returns a*connected* socket and verifies the peer's certificate hostname after connecting using the [HostnameVerifier](https://developer.android.com/reference/kotlin/javax/net/ssl/HostnameVerifier.html#) obtained from`HttpsURLConnection.getDefaultHostnameVerifier()`; if this instance was created with [getInsecure(int,android.net.SSLSessionCache)](https://developer.android.com/reference/kotlin/android/net/SSLCertificateSocketFactory#getInsecure(kotlin.Int,%20android.net.SSLSessionCache)), it returns a socket that is*not connected*instead.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------|
| `s` | the existing socket |
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the server host |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the server port |
| `autoClose` | close the underlying socket when this socket is closed |

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
open static fun getDefault(handshakeTimeoutMillis: Int): SocketFactory!
```

**Deprecated:** *Deprecated in Java.*

Returns a new socket factory instance with an optional handshake timeout.

| Parameters ||
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `handshakeTimeoutMillis` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):to use for SSL connection handshake, or 0 for none. The socket timeout is reset to 0 after the handshake. |

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------------------------------|
| [SocketFactory](https://developer.android.com/reference/kotlin/javax/net/SocketFactory.html#)! | a new SSLSocketFactory with the specified parameters |

### getDefault

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getDefault(
    handshakeTimeoutMillis: Int, 
    cache: SSLSessionCache!
): SSLSocketFactory!
```

**Deprecated:** *Deprecated in Java.*

Returns a new socket factory instance with an optional handshake timeout and SSL session cache.

| Parameters ||
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `handshakeTimeoutMillis` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):to use for SSL connection handshake, or 0 for none. The socket timeout is reset to 0 after the handshake. |
| `cache` | [SSLSessionCache](https://developer.android.com/reference/kotlin/android/net/SSLSessionCache)!:The [SSLSessionCache](https://developer.android.com/reference/kotlin/android/net/SSLSessionCache) to use, or null for no cache. |

| Return ||
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| [SSLSocketFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocketFactory.html#)! | a new SSLSocketFactory with the specified parameters |

### getDefaultCipherSuites

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDefaultCipherSuites(): Array<String!>!
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | array of the cipher suites enabled by default |

### getInsecure

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInsecure(
    handshakeTimeoutMillis: Int, 
    cache: SSLSessionCache!
): SSLSocketFactory!
```

**Deprecated:** *Deprecated in Java.*

Returns a new instance of a socket factory with all SSL security checks disabled, using an optional handshake timeout and SSL session cache.

**Warning:**Sockets created using this factory are vulnerable to person-in-the-middle attacks!

| Parameters ||
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `handshakeTimeoutMillis` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):to use for SSL connection handshake, or 0 for none. The socket timeout is reset to 0 after the handshake. |
| `cache` | [SSLSessionCache](https://developer.android.com/reference/kotlin/android/net/SSLSessionCache)!:The [SSLSessionCache](https://developer.android.com/reference/kotlin/android/net/SSLSessionCache) to use, or null for no cache. |

| Return ||
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [SSLSocketFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocketFactory.html#)! | an insecure SSLSocketFactory with the specified parameters |

### getNpnSelectedProtocol

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNpnSelectedProtocol(socket: Socket!): ByteArray!
```

**Deprecated:** *Deprecated in Java.*

Returns the [Next Protocol Negotiation (NPN)](http://technotes.googlecode.com/git/nextprotoneg.html) protocol selected by client and server, or null if no protocol was negotiated.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------|
| `socket` | [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)!:a socket created by this factory. |

| Exceptions ||
|--------------------------------------|------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the socket was not created by this factory. |

### getSupportedCipherSuites

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSupportedCipherSuites(): Array<String!>!
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | an array of cipher suite names |

### setHostname

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setHostname(
    socket: Socket!, 
    hostName: String!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Turns on [Server Name Indication (SNI)](http://tools.ietf.org/html/rfc6066#section-3) on a given socket.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------|
| `socket` | [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)!:a socket created by this factory. |
| `hostName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the desired SNI hostname, null to disable. |

| Exceptions ||
|--------------------------------------|------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the socket was not created by this factory. |

### setKeyManagers

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setKeyManagers(keyManagers: Array<KeyManager!>!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the [KeyManager](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyManager.html#) s to be used for connections made by this factory. 

### setNpnProtocols

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setNpnProtocols(npnProtocols: Array<ByteArray!>!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the [Next Protocol Negotiation (NPN)](https://tools.ietf.org/id/draft-agl-tls-nextprotoneg-03.html) protocols that this peer is interested in.

For servers this is the sequence of protocols to advertise as supported, in order of preference. This list is sent unencrypted to all clients that support NPN.

For clients this is a list of supported protocols to match against the server's list. If there is no protocol supported by both client and server then the first protocol in the client's list will be selected. The order of the client's protocols is otherwise insignificant.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `npnProtocols` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!\>!:a non-empty list of protocol byte arrays. All arrays must be non-empty and of length less than 256. |

### setTrustManagers

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTrustManagers(trustManager: Array<TrustManager!>!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the [TrustManager](https://developer.android.com/reference/kotlin/javax/net/ssl/TrustManager.html#) s to be used for connections made by this factory. 

### setUseSessionTickets

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setUseSessionTickets(
    socket: Socket!, 
    useSessionTickets: Boolean
): Unit
```

**Deprecated:** *Deprecated in Java.*

Enables [session ticket](http://tools.ietf.org/html/rfc5077#section-3.2) support on the given socket.

| Parameters ||
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `socket` | [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)!:a socket created by this factory |
| `useSessionTickets` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`to enable session ticket support on this socket. |

| Exceptions ||
|--------------------------------------|------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the socket was not created by this factory. |
