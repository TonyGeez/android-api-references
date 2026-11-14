# SSLServerSocketFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SSLServerSocketFactory

```
abstract class SSLServerSocketFactory : ServerSocketFactory
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [javax.net.ServerSocketFactory](../javax/net/ServerSocketFactory.md) ||
| | ↳ | [javax.net.ssl.SSLServerSocketFactory](../javax/net/ssl/SSLServerSocketFactory.md) |

`SSLServerSocketFactory`s create`SSLServerSocket`s.

## Summary

| Protected constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SSLServerSocketFactory](../javax/net/ssl/SSLServerSocketFactory.md))`()` Constructor is used only by subclasses. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [ServerSocketFactory](../javax/net/ServerSocketFactory.md)! | [getDefault](../javax/net/ssl/SSLServerSocketFactory.md))`()` Returns the default SSL server socket factory. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getDefaultCipherSuites](../javax/net/ssl/SSLServerSocketFactory.md))`()` Returns the list of cipher suites which are enabled by default. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getSupportedCipherSuites](../javax/net/ssl/SSLServerSocketFactory.md))`()` Returns the names of the cipher suites which could be enabled for use on an SSL connection created by this factory. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [ServerSocketFactory](../javax/net/ServerSocketFactory.md) |---------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ServerSocket](../java/net/ServerSocket.md)! | [createServerSocket](../javax/net/ServerSocketFactory.md))`()` <br /> Returns an unbound server socket. The socket is configured with the socket options (such as accept timeout) given to this factory. <br /> | | [ServerSocket](../java/net/ServerSocket.md)! | [createServerSocket](../javax/net/ServerSocketFactory.md))`(`port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns a server socket bound to the specified port. The socket is configured with the socket options (such as accept timeout) given to this factory. If there is a security manager, its`checkListen`method is called with the`port`argument as its argument to ensure the operation is allowed. This could result in a SecurityException. <br /> | | [ServerSocket](../java/net/ServerSocket.md)! | [createServerSocket](../javax/net/ServerSocketFactory.md))`(`port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `backlog:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns a server socket bound to the specified port, and uses the specified connection backlog. The socket is configured with the socket options (such as accept timeout) given to this factory. The`backlog`argument must be a positive value greater than 0. If the value passed if equal or less than 0, then the default value will be assumed. If there is a security manager, its`checkListen`method is called with the`port`argument as its argument to ensure the operation is allowed. This could result in a SecurityException. <br /> | | [ServerSocket](../java/net/ServerSocket.md)! | [createServerSocket](../javax/net/ServerSocketFactory.md))`(`port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `backlog:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `ifAddress:` ` [InetAddress](../java/net/InetAddress.md)!`)` <br /> Returns a server socket bound to the specified port, with a specified listen backlog and local IP. The`ifAddress`argument can be used on a multi-homed host for a`ServerSocket`that will only accept connect requests to one of its addresses. If`ifAddress`is null, it will accept connections on all local addresses. The socket is configured with the socket options (such as accept timeout) given to this factory. The`backlog`argument must be a positive value greater than 0. If the value passed if equal or less than 0, then the default value will be assumed. If there is a security manager, its`checkListen`method is called with the`port`argument as its argument to ensure the operation is allowed. This could result in a SecurityException. <br /> | ||

## Protected constructors

### SSLServerSocketFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected SSLServerSocketFactory()
```

Constructor is used only by subclasses.

## Public methods

### getDefault

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getDefault(): ServerSocketFactory!
```

Returns the default SSL server socket factory.

The first time this method is called, the security property "ssl.ServerSocketFactory.provider" is examined. If it is non-null, a class by that name is loaded and instantiated. If that is successful and the object is an instance of SSLServerSocketFactory, it is made the default SSL server socket factory.

Otherwise, this method returns`SSLContext.getDefault().getServerSocketFactory()`. If that call fails, an inoperative factory is returned.

| Return ||
|------------------------------------------------------------------------------------------------------------|----------------------------------|
| [ServerSocketFactory](../javax/net/ServerSocketFactory.md)! | the default`ServerSocketFactory` |

**See Also**

- [javax.net.ssl.SSLContext#getDefault](../javax/net/ssl/SSLContext.md)) 

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

- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocketFactory#getSupportedCipherSuites()> 

### getSupportedCipherSuites

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSupportedCipherSuites(): Array<String!>!
```

Returns the names of the cipher suites which could be enabled for use on an SSL connection created by this factory. Normally, only a subset of these will actually be enabled by default, since this list may include cipher suites which do not meet quality of service requirements for those defaults. Such cipher suites are useful in specialized applications.

Applications should not blindly enable all supported cipher suites. The supported cipher suites can include signaling cipher suite values that can cause connection problems if enabled inappropriately.

The proper way to use this method is to either check if a specific cipher suite is supported via`Arrays.asList(getSupportedCipherSuites()).contains(...)`or to filter a desired list of cipher suites to only the supported ones via`desiredSuiteSet.retainAll(Arrays.asList(getSupportedCipherSuites()))`.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | an array of cipher suite names |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocketFactory#getDefaultCipherSuites()>
