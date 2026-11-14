# KeyFactorySpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyFactorySpi

```
abstract class KeyFactorySpi
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.security.KeyFactorySpi](https://developer.android.com/reference/kotlin/java/security/KeyFactorySpi#) |

This class defines the *Service Provider Interface* (**SPI** ) for the `KeyFactory` class. All the abstract methods in this class must be implemented by each cryptographic service provider who wishes to supply the implementation of a key factory for a particular algorithm.

Key factories are used to convert *keys* (opaque cryptographic keys of type `Key`) into *key specifications* (transparent representations of the underlying key material), and vice versa.

Key factories are bi-directional. That is, they allow you to build an opaque key object from a given key specification (key material), or to retrieve the underlying key material of a key object in a suitable format.

Multiple compatible key specifications may exist for the same key. For example, a DSA public key may be specified using `DSAPublicKeySpec` or `X509EncodedKeySpec`. A key factory can be used to translate between compatible key specifications.

A provider should document all the key specifications supported by its key factory.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------|---|
| [KeyFactorySpi](https://developer.android.com/reference/kotlin/java/security/KeyFactorySpi#KeyFactorySpi())`()` <br /> |

| Protected methods ||
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey)! | [engineGeneratePrivate](https://developer.android.com/reference/kotlin/java/security/KeyFactorySpi#engineGeneratePrivate(java.security.spec.KeySpec))`(`keySpec:` ` [KeySpec](https://developer.android.com/reference/kotlin/java/security/spec/KeySpec)!`)` Generates a private key object from the provided key specification (key material). |
| abstract [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey)! | [engineGeneratePublic](https://developer.android.com/reference/kotlin/java/security/KeyFactorySpi#engineGeneratePublic(java.security.spec.KeySpec))`(`keySpec:` ` [KeySpec](https://developer.android.com/reference/kotlin/java/security/spec/KeySpec)!`)` Generates a public key object from the provided key specification (key material). |
| abstract T | [engineGetKeySpec](https://developer.android.com/reference/kotlin/java/security/KeyFactorySpi#engineGetKeySpec(java.security.Key,%20java.lang.Class))`(`key:` ` [Key](https://developer.android.com/reference/kotlin/java/security/Key)!`, `keySpec:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>!`)` Returns a specification (key material) of the given key object. |
| abstract [Key](https://developer.android.com/reference/kotlin/java/security/Key)! | [engineTranslateKey](https://developer.android.com/reference/kotlin/java/security/KeyFactorySpi#engineTranslateKey(java.security.Key))`(`key:` ` [Key](https://developer.android.com/reference/kotlin/java/security/Key)!`)` Translates a key object, whose provider may be unknown or potentially untrusted, into a corresponding key object of this key factory. |

## Public constructors

### KeyFactorySpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyFactorySpi()
```

## Protected methods

### engineGeneratePrivate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineGeneratePrivate(keySpec: KeySpec!): PrivateKey!
```

Generates a private key object from the provided key specification (key material).

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `keySpec` | [KeySpec](https://developer.android.com/reference/kotlin/java/security/spec/KeySpec)!: the specification (key material) of the private key. |

| Return ||
|----------------------------------------------------------------------------------------|------------------|
| [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey)! | the private key. |

| Exceptions ||
|----------------------------------------------|------------------------------------------------------------------------------------------------|
| `java.security.spec.InvalidKeySpecException` | if the given key specification is inappropriate for this key factory to produce a private key. |

### engineGeneratePublic

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineGeneratePublic(keySpec: KeySpec!): PublicKey!
```

Generates a public key object from the provided key specification (key material).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `keySpec` | [KeySpec](https://developer.android.com/reference/kotlin/java/security/spec/KeySpec)!: the specification (key material) of the public key. |

| Return ||
|--------------------------------------------------------------------------------------|-----------------|
| [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey)! | the public key. |

| Exceptions ||
|----------------------------------------------|-----------------------------------------------------------------------------------------------|
| `java.security.spec.InvalidKeySpecException` | if the given key specification is inappropriate for this key factory to produce a public key. |

### engineGetKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun <T : KeySpec!> engineGetKeySpec(
    key: Key!, 
    keySpec: Class<T>!
): T
```

Returns a specification (key material) of the given key object. `keySpec` identifies the specification class in which the key material should be returned. It could, for example, be `DSAPublicKeySpec.class`, to indicate that the key material should be returned in an instance of the `DSAPublicKeySpec` class.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the type of the key specification to be returned |
| `key` | [Key](https://developer.android.com/reference/kotlin/java/security/Key)!: the key. |
| `keySpec` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<T\>!: the specification class in which the key material should be returned. |

| Return ||
|---|------------------------------------------------------------------------------------------------------|
| T | the underlying key specification (key material) in an instance of the requested specification class. |

| Exceptions ||
|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.security.spec.InvalidKeySpecException` | if the requested key specification is inappropriate for the given key, or the given key cannot be dealt with (e.g., the given key has an unrecognized format). |

### engineTranslateKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineTranslateKey(key: Key!): Key!
```

Translates a key object, whose provider may be unknown or potentially untrusted, into a corresponding key object of this key factory.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------|
| `key` | [Key](https://developer.android.com/reference/kotlin/java/security/Key)!: the key whose provider is unknown or untrusted. |

| Return ||
|--------------------------------------------------------------------------|---------------------|
| [Key](https://developer.android.com/reference/kotlin/java/security/Key)! | the translated key. |

| Exceptions ||
|-------------------------------------|-----------------------------------------------------------|
| `java.security.InvalidKeyException` | if the given key cannot be processed by this key factory. |
