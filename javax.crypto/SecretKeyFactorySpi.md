# SecretKeyFactorySpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SecretKeyFactorySpi

```
abstract class SecretKeyFactorySpi
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.crypto.SecretKeyFactorySpi](https://developer.android.com/reference/kotlin/javax/crypto/SecretKeyFactorySpi#) |

This class defines the *Service Provider Interface* (**SPI** ) for the `SecretKeyFactory` class. All the abstract methods in this class must be implemented by each cryptographic service provider who wishes to supply the implementation of a secret-key factory for a particular algorithm.

A provider should document all the key specifications supported by its secret key factory. For example, the DES secret-key factory supplied by the "SunJCE" provider supports `DESKeySpec` as a transparent representation of DES keys, and that provider's secret-key factory for Triple DES keys supports `DESedeKeySpec` as a transparent representation of Triple DES keys.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------|---|
| [SecretKeyFactorySpi](https://developer.android.com/reference/kotlin/javax/crypto/SecretKeyFactorySpi#SecretKeyFactorySpi())`()` <br /> |

| Protected methods ||
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [SecretKey](https://developer.android.com/reference/kotlin/javax/crypto/SecretKey)! | [engineGenerateSecret](https://developer.android.com/reference/kotlin/javax/crypto/SecretKeyFactorySpi#engineGenerateSecret(java.security.spec.KeySpec))`(`keySpec:` ` [KeySpec](https://developer.android.com/reference/kotlin/java/security/spec/KeySpec.html#)!`)` Generates a `SecretKey` object from the provided key specification (key material). |
| abstract [KeySpec](https://developer.android.com/reference/kotlin/java/security/spec/KeySpec.html#)! | [engineGetKeySpec](https://developer.android.com/reference/kotlin/javax/crypto/SecretKeyFactorySpi#engineGetKeySpec(javax.crypto.SecretKey,%20java.lang.Class))`(`key:` ` [SecretKey](https://developer.android.com/reference/kotlin/javax/crypto/SecretKey)!`, `keySpec:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<*>!`)` Returns a specification (key material) of the given key object in the requested format. |
| abstract [SecretKey](https://developer.android.com/reference/kotlin/javax/crypto/SecretKey)! | [engineTranslateKey](https://developer.android.com/reference/kotlin/javax/crypto/SecretKeyFactorySpi#engineTranslateKey(javax.crypto.SecretKey))`(`key:` ` [SecretKey](https://developer.android.com/reference/kotlin/javax/crypto/SecretKey)!`)` Translates a key object, whose provider may be unknown or potentially untrusted, into a corresponding key object of this secret-key factory. |
| --- | --- |

## Public constructors

### SecretKeyFactorySpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SecretKeyFactorySpi()
```

## Protected methods

### engineGenerateSecret

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineGenerateSecret(keySpec: KeySpec!): SecretKey!
```

Generates a `SecretKey` object from the provided key specification (key material).

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `keySpec` | [KeySpec](https://developer.android.com/reference/kotlin/java/security/spec/KeySpec.html#)!: the specification (key material) of the secret key |

| Return ||
|-------------------------------------------------------------------------------------|----------------|
| [SecretKey](https://developer.android.com/reference/kotlin/javax/crypto/SecretKey)! | the secret key |

| Exceptions ||
|----------------------------------------------|------------------------------------------------------------------------------------------------------|
| `java.security.spec.InvalidKeySpecException` | if the given key specification is inappropriate for this secret-key factory to produce a secret key. |

### engineGetKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineGetKeySpec(
    key: SecretKey!, 
    keySpec: Class<*>!
): KeySpec!
```

Returns a specification (key material) of the given key object in the requested format.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [SecretKey](https://developer.android.com/reference/kotlin/javax/crypto/SecretKey)!: the key |
| `keySpec` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<\*\>!: the requested format in which the key material shall be returned |

| Return ||
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [KeySpec](https://developer.android.com/reference/kotlin/java/security/spec/KeySpec.html#)! | the underlying key specification (key material) in the requested format |

| Exceptions ||
|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.security.spec.InvalidKeySpecException` | if the requested key specification is inappropriate for the given key (e.g., the algorithms associated with `key` and `keySpec` do not match, or `key` references a key on a cryptographic hardware device whereas `keySpec` is the specification of a software-based key), or the given key cannot be dealt with (e.g., the given key has an algorithm or format not supported by this secret-key factory). |

### engineTranslateKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineTranslateKey(key: SecretKey!): SecretKey!
```

Translates a key object, whose provider may be unknown or potentially untrusted, into a corresponding key object of this secret-key factory.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [SecretKey](https://developer.android.com/reference/kotlin/javax/crypto/SecretKey)!: the key whose provider is unknown or untrusted |

| Return ||
|-------------------------------------------------------------------------------------|--------------------|
| [SecretKey](https://developer.android.com/reference/kotlin/javax/crypto/SecretKey)! | the translated key |

| Exceptions ||
|-------------------------------------|------------------------------------------------------------------|
| `java.security.InvalidKeyException` | if the given key cannot be processed by this secret-key factory. |
