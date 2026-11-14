# KeyManagerFactorySpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyManagerFactorySpi

```
abstract class KeyManagerFactorySpi
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.net.ssl.KeyManagerFactorySpi](../javax/net/ssl/KeyManagerFactorySpi.md) |

This class defines the*Service Provider Interface* (**SPI** ) for the`KeyManagerFactory`class.

All the abstract methods in this class must be implemented by each cryptographic service provider who wishes to supply the implementation of a particular key manager factory.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------|---|
| [KeyManagerFactorySpi](../javax/net/ssl/KeyManagerFactorySpi.md))`()` <br /> |

| Protected methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [KeyManager](../javax/net/ssl/KeyManager.md)!\>! | [engineGetKeyManagers](../javax/net/ssl/KeyManagerFactorySpi.md))`()` Returns one key manager for each type of key material. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInit](../javax/net/ssl/KeyManagerFactorySpi.md))`(`ks:` ` [KeyStore](../java/security/KeyStore.md)!`, `password:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`)` Initializes this factory with a source of key material. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInit](../javax/net/ssl/KeyManagerFactorySpi.md))`(`spec:` ` [ManagerFactoryParameters](../javax/net/ssl/ManagerFactoryParameters.md)!`)` Initializes this factory with a source of key material. |
| --- | --- |

## Public constructors

### KeyManagerFactorySpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyManagerFactorySpi()
```

## Protected methods

### engineGetKeyManagers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineGetKeyManagers(): Array<KeyManager!>!
```

Returns one key manager for each type of key material.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [KeyManager](../javax/net/ssl/KeyManager.md)!>! | the key managers |

| Exceptions ||
|-----------------------------------|------------------------------------------------|
| `java.lang.IllegalStateException` | if the KeyManagerFactorySpi is not initialized |

### engineInit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineInit(
    ks: KeyStore!, 
    password: CharArray!
): Unit
```

Initializes this factory with a source of key material.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------|
| `ks` | [KeyStore](../java/security/KeyStore.md)!:the key store or null |
| `password` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:the password for recovering keys |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------|
| `java.security.KeyStoreException` | if this operation fails |
| `java.security.NoSuchAlgorithmException` | if the specified algorithm is not available from the specified provider. |
| `java.security.UnrecoverableKeyException` | if the key cannot be recovered |
| --- | --- |

**See Also**

- [javax.net.ssl.KeyManagerFactory#init(KeyStore, char[])](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyManagerFactory#init(java.security.KeyStore,%20kotlin.CharArray)) 

### engineInit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineInit(spec: ManagerFactoryParameters!): Unit
```

Initializes this factory with a source of key material.

In some cases, initialization parameters other than a keystore and password may be needed by a provider. Users of that particular provider are expected to pass an implementation of the appropriate`ManagerFactoryParameters`as defined by the provider. The provider can then call the specified methods in the ManagerFactoryParameters implementation to obtain the needed information.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `spec` | [ManagerFactoryParameters](../javax/net/ssl/ManagerFactoryParameters.md)!:an implementation of a provider-specific parameter specification |

| Exceptions ||
|----------------------------------------------------|-----------------------------------------|
| `java.security.InvalidAlgorithmParameterException` | if there is problem with the parameters |

**See Also**

- [javax.net.ssl.KeyManagerFactory#init(ManagerFactoryParameters spec)](../javax/net/ssl/KeyManagerFactory.md))
