# SSLContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SSLContext

```
open class SSLContext
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.net.ssl.SSLContext](../javax/net/ssl/SSLContext.md) |

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
| [SSLContext](../javax/net/ssl/SSLContext.md))`(`contextSpi:` ` [SSLContextSpi](../javax/net/ssl/SSLContextSpi.md)!`, `provider:` ` [Provider](../java/security/Provider.md)!`, `protocol:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates an SSLContext object. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SSLEngine](../javax/net/ssl/SSLEngine.md)! | [createSSLEngine](../javax/net/ssl/SSLContext.md))`()` Creates a new`SSLEngine`using this context. |
| [SSLEngine](../javax/net/ssl/SSLEngine.md)! | [createSSLEngine](../javax/net/ssl/SSLContext.md))`(`peerHost:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `peerPort:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new`SSLEngine`using this context using advisory peer information. |
| [SSLSessionContext](../javax/net/ssl/SSLSessionContext.md)! | [getClientSessionContext](../javax/net/ssl/SSLContext.md))`()` Returns the client session context, which represents the set of SSL sessions available for use during the handshake phase of client-side SSL sockets. |
| --- | --- |
| openstatic [SSLContext](../javax/net/ssl/SSLContext.md)! | [getDefault](../javax/net/ssl/SSLContext.md))`()` Returns the default SSL context. |
| [SSLParameters](../javax/net/ssl/SSLParameters.md)! | [getDefaultSSLParameters](../javax/net/ssl/SSLContext.md))`()` Returns a copy of the SSLParameters indicating the default settings for this SSL context. |
| openstatic [SSLContext](../javax/net/ssl/SSLContext.md)! | [getInstance](../javax/net/ssl/SSLContext.md))`(`protocol:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a`SSLContext`object that implements the specified secure socket protocol. |
| --- | --- |
| openstatic [SSLContext](../javax/net/ssl/SSLContext.md)! | [getInstance](../javax/net/ssl/SSLContext.md))`(`protocol:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a`SSLContext`object that implements the specified secure socket protocol. |
| openstatic [SSLContext](../javax/net/ssl/SSLContext.md)! | [getInstance](../javax/net/ssl/SSLContext.md))`(`protocol:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `provider:` ` [Provider](../java/security/Provider.md)!`)` Returns a`SSLContext`object that implements the specified secure socket protocol. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getProtocol](../javax/net/ssl/SSLContext.md))`()` Returns the protocol name of this`SSLContext`object. |
| --- | --- |
| [Provider](../java/security/Provider.md)! | [getProvider](../javax/net/ssl/SSLContext.md))`()` Returns the provider of this`SSLContext`object. |
| [SSLSessionContext](../javax/net/ssl/SSLSessionContext.md)! | [getServerSessionContext](../javax/net/ssl/SSLContext.md))`()` Returns the server session context, which represents the set of SSL sessions available for use during the handshake phase of server-side SSL sockets. |
| [SSLServerSocketFactory](../javax/net/ssl/SSLServerSocketFactory.md)! | [getServerSocketFactory](../javax/net/ssl/SSLContext.md))`()` Returns a`ServerSocketFactory`object for this context. |
| --- | --- |
| [SSLSocketFactory](../javax/net/ssl/SSLSocketFactory.md)! | [getSocketFactory](../javax/net/ssl/SSLContext.md))`()` Returns a`SocketFactory`object for this context. |
| [SSLParameters](../javax/net/ssl/SSLParameters.md)! | [getSupportedSSLParameters](../javax/net/ssl/SSLContext.md))`()` Returns a copy of the SSLParameters indicating the supported settings for this SSL context. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](../javax/net/ssl/SSLContext.md))`(`km:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [KeyManager](../javax/net/ssl/KeyManager.md)!>!`, `tm:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [TrustManager](../javax/net/ssl/TrustManager.md)!>!`, `random:` ` [SecureRandom](../java/security/SecureRandom.md)!`)` Initializes this context. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDefault](../javax/net/ssl/SSLContext.md))`(`context:` ` [SSLContext](../javax/net/ssl/SSLContext.md)!`)` Sets the default SSL context. |

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
| `contextSpi` | [SSLContextSpi](../javax/net/ssl/SSLContextSpi.md)!:the delegate |
| `provider` | [Provider](../java/security/Provider.md)!:the provider |
| `protocol` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the protocol |
| --- | --- |

## Public methods

### createSSLEngine

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun createSSLEngine(): SSLEngine!
```

Creates a new`SSLEngine`using this context.

Applications using this factory method are providing no hints for an internal session reuse strategy. If hints are desired, [createSSLEngine(java.lang.String,int)](../javax/net/ssl/SSLContext.md))should be used instead.

Some cipher suites (such as Kerberos) require remote hostname information, in which case this factory method should not be used.

| Return ||
|--------------------------------------------------------------------------------------|----------------------|
| [SSLEngine](../javax/net/ssl/SSLEngine.md)! | the`SSLEngine`object |

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
| [SSLEngine](../javax/net/ssl/SSLEngine.md)! | the new`SSLEngine`object |

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
| [SSLSessionContext](../javax/net/ssl/SSLSessionContext.md)! | client session context bound to this SSL context |

### getDefault

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getDefault(): SSLContext!
```

Returns the default SSL context.

If a default context was set using the [SSLContext.setDefault()](../javax/net/ssl/SSLContext.md))method, it is returned. Otherwise, the first call of this method triggers the call`SSLContext.getInstance("Default")`. If successful, that object is made the default SSL context and returned.

The default context is immediately usable and does not require [initialization](../javax/net/ssl/SSLContext.md)).

| Return ||
|-----------------------------------------------------------------------------------------|-------------------------|
| [SSLContext](../javax/net/ssl/SSLContext.md)! | the default SSL context |

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
| [SSLParameters](../javax/net/ssl/SSLParameters.md)! | a copy of the SSLParameters object with the default settings |

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

Note that the list of registered providers may be retrieved via the [Security.getProviders()](../java/security/Security.md))method.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `protocol` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the standard name of the requested protocol. See the SSLContext section in the [Java Cryptography Architecture Standard Algorithm Name Documentation](https://docs.oracle.com/javase/8/docs/technotes/guides/security/StandardNames.html#SSLContext) for information about standard protocol names. |

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------|
| [SSLContext](../javax/net/ssl/SSLContext.md)! | the new`SSLContext`object. |

| Exceptions ||
|------------------------------------------|------------------------------------------------------------------------------------|
| `java.security.NoSuchAlgorithmException` | if no Provider supports a SSLContextSpi implementation for the specified protocol. |
| `java.lang.NullPointerException` | if protocol is null. |

**See Also**

- [java.security.Provider](../java/security/Provider.md) 

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

Note that the list of registered providers may be retrieved via the [Security.getProviders()](../java/security/Security.md))method.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `protocol` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the standard name of the requested protocol. See the SSLContext section in the [Java Cryptography Architecture Standard Algorithm Name Documentation](https://docs.oracle.com/javase/8/docs/technotes/guides/security/StandardNames.html#SSLContext) for information about standard protocol names. |
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the provider. |

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------|
| [SSLContext](../javax/net/ssl/SSLContext.md)! | the new`SSLContext`object. |

| Exceptions ||
|------------------------------------------|------------------------------------------------------------------------------------------------------------|
| `java.security.NoSuchAlgorithmException` | if a SSLContextSpi implementation for the specified protocol is not available from the specified provider. |
| `java.security.NoSuchProviderException` | if the specified provider is not registered in the security provider list. |
| `java.lang.IllegalArgumentException` | if the provider name is null or empty. |
| --- | --- |
| `java.lang.NullPointerException` | if protocol is null. |

**See Also**

- [java.security.Provider](../java/security/Provider.md) 

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
| `provider` | [Provider](../java/security/Provider.md)!:an instance of the provider. |

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------|
| [SSLContext](../javax/net/ssl/SSLContext.md)! | the new`SSLContext`object. |

| Exceptions ||
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| `java.security.NoSuchAlgorithmException` | if a SSLContextSpi implementation for the specified protocol is not available from the specified Provider object. |
| `java.lang.IllegalArgumentException` | if the provider is null. |
| `java.lang.NullPointerException` | if protocol is null. |
| --- | --- |

**See Also**

- [java.security.Provider](../java/security/Provider.md) 

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
| [Provider](../java/security/Provider.md)! | the provider of this`SSLContext`object |

### getServerSessionContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getServerSessionContext(): SSLSessionContext!
```

Returns the server session context, which represents the set of SSL sessions available for use during the handshake phase of server-side SSL sockets.

This context may be unavailable in some environments, in which case this method returns null. For example, when the underlying SSL provider does not provide an implementation of SSLSessionContext interface, this method returns null. A non-null session context is returned otherwise.

| Return ||
|------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [SSLSessionContext](../javax/net/ssl/SSLSessionContext.md)! | server session context bound to this SSL context |

### getServerSocketFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getServerSocketFactory(): SSLServerSocketFactory!
```

Returns a`ServerSocketFactory`object for this context.

| Return ||
|----------------------------------------------------------------------------------------------------------------|--------------------------------|
| [SSLServerSocketFactory](../javax/net/ssl/SSLServerSocketFactory.md)! | the`ServerSocketFactory`object |

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
| [SSLSocketFactory](../javax/net/ssl/SSLSocketFactory.md)! | the`SocketFactory`object |

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
| [SSLParameters](../javax/net/ssl/SSLParameters.md)! | a copy of the SSLParameters object with the supported settings |

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
| `km` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [KeyManager](../javax/net/ssl/KeyManager.md)!\>!:the sources of authentication keys or null |
| `tm` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [TrustManager](../javax/net/ssl/TrustManager.md)!\>!:the sources of peer authentication trust decisions or null |
| `random` | [SecureRandom](../java/security/SecureRandom.md)!:the source of randomness for this generator or null |
| --- | --- |

| Exceptions ||
|----------------------------------------|-------------------------|
| `java.security.KeyManagementException` | if this operation fails |

### setDefault

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun setDefault(context: SSLContext!): Unit
```

Sets the default SSL context. It will be returned by subsequent calls to [getDefault](../javax/net/ssl/SSLContext.md)). The default context must be immediately usable and not require [initialization](../javax/net/ssl/SSLContext.md)).

Developers are*strongly* discouraged from changing the default`SSLContext`as it is used as the Android default for secure communication by APIs like [SSLSocketFactory.getDefault()](../javax/net/ssl/SSLSocketFactory.md)), [SSLServerSocketFactory.getDefault()](../javax/net/ssl/SSLServerSocketFactory.md))and [HttpsURLConnection](../javax/net/ssl/HttpsURLConnection.md).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------|
| `context` | [SSLContext](../javax/net/ssl/SSLContext.md)!:the SSLContext |

| Exceptions ||
|----------------------------------|-------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if context is null |
| `java.lang.SecurityException` | if a security manager exists and its`checkPermission`method does not allow`SSLPermission("setDefaultSSLContext")` |
