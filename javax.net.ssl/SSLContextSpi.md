# SSLContextSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SSLContextSpi

```
abstract class SSLContextSpi
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.net.ssl.SSLContextSpi](SSLContextSpi.md) |

This class defines the *Service Provider Interface* (**SPI** ) for the `SSLContext` class.

All the abstract methods in this class must be implemented by each cryptographic service provider who wishes to supply the implementation of a particular SSL context.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------|---|
| [SSLContextSpi](SSLContextSpi.md))`()` <br /> |

| Protected methods ||
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [SSLEngine](SSLEngine.md)! | [engineCreateSSLEngine](SSLContextSpi.md))`()` Creates a new `SSLEngine` using this context. |
| abstract [SSLEngine](SSLEngine.md)! | [engineCreateSSLEngine](SSLContextSpi.md))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a `SSLEngine` using this context. |
| abstract [SSLSessionContext](SSLSessionContext.md)! | [engineGetClientSessionContext](SSLContextSpi.md))`()` Returns a client `SSLSessionContext` object for this context. |
| --- | --- |
| open [SSLParameters](SSLParameters.md)! | [engineGetDefaultSSLParameters](SSLContextSpi.md))`()` Returns a copy of the SSLParameters indicating the default settings for this SSL context. |
| abstract [SSLSessionContext](SSLSessionContext.md)! | [engineGetServerSessionContext](SSLContextSpi.md))`()` Returns a server `SSLSessionContext` object for this context. |
| abstract [SSLServerSocketFactory](SSLServerSocketFactory.md)! | [engineGetServerSocketFactory](SSLContextSpi.md))`()` Returns a `ServerSocketFactory` object for this context. |
| --- | --- |
| abstract [SSLSocketFactory](SSLSocketFactory.md)! | [engineGetSocketFactory](SSLContextSpi.md))`()` Returns a `SocketFactory` object for this context. |
| open [SSLParameters](SSLParameters.md)! | [engineGetSupportedSSLParameters](SSLContextSpi.md))`()` Returns a copy of the SSLParameters indicating the maximum supported settings for this SSL context. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInit](SSLContextSpi.md))`(`km:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [KeyManager](KeyManager.md)!>!`, `tm:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [TrustManager](TrustManager.md)!>!`, `sr:` ` [SecureRandom](../java.security/SecureRandom.md)!`)` Initializes this context. |
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

Applications using this factory method are providing no hints for an internal session reuse strategy. If hints are desired, [engineCreateSSLEngine(java.lang.String,int)](SSLContextSpi.md)) should be used instead.

Some cipher suites (such as Kerberos) require remote hostname information, in which case this factory method should not be used.

| Return ||
|--------------------------------------------------------------------------------------|------------------------|
| [SSLEngine](SSLEngine.md)! | the `SSLEngine` Object |

| Exceptions ||
|-----------------------------------|------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the SSLContextImpl requires initialization and the `engineInit()` has not been called |

**See Also**

- [javax.net.ssl.SSLContext#createSSLEngine()](SSLContext.md)) 

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
| [SSLEngine](SSLEngine.md)! | the `SSLEngine` Object |

| Exceptions ||
|-----------------------------------|------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the SSLContextImpl requires initialization and the `engineInit()` has not been called |

**See Also**

- [javax.net.ssl.SSLContext#createSSLEngine(String, int)](SSLContext.md)) 

### engineGetClientSessionContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineGetClientSessionContext(): SSLSessionContext!
```

Returns a client `SSLSessionContext` object for this context.

| Return ||
|------------------------------------------------------------------------------------------------------|--------------------------------|
| [SSLSessionContext](SSLSessionContext.md)! | the `SSLSessionContext` object |

**See Also**

- [javax.net.ssl.SSLContext#getClientSessionContext()](SSLContext.md)) 

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
| [SSLParameters](SSLParameters.md)! | a copy of the SSLParameters object with the default settings |

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
| [SSLSessionContext](SSLSessionContext.md)! | the `SSLSessionContext` object |

**See Also**

- [javax.net.ssl.SSLContext#getServerSessionContext()](SSLContext.md)) 

### engineGetServerSocketFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineGetServerSocketFactory(): SSLServerSocketFactory!
```

Returns a `ServerSocketFactory` object for this context.

| Return ||
|----------------------------------------------------------------------------------------------------------------|----------------------------------|
| [SSLServerSocketFactory](SSLServerSocketFactory.md)! | the `ServerSocketFactory` object |

| Exceptions ||
|-----------------------------------|------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the SSLContextImpl requires initialization and the `engineInit()` has not been called |

**See Also**

- [javax.net.ssl.SSLContext#getServerSocketFactory()](SSLContext.md)) 

### engineGetSocketFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineGetSocketFactory(): SSLSocketFactory!
```

Returns a `SocketFactory` object for this context.

| Return ||
|----------------------------------------------------------------------------------------------------|----------------------------|
| [SSLSocketFactory](SSLSocketFactory.md)! | the `SocketFactory` object |

| Exceptions ||
|-----------------------------------|------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the SSLContextImpl requires initialization and the `engineInit()` has not been called |

**See Also**

- [javax.net.ssl.SSLContext#getSocketFactory()](SSLContext.md)) 

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
| [SSLParameters](SSLParameters.md)! | a copy of the SSLParameters object with the maximum supported settings |

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
| `km` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [KeyManager](KeyManager.md)!\>!: the sources of authentication keys |
| `tm` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [TrustManager](TrustManager.md)!\>!: the sources of peer authentication trust decisions |
| `sr` | [SecureRandom](../java.security/SecureRandom.md)!: the source of randomness |
| --- | --- |

| Exceptions ||
|----------------------------------------|-------------------------|
| `java.security.KeyManagementException` | if this operation fails |

**See Also**
