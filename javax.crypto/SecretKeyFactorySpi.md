# SecretKeyFactorySpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SecretKeyFactorySpi

```
abstract class SecretKeyFactorySpi
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.crypto.SecretKeyFactorySpi](../javax/crypto/SecretKeyFactorySpi.md) |

This class defines the *Service Provider Interface* (**SPI** ) for the `SecretKeyFactory` class. All the abstract methods in this class must be implemented by each cryptographic service provider who wishes to supply the implementation of a secret-key factory for a particular algorithm.

A provider should document all the key specifications supported by its secret key factory. For example, the DES secret-key factory supplied by the "SunJCE" provider supports `DESKeySpec` as a transparent representation of DES keys, and that provider's secret-key factory for Triple DES keys supports `DESedeKeySpec` as a transparent representation of Triple DES keys.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------|---|
| [SecretKeyFactorySpi](../javax/crypto/SecretKeyFactorySpi.md))`()` <br /> |

| Protected methods ||
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [SecretKey](../javax/crypto/SecretKey.md)! | [engineGenerateSecret](../javax/crypto/SecretKeyFactorySpi.md))`(`keySpec:` ` [KeySpec](../java/security/spec/KeySpec.md)!`)` Generates a `SecretKey` object from the provided key specification (key material). |
| abstract [KeySpec](../java/security/spec/KeySpec.md)! | [engineGetKeySpec](../javax/crypto/SecretKeyFactorySpi.md))`(`key:` ` [SecretKey](../javax/crypto/SecretKey.md)!`, `keySpec:` ` [Class](../java/lang/Class.md)<*>!`)` Returns a specification (key material) of the given key object in the requested format. |
| abstract [SecretKey](../javax/crypto/SecretKey.md)! | [engineTranslateKey](../javax/crypto/SecretKeyFactorySpi.md))`(`key:` ` [SecretKey](../javax/crypto/SecretKey.md)!`)` Translates a key object, whose provider may be unknown or potentially untrusted, into a corresponding key object of this secret-key factory. |
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
| `keySpec` | [KeySpec](../java/security/spec/KeySpec.md)!: the specification (key material) of the secret key |

| Return ||
|-------------------------------------------------------------------------------------|----------------|
| [SecretKey](../javax/crypto/SecretKey.md)! | the secret key |

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
| `key` | [SecretKey](../javax/crypto/SecretKey.md)!: the key |
| `keySpec` | [Class](../java/lang/Class.md)\<\*\>!: the requested format in which the key material shall be returned |

| Return ||
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [KeySpec](../java/security/spec/KeySpec.md)! | the underlying key specification (key material) in the requested format |

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
| `key` | [SecretKey](../javax/crypto/SecretKey.md)!: the key whose provider is unknown or untrusted |

| Return ||
|-------------------------------------------------------------------------------------|--------------------|
| [SecretKey](../javax/crypto/SecretKey.md)! | the translated key |

| Exceptions ||
|-------------------------------------|------------------------------------------------------------------|
| `java.security.InvalidKeyException` | if the given key cannot be processed by this secret-key factory. |
