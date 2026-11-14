# SecretKeyFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SecretKeyFactory

```
open class SecretKeyFactory
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [javax.crypto.SecretKeyFactory](https://developer.android.com/reference/kotlin/javax/crypto/SecretKeyFactory#) |

This class represents a factory for secret keys.

Key factories are used to convert*keys* (opaque cryptographic keys of type`Key`) into*key specifications*(transparent representations of the underlying key material), and vice versa. Secret key factories operate only on secret (symmetric) keys.

Key factories are bi-directional, i.e., they allow to build an opaque key object from a given key specification (key material), or to retrieve the underlying key material of a key object in a suitable format.

Application developers should refer to their provider's documentation to find out which key specifications are supported by the [generateSecret](https://developer.android.com/reference/kotlin/javax/crypto/SecretKeyFactory#generateSecret(java.security.spec.KeySpec))and [getKeySpec](https://developer.android.com/reference/kotlin/javax/crypto/SecretKeyFactory#getKeySpec(javax.crypto.SecretKey,%20java.lang.Class))methods. For example, the DES secret-key factory supplied by the "SunJCE" provider supports`DESKeySpec`as a transparent representation of DES keys, and that provider's secret-key factory for Triple DES keys supports`DESedeKeySpec`as a transparent representation of Triple DES keys.

Android provides the following`SecretKeyFactory`algorithms:

| Algorithm | Supported API Levels |
|------------------------------------|----------------------|
| AES | 23+ |
| DES | 1+ |
| DESede | 1+ |
| HmacSHA1 | 23+ |
| HmacSHA224 | 23+ |
| HmacSHA256 | 23+ |
| HmacSHA384 | 23+ |
| HmacSHA512 | 23+ |
| PBEwithHmacSHA1 | 1+ |
| PBEwithHmacSHA1AndAES_128 | 26+ |
| PBEwithHmacSHA1AndAES_256 | 26+ |
| PBEwithHmacSHA224AndAES_128 | 26+ |
| PBEwithHmacSHA224AndAES_256 | 26+ |
| PBEwithHmacSHA256AndAES_128 | 26+ |
| PBEwithHmacSHA256AndAES_256 | 26+ |
| PBEwithHmacSHA384AndAES_128 | 26+ |
| PBEwithHmacSHA384AndAES_256 | 26+ |
| PBEwithHmacSHA512AndAES_128 | 26+ |
| PBEwithHmacSHA512AndAES_256 | 26+ |
| PBEwithMD5AND128BITAES-CBC-OPENSSL | 1+ |
| PBEwithMD5AND192BITAES-CBC-OPENSSL | 1+ |
| PBEwithMD5AND256BITAES-CBC-OPENSSL | 1+ |
| PBEwithMD5ANDDES | 1+ |
| PBEwithMD5ANDRC2 | 1+ |
| PBEwithSHA1ANDDES | 1+ |
| PBEwithSHA1ANDRC2 | 1+ |
| PBEwithSHA256AND128BITAES-CBC-BC | 1+ |
| PBEwithSHA256AND192BITAES-CBC-BC | 1+ |
| PBEwithSHA256AND256BITAES-CBC-BC | 1+ |
| PBEwithSHAAND128BITAES-CBC-BC | 1+ |
| PBEwithSHAAND128BITRC2-CBC | 10+ |
| PBEwithSHAAND128BITRC4 | 10+ |
| PBEwithSHAAND192BITAES-CBC-BC | 1+ |
| PBEwithSHAAND2-KEYTRIPLEDES-CBC | 1+ |
| PBEwithSHAAND256BITAES-CBC-BC | 1+ |
| PBEwithSHAAND3-KEYTRIPLEDES-CBC | 1+ |
| PBEwithSHAAND40BITRC2-CBC | 1+ |
| PBEwithSHAAND40BITRC4 | 10+ |
| PBEwithSHAANDTWOFISH-CBC | 10+ |
| PBKDF2withHmacSHA1 | 10+ |
| PBKDF2withHmacSHA1And8BIT | 19+ |
| PBKDF2withHmacSHA224 | 26+ |
| PBKDF2withHmacSHA256 | 26+ |
| PBKDF2withHmacSHA384 | 26+ |
| PBKDF2withHmacSHA512 | 26+ |

These algorithms are described in the [SecretKeyFactory section](https://docs.oracle.com/javase/8/docs/technotes/guides/security/StandardNames.html#SecretKeyFactory) of the Java Cryptography Architecture Standard Algorithm Name Documentation.

## Summary

| Protected constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SecretKeyFactory](https://developer.android.com/reference/kotlin/javax/crypto/SecretKeyFactory#SecretKeyFactory(javax.crypto.SecretKeyFactorySpi,%20java.security.Provider,%20kotlin.String))`(`keyFacSpi:` ` [SecretKeyFactorySpi](https://developer.android.com/reference/kotlin/javax/crypto/SecretKeyFactorySpi)!`, `provider:` ` [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)!`, `algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a SecretKeyFactory object. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SecretKey](https://developer.android.com/reference/kotlin/javax/crypto/SecretKey)! | [generateSecret](https://developer.android.com/reference/kotlin/javax/crypto/SecretKeyFactory#generateSecret(java.security.spec.KeySpec))`(`keySpec:` ` [KeySpec](https://developer.android.com/reference/kotlin/java/security/spec/KeySpec.html#)!`)` Generates a`SecretKey`object from the provided key specification (key material). |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAlgorithm](https://developer.android.com/reference/kotlin/javax/crypto/SecretKeyFactory#getAlgorithm())`()` Returns the algorithm name of this`SecretKeyFactory`object. |
| static [SecretKeyFactory](https://developer.android.com/reference/kotlin/javax/crypto/SecretKeyFactory#)! | [getInstance](https://developer.android.com/reference/kotlin/javax/crypto/SecretKeyFactory#getInstance(kotlin.String))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a`SecretKeyFactory`object that converts secret keys of the specified algorithm. |
| static [SecretKeyFactory](https://developer.android.com/reference/kotlin/javax/crypto/SecretKeyFactory#)! | [getInstance](https://developer.android.com/reference/kotlin/javax/crypto/SecretKeyFactory#getInstance(kotlin.String,%20kotlin.String))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a`SecretKeyFactory`object that converts secret keys of the specified algorithm. |
| static [SecretKeyFactory](https://developer.android.com/reference/kotlin/javax/crypto/SecretKeyFactory#)! | [getInstance](https://developer.android.com/reference/kotlin/javax/crypto/SecretKeyFactory#getInstance(kotlin.String,%20java.security.Provider))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `provider:` ` [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)!`)` Returns a`SecretKeyFactory`object that converts secret keys of the specified algorithm. |
| [KeySpec](https://developer.android.com/reference/kotlin/java/security/spec/KeySpec.html#)! | [getKeySpec](https://developer.android.com/reference/kotlin/javax/crypto/SecretKeyFactory#getKeySpec(javax.crypto.SecretKey,%20java.lang.Class))`(`key:` ` [SecretKey](https://developer.android.com/reference/kotlin/javax/crypto/SecretKey)!`, `keySpec:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<*>!`)` Returns a specification (key material) of the given key object in the requested format. |
| [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)! | [getProvider](https://developer.android.com/reference/kotlin/javax/crypto/SecretKeyFactory#getProvider())`()` Returns the provider of this`SecretKeyFactory`object. |
| [SecretKey](https://developer.android.com/reference/kotlin/javax/crypto/SecretKey)! | [translateKey](https://developer.android.com/reference/kotlin/javax/crypto/SecretKeyFactory#translateKey(javax.crypto.SecretKey))`(`key:` ` [SecretKey](https://developer.android.com/reference/kotlin/javax/crypto/SecretKey)!`)` Translates a key object, whose provider may be unknown or potentially untrusted, into a corresponding key object of this secret-key factory. |

## Protected constructors

### SecretKeyFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected SecretKeyFactory(
    keyFacSpi: SecretKeyFactorySpi!, 
    provider: Provider!, 
    algorithm: String!)
```

Creates a SecretKeyFactory object.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------|
| `keyFacSpi` | [SecretKeyFactorySpi](https://developer.android.com/reference/kotlin/javax/crypto/SecretKeyFactorySpi)!:the delegate |
| `provider` | [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)!:the provider |
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the secret-key algorithm |

## Public methods

### generateSecret

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun generateSecret(keySpec: KeySpec!): SecretKey!
```

Generates a`SecretKey`object from the provided key specification (key material).

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `keySpec` | [KeySpec](https://developer.android.com/reference/kotlin/java/security/spec/KeySpec.html#)!:the specification (key material) of the secret key |

| Return ||
|-------------------------------------------------------------------------------------|----------------|
| [SecretKey](https://developer.android.com/reference/kotlin/javax/crypto/SecretKey)! | the secret key |

| Exceptions ||
|----------------------------------------------|------------------------------------------------------------------------------------------------------|
| `java.security.spec.InvalidKeySpecException` | if the given key specification is inappropriate for this secret-key factory to produce a secret key. |

### getAlgorithm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAlgorithm(): String!
```

Returns the algorithm name of this`SecretKeyFactory`object.

This is the same name that was specified in one of the`getInstance`calls that created this`SecretKeyFactory`object.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the algorithm name of this`SecretKeyFactory`object. |

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(algorithm: String!): SecretKeyFactory!
```

Returns a`SecretKeyFactory`object that converts secret keys of the specified algorithm.

This method traverses the list of registered security Providers, starting with the most preferred Provider. A new SecretKeyFactory object encapsulating the SecretKeyFactorySpi implementation from the first Provider that supports the specified algorithm is returned.

Note that the list of registered providers may be retrieved via the [Security.getProviders()](https://developer.android.com/reference/kotlin/java/security/Security.html#getProviders())method.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the standard name of the requested secret-key algorithm. See the SecretKeyFactory section in the [Java Cryptography Architecture Standard Algorithm Name Documentation](https://docs.oracle.com/javase/8/docs/technotes/guides/security/StandardNames.html#SecretKeyFactory) for information about standard algorithm names. |

| Return ||
|----------------------------------------------------------------------------------------------------|----------------------------------|
| [SecretKeyFactory](https://developer.android.com/reference/kotlin/javax/crypto/SecretKeyFactory#)! | the new`SecretKeyFactory`object. |

| Exceptions ||
|------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified algorithm is null. |
| `java.security.NoSuchAlgorithmException` | if no Provider supports a SecretKeyFactorySpi implementation for the specified algorithm. |

**See Also**

- [java.security.Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(
    algorithm: String!, 
    provider: String!
): SecretKeyFactory!
```

Returns a`SecretKeyFactory`object that converts secret keys of the specified algorithm.

A new SecretKeyFactory object encapsulating the SecretKeyFactorySpi implementation from the specified provider is returned. The specified provider must be registered in the security provider list.

Note that the list of registered providers may be retrieved via the [Security.getProviders()](https://developer.android.com/reference/kotlin/java/security/Security.html#getProviders())method.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the standard name of the requested secret-key algorithm. See the SecretKeyFactory section in the [Java Cryptography Architecture Standard Algorithm Name Documentation](https://docs.oracle.com/javase/8/docs/technotes/guides/security/StandardNames.html#SecretKeyFactory) for information about standard algorithm names. |
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the provider. |

| Return ||
|----------------------------------------------------------------------------------------------------|----------------------------------|
| [SecretKeyFactory](https://developer.android.com/reference/kotlin/javax/crypto/SecretKeyFactory#)! | the new`SecretKeyFactory`object. |

| Exceptions ||
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| `java.security.NoSuchProviderException` | if the specified provider is not registered in the security provider list. |
| `java.security.NoSuchAlgorithmException` | if a SecretKeyFactorySpi implementation for the specified algorithm is not available from the specified provider. |
| `java.lang.NullPointerException` | if the specified algorithm is null. |
| `java.lang.IllegalArgumentException` | if the`provider`is null or empty. |

**See Also**

- [java.security.Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(
    algorithm: String!, 
    provider: Provider!
): SecretKeyFactory!
```

Returns a`SecretKeyFactory`object that converts secret keys of the specified algorithm.

A new SecretKeyFactory object encapsulating the SecretKeyFactorySpi implementation from the specified Provider object is returned. Note that the specified Provider object does not have to be registered in the provider list.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the standard name of the requested secret-key algorithm. See the SecretKeyFactory section in the [Java Cryptography Architecture Standard Algorithm Name Documentation](https://docs.oracle.com/javase/8/docs/technotes/guides/security/StandardNames.html#SecretKeyFactory) for information about standard algorithm names. |
| `provider` | [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)!:the provider. |

| Return ||
|----------------------------------------------------------------------------------------------------|----------------------------------|
| [SecretKeyFactory](https://developer.android.com/reference/kotlin/javax/crypto/SecretKeyFactory#)! | the new`SecretKeyFactory`object. |

| Exceptions ||
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified algorithm is null. |
| `java.security.NoSuchAlgorithmException` | if a SecretKeyFactorySpi implementation for the specified algorithm is not available from the specified Provider object. |
| `java.lang.IllegalArgumentException` | if the`provider`is null. |

**See Also**

- [java.security.Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#) 

### getKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getKeySpec(
    key: SecretKey!, 
    keySpec: Class<*>!
): KeySpec!
```

Returns a specification (key material) of the given key object in the requested format.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [SecretKey](https://developer.android.com/reference/kotlin/javax/crypto/SecretKey)!:the key |
| `keySpec` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<\*\>!:the requested format in which the key material shall be returned |

| Return ||
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [KeySpec](https://developer.android.com/reference/kotlin/java/security/spec/KeySpec.html#)! | the underlying key specification (key material) in the requested format |

| Exceptions ||
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.security.spec.InvalidKeySpecException` | if the requested key specification is inappropriate for the given key (e.g., the algorithms associated with`key`and`keySpec`do not match, or`key`references a key on a cryptographic hardware device whereas`keySpec`is the specification of a software-based key), or the given key cannot be dealt with (e.g., the given key has an algorithm or format not supported by this secret-key factory). |

### getProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getProvider(): Provider!
```

Returns the provider of this`SecretKeyFactory`object.

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------------|
| [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)! | the provider of this`SecretKeyFactory`object |

### translateKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun translateKey(key: SecretKey!): SecretKey!
```

Translates a key object, whose provider may be unknown or potentially untrusted, into a corresponding key object of this secret-key factory.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [SecretKey](https://developer.android.com/reference/kotlin/javax/crypto/SecretKey)!:the key whose provider is unknown or untrusted |

| Return ||
|-------------------------------------------------------------------------------------|--------------------|
| [SecretKey](https://developer.android.com/reference/kotlin/javax/crypto/SecretKey)! | the translated key |

| Exceptions ||
|-------------------------------------|------------------------------------------------------------------|
| `java.security.InvalidKeyException` | if the given key cannot be processed by this secret-key factory. |
