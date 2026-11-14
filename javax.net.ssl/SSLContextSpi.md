# SSLContextSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SSLContextSpi

```
abstract class SSLContextSpi
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.net.ssl.SSLContextSpi](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContextSpi#) |

This class defines the *Service Provider Interface* (**SPI** ) for the `SSLContext` class.

All the abstract methods in this class must be implemented by each cryptographic service provider who wishes to supply the implementation of a particular SSL context.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------|---|
| [SSLContextSpi](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContextSpi#SSLContextSpi())`()` <br /> |

| Protected methods ||
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [SSLEngine](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine)! | [engineCreateSSLEngine](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContextSpi#engineCreateSSLEngine())`()` Creates a new `SSLEngine` using this context. |
| abstract [SSLEngine](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine)! | [engineCreateSSLEngine](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContextSpi#engineCreateSSLEngine(kotlin.String,%20kotlin.Int))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a `SSLEngine` using this context. |
| abstract [SSLSessionContext](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSessionContext)! | [engineGetClientSessionContext](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContextSpi#engineGetClientSessionContext())`()` Returns a client `SSLSessionContext` object for this context. |
| --- | --- |
| open [SSLParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters)! | [engineGetDefaultSSLParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContextSpi#engineGetDefaultSSLParameters())`()` Returns a copy of the SSLParameters indicating the default settings for this SSL context. |
| abstract [SSLSessionContext](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSessionContext)! | [engineGetServerSessionContext](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContextSpi#engineGetServerSessionContext())`()` Returns a server `SSLSessionContext` object for this context. |
| abstract [SSLServerSocketFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocketFactory)! | [engineGetServerSocketFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContextSpi#engineGetServerSocketFactory())`()` Returns a `ServerSocketFactory` object for this context. |
| --- | --- |
| abstract [SSLSocketFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocketFactory)! | [engineGetSocketFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContextSpi#engineGetSocketFactory())`()` Returns a `SocketFactory` object for this context. |
| open [SSLParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters)! | [engineGetSupportedSSLParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContextSpi#engineGetSupportedSSLParameters())`()` Returns a copy of the SSLParameters indicating the maximum supported settings for this SSL context. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInit](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContextSpi#engineInit(kotlin.Array,%20kotlin.Array,%20java.security.SecureRandom))`(`km:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [KeyManager](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyManager)!>!`, `tm:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [TrustManager](https://developer.android.com/reference/kotlin/javax/net/ssl/TrustManager)!>!`, `sr:` ` [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom.html#)!`)` Initializes this context. |
| --- | --- |

## Public constructors

### SSLContextSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SSLContextSpi()
```

## Protected methods

### engineCreateSSLEngine

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineCreateSSLEngine(): SSLEngine!
```

Creates a new `SSLEngine` using this context.

Applications using this factory method are providing no hints for an internal session reuse strategy. If hints are desired, [engineCreateSSLEngine(java.lang.String,int)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContextSpi#engineCreateSSLEngine(kotlin.String,%20kotlin.Int)) should be used instead.

Some cipher suites (such as Kerberos) require remote hostname information, in which case this factory method should not be used.

| Return ||
|--------------------------------------------------------------------------------------|------------------------|
| [SSLEngine](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine)! | the `SSLEngine` Object |

| Exceptions ||
|-----------------------------------|------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the SSLContextImpl requires initialization and the `engineInit()` has not been called |

**See Also**

- [javax.net.ssl.SSLContext#createSSLEngine()](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#createSSLEngine()) 

### engineCreateSSLEngine

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineCreateSSLEngine(
    host: String!, 
    port: Int
): SSLEngine!
```

Creates a `SSLEngine` using this context.

Applications using this factory method are providing hints for an internal session reuse strategy.

Some cipher suites (such as Kerberos) require remote hostname information, in which case peerHost needs to be specified.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------|
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the non-authoritative name of the host |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the non-authoritative port |

| Return ||
|--------------------------------------------------------------------------------------|------------------------|
| [SSLEngine](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine)! | the `SSLEngine` Object |

| Exceptions ||
|-----------------------------------|------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the SSLContextImpl requires initialization and the `engineInit()` has not been called |

**See Also**

- [javax.net.ssl.SSLContext#createSSLEngine(String, int)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#createSSLEngine(kotlin.String,%20kotlin.Int)) 

### engineGetClientSessionContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineGetClientSessionContext(): SSLSessionContext!
```

Returns a client `SSLSessionContext` object for this context.

| Return ||
|------------------------------------------------------------------------------------------------------|--------------------------------|
| [SSLSessionContext](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSessionContext)! | the `SSLSessionContext` object |

**See Also**

- [javax.net.ssl.SSLContext#getClientSessionContext()](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#getClientSessionContext()) 

### engineGetDefaultSSLParameters

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun engineGetDefaultSSLParameters(): SSLParameters!
```

Returns a copy of the SSLParameters indicating the default settings for this SSL context.

The parameters will always have the ciphersuite and protocols arrays set to non-null values.

The default implementation obtains the parameters from an SSLSocket created by calling the javax.net.SocketFactory#createSocket method of this context's SocketFactory.

| Return ||
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [SSLParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters)! | a copy of the SSLParameters object with the default settings |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the default SSL parameters could not be obtained. |

### engineGetServerSessionContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineGetServerSessionContext(): SSLSessionContext!
```

Returns a server `SSLSessionContext` object for this context.

| Return ||
|------------------------------------------------------------------------------------------------------|--------------------------------|
| [SSLSessionContext](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSessionContext)! | the `SSLSessionContext` object |

**See Also**

- [javax.net.ssl.SSLContext#getServerSessionContext()](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#getServerSessionContext()) 

### engineGetServerSocketFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineGetServerSocketFactory(): SSLServerSocketFactory!
```

Returns a `ServerSocketFactory` object for this context.

| Return ||
|----------------------------------------------------------------------------------------------------------------|----------------------------------|
| [SSLServerSocketFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocketFactory)! | the `ServerSocketFactory` object |

| Exceptions ||
|-----------------------------------|------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the SSLContextImpl requires initialization and the `engineInit()` has not been called |

**See Also**

- [javax.net.ssl.SSLContext#getServerSocketFactory()](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#getServerSocketFactory()) 

### engineGetSocketFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineGetSocketFactory(): SSLSocketFactory!
```

Returns a `SocketFactory` object for this context.

| Return ||
|----------------------------------------------------------------------------------------------------|----------------------------|
| [SSLSocketFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocketFactory)! | the `SocketFactory` object |

| Exceptions ||
|-----------------------------------|------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the SSLContextImpl requires initialization and the `engineInit()` has not been called |

**See Also**

- [javax.net.ssl.SSLContext#getSocketFactory()](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#getSocketFactory()) 

### engineGetSupportedSSLParameters

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun engineGetSupportedSSLParameters(): SSLParameters!
```

Returns a copy of the SSLParameters indicating the maximum supported settings for this SSL context.

The parameters will always have the ciphersuite and protocols arrays set to non-null values.

The default implementation obtains the parameters from an SSLSocket created by calling the javax.net.SocketFactory#createSocket method of this context's SocketFactory.

| Return ||
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [SSLParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters)! | a copy of the SSLParameters object with the maximum supported settings |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the supported SSL parameters could not be obtained. |

### engineInit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineInit(
    km: Array<KeyManager!>!, 
    tm: Array<TrustManager!>!, 
    sr: SecureRandom!
): Unit
```

Initializes this context.

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `km` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [KeyManager](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyManager)!\>!: the sources of authentication keys |
| `tm` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [TrustManager](https://developer.android.com/reference/kotlin/javax/net/ssl/TrustManager)!\>!: the sources of peer authentication trust decisions |
| `sr` | [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom.html#)!: the source of randomness |
| --- | --- |

| Exceptions ||
|----------------------------------------|-------------------------|
| `java.security.KeyManagementException` | if this operation fails |

**See Also**
