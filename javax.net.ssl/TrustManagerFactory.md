# TrustManagerFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TrustManagerFactory

```
open class TrustManagerFactory
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.net.ssl.TrustManagerFactory](TrustManagerFactory.md) |

This class acts as a factory for trust managers based on a source of trust material. Each trust manager manages a specific type of trust material for use by secure sockets. The trust material is based on a KeyStore and/or provider specific sources.

Android provides the following`TrustManagerFactory`algorithms:

| Algorithm | Supported API Levels |
|-----------|----------------------|
| PKIX | 1+ |

## Summary

| Protected constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TrustManagerFactory](TrustManagerFactory.md))`(`factorySpi:` ` [TrustManagerFactorySpi](TrustManagerFactorySpi.md)!`, `provider:` ` [Provider](../java.security/Provider.md)!`, `algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a TrustManagerFactory object. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAlgorithm](TrustManagerFactory.md))`()` Returns the algorithm name of this`TrustManagerFactory`object. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDefaultAlgorithm](TrustManagerFactory.md))`()` Obtains the default TrustManagerFactory algorithm name. |
| static [TrustManagerFactory](TrustManagerFactory.md)! | [getInstance](TrustManagerFactory.md))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a`TrustManagerFactory`object that acts as a factory for trust managers. |
| --- | --- |
| static [TrustManagerFactory](TrustManagerFactory.md)! | [getInstance](TrustManagerFactory.md))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a`TrustManagerFactory`object that acts as a factory for trust managers. |
| static [TrustManagerFactory](TrustManagerFactory.md)! | [getInstance](TrustManagerFactory.md))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `provider:` ` [Provider](../java.security/Provider.md)!`)` Returns a`TrustManagerFactory`object that acts as a factory for trust managers. |
| [Provider](../java.security/Provider.md)! | [getProvider](TrustManagerFactory.md))`()` Returns the provider of this`TrustManagerFactory`object. |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [TrustManager](TrustManager.md)!\>! | [getTrustManagers](TrustManagerFactory.md))`()` Returns one trust manager for each type of trust material. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](TrustManagerFactory.md))`(`ks:` ` [KeyStore](../java.security/KeyStore.md)!`)` Initializes this factory with a source of certificate authorities and related trust material. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](TrustManagerFactory.md))`(`spec:` ` [ManagerFactoryParameters](ManagerFactoryParameters.md)!`)` Initializes this factory with a source of provider-specific trust material. |
| --- | --- |

## Protected constructors

### TrustManagerFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected TrustManagerFactory(
    factorySpi: TrustManagerFactorySpi!, 
    provider: Provider!, 
    algorithm: String!)
```

Creates a TrustManagerFactory object.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------|
| `factorySpi` | [TrustManagerFactorySpi](TrustManagerFactorySpi.md)!:the delegate |
| `provider` | [Provider](../java.security/Provider.md)!:the provider |
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the algorithm |
| --- | --- |

## Public methods

### getAlgorithm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAlgorithm(): String!
```

Returns the algorithm name of this`TrustManagerFactory`object.

This is the same name that was specified in one of the`getInstance`calls that created this`TrustManagerFactory`object.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the algorithm name of this`TrustManagerFactory`object |

### getDefaultAlgorithm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDefaultAlgorithm(): String!
```

Obtains the default TrustManagerFactory algorithm name.

The default TrustManager can be changed at runtime by setting the value of the`ssl.TrustManagerFactory.algorithm`security property to the desired algorithm name.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the default algorithm name as specified by the`ssl.TrustManagerFactory.algorithm`security property, or an implementation-specific default if no such property exists. |

**See Also**

- [java.security.Security](../java.security/Security.md) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(algorithm: String!): TrustManagerFactory!
```

Returns a`TrustManagerFactory`object that acts as a factory for trust managers.

This method traverses the list of registered security Providers, starting with the most preferred Provider. A new TrustManagerFactory object encapsulating the TrustManagerFactorySpi implementation from the first Provider that supports the specified algorithm is returned.

Note that the list of registered providers may be retrieved via the [Security.getProviders()](../java.security/Security.md))method.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the standard name of the requested trust management algorithm. See the [Java Secure Socket Extension Reference Guide](https://docs.oracle.com/javase/8/docs/technotes/guides/security/jsse/JSSERefGuide.html) for information about standard algorithm names. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------|
| [TrustManagerFactory](TrustManagerFactory.md)! | the new`TrustManagerFactory`object. |

| Exceptions ||
|------------------------------------------|----------------------------------------------------------------------------------------------|
| `java.security.NoSuchAlgorithmException` | if no Provider supports a TrustManagerFactorySpi implementation for the specified algorithm. |
| `java.lang.NullPointerException` | if algorithm is null. |

**See Also**

- [java.security.Provider](../java.security/Provider.md) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(
    algorithm: String!, 
    provider: String!
): TrustManagerFactory!
```

Returns a`TrustManagerFactory`object that acts as a factory for trust managers.

A new KeyManagerFactory object encapsulating the KeyManagerFactorySpi implementation from the specified provider is returned. The specified provider must be registered in the security provider list.

Note that the list of registered providers may be retrieved via the [Security.getProviders()](../java.security/Security.md))method.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the standard name of the requested trust management algorithm. See the [Java Secure Socket Extension Reference Guide](https://docs.oracle.com/javase/8/docs/technotes/guides/security/jsse/JSSERefGuide.html) for information about standard algorithm names. |
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the provider. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|------------------------------------|
| [TrustManagerFactory](TrustManagerFactory.md)! | the new`TrustManagerFactory`object |

| Exceptions ||
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| `java.security.NoSuchAlgorithmException` | if a TrustManagerFactorySpi implementation for the specified algorithm is not available from the specified provider. |
| `java.security.NoSuchProviderException` | if the specified provider is not registered in the security provider list. |
| `java.lang.IllegalArgumentException` | if the provider name is null or empty. |
| --- | --- |
| `java.lang.NullPointerException` | if algorithm is null. |

**See Also**

- [java.security.Provider](../java.security/Provider.md) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(
    algorithm: String!, 
    provider: Provider!
): TrustManagerFactory!
```

Returns a`TrustManagerFactory`object that acts as a factory for trust managers.

A new TrustManagerFactory object encapsulating the TrustManagerFactorySpi implementation from the specified Provider object is returned. Note that the specified Provider object does not have to be registered in the provider list.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the standard name of the requested trust management algorithm. See the [Java Secure Socket Extension Reference Guide](https://docs.oracle.com/javase/8/docs/technotes/guides/security/jsse/JSSERefGuide.html) for information about standard algorithm names. |
| `provider` | [Provider](../java.security/Provider.md)!:an instance of the provider. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------|
| [TrustManagerFactory](TrustManagerFactory.md)! | the new`TrustManagerFactory`object. |

| Exceptions ||
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| `java.security.NoSuchAlgorithmException` | if a TrustManagerFactorySpi implementation for the specified algorithm is not available from the specified Provider object. |
| `java.lang.IllegalArgumentException` | if the provider is null. |
| `java.lang.NullPointerException` | if algorithm is null. |
| --- | --- |

**See Also**

- [java.security.Provider](../java.security/Provider.md) 

### getProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getProvider(): Provider!
```

Returns the provider of this`TrustManagerFactory`object.

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------|
| [Provider](../java.security/Provider.md)! | the provider of this`TrustManagerFactory`object |

### getTrustManagers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTrustManagers(): Array<TrustManager!>!
```

Returns one trust manager for each type of trust material.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [TrustManager](TrustManager.md)!>! | the trust managers |

| Exceptions ||
|-----------------------------------|------------------------------------|
| `java.lang.IllegalStateException` | if the factory is not initialized. |

### init

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun init(ks: KeyStore!): Unit
```

Initializes this factory with a source of certificate authorities and related trust material.

The provider typically uses a KeyStore as a basis for making trust decisions.

For more flexible initialization, please see [init(javax.net.ssl.ManagerFactoryParameters)](TrustManagerFactory.md)).

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------|
| `ks` | [KeyStore](../java.security/KeyStore.md)!:the key store, or null |

| Exceptions ||
|-----------------------------------|-------------------------|
| `java.security.KeyStoreException` | if this operation fails |

### init

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun init(spec: ManagerFactoryParameters!): Unit
```

Initializes this factory with a source of provider-specific trust material.

In some cases, initialization parameters other than a keystore may be needed by a provider. Users of that particular provider are expected to pass an implementation of the appropriate`ManagerFactoryParameters`as defined by the provider. The provider can then call the specified methods in the`ManagerFactoryParameters`implementation to obtain the needed information.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `spec` | [ManagerFactoryParameters](ManagerFactoryParameters.md)!:an implementation of a provider-specific parameter specification |

| Exceptions ||
|----------------------------------------------------|----------------------------|
| `java.security.InvalidAlgorithmParameterException` | if an error is encountered |
