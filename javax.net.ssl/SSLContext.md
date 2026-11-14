# SSLContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SSLContext

```
open class SSLContext
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.net.ssl.SSLContext](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#) |

Instances of this class represent a secure socket protocol implementation which acts as a factory for secure socket factories or`SSLEngine`s. This class is initialized with an optional set of key and trust managers and source of secure random bytes.

Android provides the following`SSLContext`protocols:

| Algorithm | Supported API Levels |
|-----------|----------------------|
| Default | 10+ |
| SSL | 10+ |
| SSLv3 | 10-25 |
| --- | --- |
| TLS | 1+ |
| TLSv1 | 10+ |
| TLSv1.1 | 16+ |
| --- | --- |
| TLSv1.2 | 16+ |
| TLSv1.3 | 29+ |

This protocol is described in the [SSLContext section](https://docs.oracle.com/javase/8/docs/technotes/guides/security/StandardNames.html#SSLContext) of the Java Cryptography Architecture Standard Algorithm Name Documentation.

## Summary

| Protected constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SSLContext](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#SSLContext(javax.net.ssl.SSLContextSpi,%20java.security.Provider,%20kotlin.String))`(`contextSpi:` ` [SSLContextSpi](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContextSpi)!`, `provider:` ` [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)!`, `protocol:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates an SSLContext object. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SSLEngine](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine)! | [createSSLEngine](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#createSSLEngine())`()` Creates a new`SSLEngine`using this context. |
| [SSLEngine](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine)! | [createSSLEngine](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#createSSLEngine(kotlin.String,%20kotlin.Int))`(`peerHost:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `peerPort:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new`SSLEngine`using this context using advisory peer information. |
| [SSLSessionContext](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSessionContext)! | [getClientSessionContext](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#getClientSessionContext())`()` Returns the client session context, which represents the set of SSL sessions available for use during the handshake phase of client-side SSL sockets. |
| --- | --- |
| openstatic [SSLContext](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#)! | [getDefault](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#getDefault())`()` Returns the default SSL context. |
| [SSLParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters)! | [getDefaultSSLParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#getDefaultSSLParameters())`()` Returns a copy of the SSLParameters indicating the default settings for this SSL context. |
| openstatic [SSLContext](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#)! | [getInstance](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#getInstance(kotlin.String))`(`protocol:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a`SSLContext`object that implements the specified secure socket protocol. |
| --- | --- |
| openstatic [SSLContext](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#)! | [getInstance](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#getInstance(kotlin.String,%20kotlin.String))`(`protocol:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a`SSLContext`object that implements the specified secure socket protocol. |
| openstatic [SSLContext](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#)! | [getInstance](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#getInstance(kotlin.String,%20java.security.Provider))`(`protocol:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `provider:` ` [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)!`)` Returns a`SSLContext`object that implements the specified secure socket protocol. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getProtocol](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#getProtocol())`()` Returns the protocol name of this`SSLContext`object. |
| --- | --- |
| [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)! | [getProvider](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#getProvider())`()` Returns the provider of this`SSLContext`object. |
| [SSLSessionContext](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSessionContext)! | [getServerSessionContext](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#getServerSessionContext())`()` Returns the server session context, which represents the set of SSL sessions available for use during the handshake phase of server-side SSL sockets. |
| [SSLServerSocketFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocketFactory)! | [getServerSocketFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#getServerSocketFactory())`()` Returns a`ServerSocketFactory`object for this context. |
| --- | --- |
| [SSLSocketFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocketFactory)! | [getSocketFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#getSocketFactory())`()` Returns a`SocketFactory`object for this context. |
| [SSLParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters)! | [getSupportedSSLParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#getSupportedSSLParameters())`()` Returns a copy of the SSLParameters indicating the supported settings for this SSL context. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#init(kotlin.Array,%20kotlin.Array,%20java.security.SecureRandom))`(`km:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [KeyManager](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyManager)!>!`, `tm:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [TrustManager](https://developer.android.com/reference/kotlin/javax/net/ssl/TrustManager)!>!`, `random:` ` [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom.html#)!`)` Initializes this context. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDefault](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#setDefault(javax.net.ssl.SSLContext))`(`context:` ` [SSLContext](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#)!`)` Sets the default SSL context. |

## Protected constructors

### SSLContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected SSLContext(
    contextSpi: SSLContextSpi!, 
    provider: Provider!, 
    protocol: String!)
```

Creates an SSLContext object.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------|
| `contextSpi` | [SSLContextSpi](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContextSpi)!:the delegate |
| `provider` | [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)!:the provider |
| `protocol` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the protocol |
| --- | --- |

## Public methods

### createSSLEngine

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun createSSLEngine(): SSLEngine!
```

Creates a new`SSLEngine`using this context.

Applications using this factory method are providing no hints for an internal session reuse strategy. If hints are desired, [createSSLEngine(java.lang.String,int)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#createSSLEngine(kotlin.String,%20kotlin.Int))should be used instead.

Some cipher suites (such as Kerberos) require remote hostname information, in which case this factory method should not be used.

| Return ||
|--------------------------------------------------------------------------------------|----------------------|
| [SSLEngine](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine)! | the`SSLEngine`object |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the underlying provider does not implement the operation. |
| `java.lang.IllegalStateException` | if the SSLContextImpl requires initialization and the`init()`has not been called |

### createSSLEngine

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun createSSLEngine(
    peerHost: String!, 
    peerPort: Int
): SSLEngine!
```

Creates a new`SSLEngine`using this context using advisory peer information.

Applications using this factory method are providing hints for an internal session reuse strategy.

Some cipher suites (such as Kerberos) require remote hostname information, in which case peerHost needs to be specified.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------|
| `peerHost` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the non-authoritative name of the host |
| `peerPort` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the non-authoritative port |

| Return ||
|--------------------------------------------------------------------------------------|--------------------------|
| [SSLEngine](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine)! | the new`SSLEngine`object |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the underlying provider does not implement the operation. |
| `java.lang.IllegalStateException` | if the SSLContextImpl requires initialization and the`init()`has not been called |

### getClientSessionContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getClientSessionContext(): SSLSessionContext!
```

Returns the client session context, which represents the set of SSL sessions available for use during the handshake phase of client-side SSL sockets.

This context may be unavailable in some environments, in which case this method returns null. For example, when the underlying SSL provider does not provide an implementation of SSLSessionContext interface, this method returns null. A non-null session context is returned otherwise.

| Return ||
|------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [SSLSessionContext](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSessionContext)! | client session context bound to this SSL context |

### getDefault

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getDefault(): SSLContext!
```

Returns the default SSL context.

If a default context was set using the [SSLContext.setDefault()](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#setDefault(javax.net.ssl.SSLContext))method, it is returned. Otherwise, the first call of this method triggers the call`SSLContext.getInstance("Default")`. If successful, that object is made the default SSL context and returned.

The default context is immediately usable and does not require [initialization](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#init(kotlin.Array,%20kotlin.Array,%20java.security.SecureRandom)).

| Return ||
|-----------------------------------------------------------------------------------------|-------------------------|
| [SSLContext](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#)! | the default SSL context |

| Exceptions ||
|------------------------------------------|--------------------------------------------------------|
| `java.security.NoSuchAlgorithmException` | if the javax.net.ssl.SSLContext#getInstance call fails |

### getDefaultSSLParameters

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDefaultSSLParameters(): SSLParameters!
```

Returns a copy of the SSLParameters indicating the default settings for this SSL context.

The parameters will always have the ciphersuites and protocols arrays set to non-null values.

| Return ||
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [SSLParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters)! | a copy of the SSLParameters object with the default settings |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the default SSL parameters could not be obtained. |

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(protocol: String!): SSLContext!
```

Returns a`SSLContext`object that implements the specified secure socket protocol.

This method traverses the list of registered security Providers, starting with the most preferred Provider. A new SSLContext object encapsulating the SSLContextSpi implementation from the first Provider that supports the specified protocol is returned.

Note that the list of registered providers may be retrieved via the [Security.getProviders()](https://developer.android.com/reference/kotlin/java/security/Security.html#getProviders())method.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `protocol` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the standard name of the requested protocol. See the SSLContext section in the [Java Cryptography Architecture Standard Algorithm Name Documentation](https://docs.oracle.com/javase/8/docs/technotes/guides/security/StandardNames.html#SSLContext) for information about standard protocol names. |

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------|
| [SSLContext](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#)! | the new`SSLContext`object. |

| Exceptions ||
|------------------------------------------|------------------------------------------------------------------------------------|
| `java.security.NoSuchAlgorithmException` | if no Provider supports a SSLContextSpi implementation for the specified protocol. |
| `java.lang.NullPointerException` | if protocol is null. |

**See Also**

- [java.security.Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    protocol: String!, 
    provider: String!
): SSLContext!
```

Returns a`SSLContext`object that implements the specified secure socket protocol.

A new SSLContext object encapsulating the SSLContextSpi implementation from the specified provider is returned. The specified provider must be registered in the security provider list.

Note that the list of registered providers may be retrieved via the [Security.getProviders()](https://developer.android.com/reference/kotlin/java/security/Security.html#getProviders())method.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `protocol` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the standard name of the requested protocol. See the SSLContext section in the [Java Cryptography Architecture Standard Algorithm Name Documentation](https://docs.oracle.com/javase/8/docs/technotes/guides/security/StandardNames.html#SSLContext) for information about standard protocol names. |
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the provider. |

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------|
| [SSLContext](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#)! | the new`SSLContext`object. |

| Exceptions ||
|------------------------------------------|------------------------------------------------------------------------------------------------------------|
| `java.security.NoSuchAlgorithmException` | if a SSLContextSpi implementation for the specified protocol is not available from the specified provider. |
| `java.security.NoSuchProviderException` | if the specified provider is not registered in the security provider list. |
| `java.lang.IllegalArgumentException` | if the provider name is null or empty. |
| --- | --- |
| `java.lang.NullPointerException` | if protocol is null. |

**See Also**

- [java.security.Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    protocol: String!, 
    provider: Provider!
): SSLContext!
```

Returns a`SSLContext`object that implements the specified secure socket protocol.

A new SSLContext object encapsulating the SSLContextSpi implementation from the specified Provider object is returned. Note that the specified Provider object does not have to be registered in the provider list.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `protocol` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the standard name of the requested protocol. See the SSLContext section in the [Java Cryptography Architecture Standard Algorithm Name Documentation](https://docs.oracle.com/javase/8/docs/technotes/guides/security/StandardNames.html#SSLContext) for information about standard protocol names. |
| `provider` | [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)!:an instance of the provider. |

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------|
| [SSLContext](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#)! | the new`SSLContext`object. |

| Exceptions ||
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| `java.security.NoSuchAlgorithmException` | if a SSLContextSpi implementation for the specified protocol is not available from the specified Provider object. |
| `java.lang.IllegalArgumentException` | if the provider is null. |
| `java.lang.NullPointerException` | if protocol is null. |
| --- | --- |

**See Also**

- [java.security.Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#) 

### getProtocol

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getProtocol(): String!
```

Returns the protocol name of this`SSLContext`object.

This is the same name that was specified in one of the`getInstance`calls that created this`SSLContext`object.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the protocol name of this`SSLContext`object. |

### getProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getProvider(): Provider!
```

Returns the provider of this`SSLContext`object.

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------|
| [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)! | the provider of this`SSLContext`object |

### getServerSessionContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getServerSessionContext(): SSLSessionContext!
```

Returns the server session context, which represents the set of SSL sessions available for use during the handshake phase of server-side SSL sockets.

This context may be unavailable in some environments, in which case this method returns null. For example, when the underlying SSL provider does not provide an implementation of SSLSessionContext interface, this method returns null. A non-null session context is returned otherwise.

| Return ||
|------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [SSLSessionContext](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSessionContext)! | server session context bound to this SSL context |

### getServerSocketFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getServerSocketFactory(): SSLServerSocketFactory!
```

Returns a`ServerSocketFactory`object for this context.

| Return ||
|----------------------------------------------------------------------------------------------------------------|--------------------------------|
| [SSLServerSocketFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocketFactory)! | the`ServerSocketFactory`object |

| Exceptions ||
|-----------------------------------|----------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the SSLContextImpl requires initialization and the`init()`has not been called |

### getSocketFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSocketFactory(): SSLSocketFactory!
```

Returns a`SocketFactory`object for this context.

| Return ||
|----------------------------------------------------------------------------------------------------|--------------------------|
| [SSLSocketFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocketFactory)! | the`SocketFactory`object |

| Exceptions ||
|-----------------------------------|----------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the SSLContextImpl requires initialization and the`init()`has not been called |

### getSupportedSSLParameters

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSupportedSSLParameters(): SSLParameters!
```

Returns a copy of the SSLParameters indicating the supported settings for this SSL context.

The parameters will always have the ciphersuites and protocols arrays set to non-null values.

| Return ||
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [SSLParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters)! | a copy of the SSLParameters object with the supported settings |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the supported SSL parameters could not be obtained. |

### init

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun init(
    km: Array<KeyManager!>!, 
    tm: Array<TrustManager!>!, 
    random: SecureRandom!
): Unit
```

Initializes this context. Either of the first two parameters may be null in which case the installed security providers will be searched for the highest priority implementation of the appropriate factory. Likewise, the secure random parameter may be null in which case the default implementation will be used.

Only the first instance of a particular key and/or trust manager implementation type in the array is used. (For example, only the first javax.net.ssl.X509KeyManager in the array will be used.)

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `km` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [KeyManager](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyManager)!\>!:the sources of authentication keys or null |
| `tm` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [TrustManager](https://developer.android.com/reference/kotlin/javax/net/ssl/TrustManager)!\>!:the sources of peer authentication trust decisions or null |
| `random` | [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom.html#)!:the source of randomness for this generator or null |
| --- | --- |

| Exceptions ||
|----------------------------------------|-------------------------|
| `java.security.KeyManagementException` | if this operation fails |

### setDefault

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun setDefault(context: SSLContext!): Unit
```

Sets the default SSL context. It will be returned by subsequent calls to [getDefault](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#getDefault()). The default context must be immediately usable and not require [initialization](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#init(kotlin.Array,%20kotlin.Array,%20java.security.SecureRandom)).

Developers are*strongly* discouraged from changing the default`SSLContext`as it is used as the Android default for secure communication by APIs like [SSLSocketFactory.getDefault()](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocketFactory#getDefault()), [SSLServerSocketFactory.getDefault()](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocketFactory#getDefault())and [HttpsURLConnection](https://developer.android.com/reference/kotlin/javax/net/ssl/HttpsURLConnection).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------|
| `context` | [SSLContext](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#)!:the SSLContext |

| Exceptions ||
|----------------------------------|-------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if context is null |
| `java.lang.SecurityException` | if a security manager exists and its`checkPermission`method does not allow`SSLPermission("setDefaultSSLContext")` |
