# SSLContextSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SSLContextSpi

```
abstract class SSLContextSpi
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.net.ssl.SSLContextSpi](../javax/net/ssl/SSLContextSpi.md) |

This class defines the *Service Provider Interface* (**SPI** ) for the `SSLContext` class.

All the abstract methods in this class must be implemented by each cryptographic service provider who wishes to supply the implementation of a particular SSL context.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------|---|
| [SSLContextSpi](../javax/net/ssl/SSLContextSpi.md))`()` <br /> |

| Protected methods ||
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [SSLEngine](../javax/net/ssl/SSLEngine.md)! | [engineCreateSSLEngine](../javax/net/ssl/SSLContextSpi.md))`()` Creates a new `SSLEngine` using this context. |
| abstract [SSLEngine](../javax/net/ssl/SSLEngine.md)! | [engineCreateSSLEngine](../javax/net/ssl/SSLContextSpi.md))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a `SSLEngine` using this context. |
| abstract [SSLSessionContext](../javax/net/ssl/SSLSessionContext.md)! | [engineGetClientSessionContext](../javax/net/ssl/SSLContextSpi.md))`()` Returns a client `SSLSessionContext` object for this context. |
| --- | --- |
| open [SSLParameters](../javax/net/ssl/SSLParameters.md)! | [engineGetDefaultSSLParameters](../javax/net/ssl/SSLContextSpi.md))`()` Returns a copy of the SSLParameters indicating the default settings for this SSL context. |
| abstract [SSLSessionContext](../javax/net/ssl/SSLSessionContext.md)! | [engineGetServerSessionContext](../javax/net/ssl/SSLContextSpi.md))`()` Returns a server `SSLSessionContext` object for this context. |
| abstract [SSLServerSocketFactory](../javax/net/ssl/SSLServerSocketFactory.md)! | [engineGetServerSocketFactory](../javax/net/ssl/SSLContextSpi.md))`()` Returns a `ServerSocketFactory` object for this context. |
| --- | --- |
| abstract [SSLSocketFactory](../javax/net/ssl/SSLSocketFactory.md)! | [engineGetSocketFactory](../javax/net/ssl/SSLContextSpi.md))`()` Returns a `SocketFactory` object for this context. |
| open [SSLParameters](../javax/net/ssl/SSLParameters.md)! | [engineGetSupportedSSLParameters](../javax/net/ssl/SSLContextSpi.md))`()` Returns a copy of the SSLParameters indicating the maximum supported settings for this SSL context. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInit](../javax/net/ssl/SSLContextSpi.md))`(`km:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [KeyManager](../javax/net/ssl/KeyManager.md)!>!`, `tm:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [TrustManager](../javax/net/ssl/TrustManager.md)!>!`, `sr:` ` [SecureRandom](../java/security/SecureRandom.md)!`)` Initializes this context. |
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

Applications using this factory method are providing no hints for an internal session reuse strategy. If hints are desired, [engineCreateSSLEngine(java.lang.String,int)](../javax/net/ssl/SSLContextSpi.md)) should be used instead.

Some cipher suites (such as Kerberos) require remote hostname information, in which case this factory method should not be used.

| Return ||
|--------------------------------------------------------------------------------------|------------------------|
| [SSLEngine](../javax/net/ssl/SSLEngine.md)! | the `SSLEngine` Object |

| Exceptions ||
|-----------------------------------|------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the SSLContextImpl requires initialization and the `engineInit()` has not been called |

**See Also**

- [javax.net.ssl.SSLContext#createSSLEngine()](../javax/net/ssl/SSLContext.md)) 

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
| [SSLEngine](../javax/net/ssl/SSLEngine.md)! | the `SSLEngine` Object |

| Exceptions ||
|-----------------------------------|------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the SSLContextImpl requires initialization and the `engineInit()` has not been called |

**See Also**

- [javax.net.ssl.SSLContext#createSSLEngine(String, int)](../javax/net/ssl/SSLContext.md)) 

### engineGetClientSessionContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineGetClientSessionContext(): SSLSessionContext!
```

Returns a client `SSLSessionContext` object for this context.

| Return ||
|------------------------------------------------------------------------------------------------------|--------------------------------|
| [SSLSessionContext](../javax/net/ssl/SSLSessionContext.md)! | the `SSLSessionContext` object |

**See Also**

- [javax.net.ssl.SSLContext#getClientSessionContext()](../javax/net/ssl/SSLContext.md)) 

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
| [SSLParameters](../javax/net/ssl/SSLParameters.md)! | a copy of the SSLParameters object with the default settings |

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
| [SSLSessionContext](../javax/net/ssl/SSLSessionContext.md)! | the `SSLSessionContext` object |

**See Also**

- [javax.net.ssl.SSLContext#getServerSessionContext()](../javax/net/ssl/SSLContext.md)) 

### engineGetServerSocketFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineGetServerSocketFactory(): SSLServerSocketFactory!
```

Returns a `ServerSocketFactory` object for this context.

| Return ||
|----------------------------------------------------------------------------------------------------------------|----------------------------------|
| [SSLServerSocketFactory](../javax/net/ssl/SSLServerSocketFactory.md)! | the `ServerSocketFactory` object |

| Exceptions ||
|-----------------------------------|------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the SSLContextImpl requires initialization and the `engineInit()` has not been called |

**See Also**

- [javax.net.ssl.SSLContext#getServerSocketFactory()](../javax/net/ssl/SSLContext.md)) 

### engineGetSocketFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineGetSocketFactory(): SSLSocketFactory!
```

Returns a `SocketFactory` object for this context.

| Return ||
|----------------------------------------------------------------------------------------------------|----------------------------|
| [SSLSocketFactory](../javax/net/ssl/SSLSocketFactory.md)! | the `SocketFactory` object |

| Exceptions ||
|-----------------------------------|------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the SSLContextImpl requires initialization and the `engineInit()` has not been called |

**See Also**

- [javax.net.ssl.SSLContext#getSocketFactory()](../javax/net/ssl/SSLContext.md)) 

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
| [SSLParameters](../javax/net/ssl/SSLParameters.md)! | a copy of the SSLParameters object with the maximum supported settings |

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
| `km` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [KeyManager](../javax/net/ssl/KeyManager.md)!\>!: the sources of authentication keys |
| `tm` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [TrustManager](../javax/net/ssl/TrustManager.md)!\>!: the sources of peer authentication trust decisions |
| `sr` | [SecureRandom](../java/security/SecureRandom.md)!: the source of randomness |
| --- | --- |

| Exceptions ||
|----------------------------------------|-------------------------|
| `java.security.KeyManagementException` | if this operation fails |

**See Also**
