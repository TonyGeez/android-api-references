# TrustManagerFactorySpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TrustManagerFactorySpi

```
abstract class TrustManagerFactorySpi
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.net.ssl.TrustManagerFactorySpi](../javax/net/ssl/TrustManagerFactorySpi.md) |

This class defines the*Service Provider Interface* (**SPI** ) for the`TrustManagerFactory`class.

All the abstract methods in this class must be implemented by each cryptographic service provider who wishes to supply the implementation of a particular trust manager factory.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TrustManagerFactorySpi](../javax/net/ssl/TrustManagerFactorySpi.md))`()` <br /> |

| Protected methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [TrustManager](../javax/net/ssl/TrustManager.md)!\>! | [engineGetTrustManagers](../javax/net/ssl/TrustManagerFactorySpi.md))`()` Returns one trust manager for each type of trust material. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInit](../javax/net/ssl/TrustManagerFactorySpi.md))`(`ks:` ` [KeyStore](../java/security/KeyStore.md)!`)` Initializes this factory with a source of certificate authorities and related trust material. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInit](../javax/net/ssl/TrustManagerFactorySpi.md))`(`spec:` ` [ManagerFactoryParameters](../javax/net/ssl/ManagerFactoryParameters.md)!`)` Initializes this factory with a source of provider-specific key material. |
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
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [TrustManager](../javax/net/ssl/TrustManager.md)!>! | the trust managers |

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
| `ks` | [KeyStore](../java/security/KeyStore.md)!:the key store or null |

| Exceptions ||
|-----------------------------------|-------------------------|
| `java.security.KeyStoreException` | if this operation fails |

**See Also**

- [javax.net.ssl.TrustManagerFactory#init(KeyStore)](../javax/net/ssl/TrustManagerFactory.md)) 

### engineInit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineInit(spec: ManagerFactoryParameters!): Unit
```

Initializes this factory with a source of provider-specific key material.

In some cases, initialization parameters other than a keystore may be needed by a provider. Users of that particular provider are expected to pass an implementation of the appropriate`ManagerFactoryParameters`as defined by the provider. The provider can then call the specified methods in the`ManagerFactoryParameters`implementation to obtain the needed information.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `spec` | [ManagerFactoryParameters](../javax/net/ssl/ManagerFactoryParameters.md)!:an implementation of a provider-specific parameter specification |

| Exceptions ||
|----------------------------------------------------|-----------------------------------------|
| `java.security.InvalidAlgorithmParameterException` | if there is problem with the parameters |

**See Also**

- [javax.net.ssl.TrustManagerFactory#init(ManagerFactoryParameters spec)](../javax/net/ssl/TrustManagerFactory.md))
