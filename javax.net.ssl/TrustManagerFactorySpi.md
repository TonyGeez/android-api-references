# TrustManagerFactorySpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TrustManagerFactorySpi

```
abstract class TrustManagerFactorySpi
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.net.ssl.TrustManagerFactorySpi](https://developer.android.com/reference/kotlin/javax/net/ssl/TrustManagerFactorySpi#) |

This class defines the*Service Provider Interface* (**SPI** ) for the`TrustManagerFactory`class.

All the abstract methods in this class must be implemented by each cryptographic service provider who wishes to supply the implementation of a particular trust manager factory.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TrustManagerFactorySpi](https://developer.android.com/reference/kotlin/javax/net/ssl/TrustManagerFactorySpi#TrustManagerFactorySpi())`()` <br /> |

| Protected methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [TrustManager](https://developer.android.com/reference/kotlin/javax/net/ssl/TrustManager)!\>! | [engineGetTrustManagers](https://developer.android.com/reference/kotlin/javax/net/ssl/TrustManagerFactorySpi#engineGetTrustManagers())`()` Returns one trust manager for each type of trust material. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInit](https://developer.android.com/reference/kotlin/javax/net/ssl/TrustManagerFactorySpi#engineInit(java.security.KeyStore))`(`ks:` ` [KeyStore](https://developer.android.com/reference/kotlin/java/security/KeyStore.html#)!`)` Initializes this factory with a source of certificate authorities and related trust material. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInit](https://developer.android.com/reference/kotlin/javax/net/ssl/TrustManagerFactorySpi#engineInit(javax.net.ssl.ManagerFactoryParameters))`(`spec:` ` [ManagerFactoryParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/ManagerFactoryParameters)!`)` Initializes this factory with a source of provider-specific key material. |
| --- | --- |

## Public constructors

### TrustManagerFactorySpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TrustManagerFactorySpi()
```

## Protected methods

### engineGetTrustManagers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineGetTrustManagers(): Array<TrustManager!>!
```

Returns one trust manager for each type of trust material.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [TrustManager](https://developer.android.com/reference/kotlin/javax/net/ssl/TrustManager)!>! | the trust managers |

| Exceptions ||
|-----------------------------------|------------------------------------|
| `java.lang.IllegalStateException` | if the factory is not initialized. |

### engineInit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineInit(ks: KeyStore!): Unit
```

Initializes this factory with a source of certificate authorities and related trust material.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------|
| `ks` | [KeyStore](https://developer.android.com/reference/kotlin/java/security/KeyStore.html#)!:the key store or null |

| Exceptions ||
|-----------------------------------|-------------------------|
| `java.security.KeyStoreException` | if this operation fails |

**See Also**

- [javax.net.ssl.TrustManagerFactory#init(KeyStore)](https://developer.android.com/reference/kotlin/javax/net/ssl/TrustManagerFactory#init(java.security.KeyStore)) 

### engineInit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineInit(spec: ManagerFactoryParameters!): Unit
```

Initializes this factory with a source of provider-specific key material.

In some cases, initialization parameters other than a keystore may be needed by a provider. Users of that particular provider are expected to pass an implementation of the appropriate`ManagerFactoryParameters`as defined by the provider. The provider can then call the specified methods in the`ManagerFactoryParameters`implementation to obtain the needed information.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `spec` | [ManagerFactoryParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/ManagerFactoryParameters)!:an implementation of a provider-specific parameter specification |

| Exceptions ||
|----------------------------------------------------|-----------------------------------------|
| `java.security.InvalidAlgorithmParameterException` | if there is problem with the parameters |

**See Also**

- [javax.net.ssl.TrustManagerFactory#init(ManagerFactoryParameters spec)](https://developer.android.com/reference/kotlin/javax/net/ssl/TrustManagerFactory#init(javax.net.ssl.ManagerFactoryParameters))
