# KeyManagerFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyManagerFactory

```
open class KeyManagerFactory
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [javax.net.ssl.KeyManagerFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyManagerFactory#) |

This class acts as a factory for key managers based on a source of key material. Each key manager manages a specific type of key material for use by secure sockets. The key material is based on a KeyStore and/or provider specific sources.

Android provides the following`KeyManagerFactory`algorithms:

| Algorithm | Supported API Levels |
|-----------|----------------------|
| PKIX | 1+ |

## Summary

| Protected constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [KeyManagerFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyManagerFactory#KeyManagerFactory(javax.net.ssl.KeyManagerFactorySpi,%20java.security.Provider,%20kotlin.String))`(`factorySpi:` ` [KeyManagerFactorySpi](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyManagerFactorySpi)!`, `provider:` ` [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)!`, `algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a KeyManagerFactory object. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAlgorithm](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyManagerFactory#getAlgorithm())`()` Returns the algorithm name of this`KeyManagerFactory`object. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDefaultAlgorithm](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyManagerFactory#getDefaultAlgorithm())`()` Obtains the default KeyManagerFactory algorithm name. |
| static [KeyManagerFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyManagerFactory#)! | [getInstance](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyManagerFactory#getInstance(kotlin.String))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a`KeyManagerFactory`object that acts as a factory for key managers. |
| static [KeyManagerFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyManagerFactory#)! | [getInstance](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyManagerFactory#getInstance(kotlin.String,%20kotlin.String))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a`KeyManagerFactory`object that acts as a factory for key managers. |
| static [KeyManagerFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyManagerFactory#)! | [getInstance](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyManagerFactory#getInstance(kotlin.String,%20java.security.Provider))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `provider:` ` [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)!`)` Returns a`KeyManagerFactory`object that acts as a factory for key managers. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [KeyManager](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyManager)!\>! | [getKeyManagers](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyManagerFactory#getKeyManagers())`()` Returns one key manager for each type of key material. |
| [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)! | [getProvider](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyManagerFactory#getProvider())`()` Returns the provider of this`KeyManagerFactory`object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyManagerFactory#init(java.security.KeyStore,%20kotlin.CharArray))`(`ks:` ` [KeyStore](https://developer.android.com/reference/kotlin/java/security/KeyStore.html#)!`, `password:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`)` Initializes this factory with a source of key material. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyManagerFactory#init(javax.net.ssl.ManagerFactoryParameters))`(`spec:` ` [ManagerFactoryParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/ManagerFactoryParameters)!`)` Initializes this factory with a source of provider-specific key material. |

## Protected constructors

### KeyManagerFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected KeyManagerFactory(
    factorySpi: KeyManagerFactorySpi!, 
    provider: Provider!, 
    algorithm: String!)
```

Creates a KeyManagerFactory object.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------|
| `factorySpi` | [KeyManagerFactorySpi](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyManagerFactorySpi)!:the delegate |
| `provider` | [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)!:the provider |
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the algorithm |

## Public methods

### getAlgorithm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAlgorithm(): String!
```

Returns the algorithm name of this`KeyManagerFactory`object.

This is the same name that was specified in one of the`getInstance`calls that created this`KeyManagerFactory`object.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the algorithm name of this`KeyManagerFactory`object. |

### getDefaultAlgorithm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDefaultAlgorithm(): String!
```

Obtains the default KeyManagerFactory algorithm name.

The default algorithm can be changed at runtime by setting the value of the`ssl.KeyManagerFactory.algorithm`security property to the desired algorithm name.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the default algorithm name as specified by the`ssl.KeyManagerFactory.algorithm`security property, or an implementation-specific default if no such property exists. |

**See Also**

- [java.security.Security](https://developer.android.com/reference/kotlin/java/security/Security.html#) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(algorithm: String!): KeyManagerFactory!
```

Returns a`KeyManagerFactory`object that acts as a factory for key managers.

This method traverses the list of registered security Providers, starting with the most preferred Provider. A new KeyManagerFactory object encapsulating the KeyManagerFactorySpi implementation from the first Provider that supports the specified algorithm is returned.

Note that the list of registered providers may be retrieved via the [Security.getProviders()](https://developer.android.com/reference/kotlin/java/security/Security.html#getProviders())method.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the standard name of the requested algorithm. See the [Java Secure Socket Extension Reference Guide](https://docs.oracle.com/javase/8/docs/technotes/guides/security/jsse/JSSERefGuide.html) for information about standard algorithm names. |

| Return ||
|-------------------------------------------------------------------------------------------------------|-----------------------------------|
| [KeyManagerFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyManagerFactory#)! | the new`KeyManagerFactory`object. |

| Exceptions ||
|------------------------------------------|--------------------------------------------------------------------------------------------|
| `java.security.NoSuchAlgorithmException` | if no Provider supports a KeyManagerFactorySpi implementation for the specified algorithm. |
| `java.lang.NullPointerException` | if`algorithm`is null. |

**See Also**

- [java.security.Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(
    algorithm: String!, 
    provider: String!
): KeyManagerFactory!
```

Returns a`KeyManagerFactory`object that acts as a factory for key managers.

A new KeyManagerFactory object encapsulating the KeyManagerFactorySpi implementation from the specified provider is returned. The specified provider must be registered in the security provider list.

Note that the list of registered providers may be retrieved via the [Security.getProviders()](https://developer.android.com/reference/kotlin/java/security/Security.html#getProviders())method.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the standard name of the requested algorithm. See the [Java Secure Socket Extension Reference Guide](https://docs.oracle.com/javase/8/docs/technotes/guides/security/jsse/JSSERefGuide.html) for information about standard algorithm names. |
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the provider. |

| Return ||
|-------------------------------------------------------------------------------------------------------|-----------------------------------|
| [KeyManagerFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyManagerFactory#)! | the new`KeyManagerFactory`object. |

| Exceptions ||
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| `java.security.NoSuchAlgorithmException` | if a KeyManagerFactorySpi implementation for the specified algorithm is not available from the specified provider. |
| `java.security.NoSuchProviderException` | if the specified provider is not registered in the security provider list. |
| `java.lang.IllegalArgumentException` | if the provider name is null or empty. |
| `java.lang.NullPointerException` | if`algorithm`is null. |

**See Also**

- [java.security.Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(
    algorithm: String!, 
    provider: Provider!
): KeyManagerFactory!
```

Returns a`KeyManagerFactory`object that acts as a factory for key managers.

A new KeyManagerFactory object encapsulating the KeyManagerFactorySpi implementation from the specified Provider object is returned. Note that the specified Provider object does not have to be registered in the provider list.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the standard name of the requested algorithm. See the [Java Secure Socket Extension Reference Guide](https://docs.oracle.com/javase/8/docs/technotes/guides/security/jsse/JSSERefGuide.html) for information about standard algorithm names. |
| `provider` | [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)!:an instance of the provider. |

| Return ||
|-------------------------------------------------------------------------------------------------------|-----------------------------------|
| [KeyManagerFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyManagerFactory#)! | the new`KeyManagerFactory`object. |

| Exceptions ||
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| `java.security.NoSuchAlgorithmException` | if a KeyManagerFactorySpi implementation for the specified algorithm is not available from the specified Provider object. |
| `java.lang.IllegalArgumentException` | if provider is null. |
| `java.lang.NullPointerException` | if`algorithm`is null. |

**See Also**

- [java.security.Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#) 

### getKeyManagers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getKeyManagers(): Array<KeyManager!>!
```

Returns one key manager for each type of key material.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [KeyManager](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyManager)!>! | the key managers |

| Exceptions ||
|-----------------------------------|---------------------------------------------|
| `java.lang.IllegalStateException` | if the KeyManagerFactory is not initialized |

### getProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getProvider(): Provider!
```

Returns the provider of this`KeyManagerFactory`object.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------------------|
| [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)! | the provider of this`KeyManagerFactory`object |

### init

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun init(
    ks: KeyStore!, 
    password: CharArray!
): Unit
```

Initializes this factory with a source of key material.

The provider typically uses a KeyStore for obtaining key material for use during secure socket negotiations. The KeyStore is generally password-protected.

For more flexible initialization, please see [init(javax.net.ssl.ManagerFactoryParameters)](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyManagerFactory#init(javax.net.ssl.ManagerFactoryParameters)).

<br />

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `ks` | [KeyStore](https://developer.android.com/reference/kotlin/java/security/KeyStore.html#)!:the key store or null |
| `password` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:the password for recovering keys in the KeyStore |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------|
| `java.security.KeyStoreException` | if this operation fails |
| `java.security.NoSuchAlgorithmException` | if the specified algorithm is not available from the specified provider. |
| `java.security.UnrecoverableKeyException` | if the key cannot be recovered (e.g. the given password is wrong). |

### init

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun init(spec: ManagerFactoryParameters!): Unit
```

Initializes this factory with a source of provider-specific key material.

In some cases, initialization parameters other than a keystore and password may be needed by a provider. Users of that particular provider are expected to pass an implementation of the appropriate`ManagerFactoryParameters`as defined by the provider. The provider can then call the specified methods in the`ManagerFactoryParameters`implementation to obtain the needed information.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `spec` | [ManagerFactoryParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/ManagerFactoryParameters)!:an implementation of a provider-specific parameter specification |

| Exceptions ||
|----------------------------------------------------|----------------------------|
| `java.security.InvalidAlgorithmParameterException` | if an error is encountered |
