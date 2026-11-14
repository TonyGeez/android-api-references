# KeyGenerator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyGenerator

```
open class KeyGenerator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [javax.crypto.KeyGenerator](https://developer.android.com/reference/kotlin/javax/crypto/KeyGenerator#) |

This class provides the functionality of a secret (symmetric) key generator.

Key generators are constructed using one of the`getInstance`class methods of this class.

KeyGenerator objects are reusable, i.e., after a key has been generated, the same KeyGenerator object can be re-used to generate further keys.

There are two ways to generate a key: in an algorithm-independent manner, and in an algorithm-specific manner. The only difference between the two is the initialization of the object:

- **Algorithm-Independent Initialization**

 All key generators share the concepts of a*keysize* and a*source of randomness* . There is an [init](https://developer.android.com/reference/kotlin/javax/crypto/KeyGenerator#init(kotlin.Int,%20java.security.SecureRandom))method in this KeyGenerator class that takes these two universally shared types of arguments. There is also one that takes just a`keysize`argument, and uses the SecureRandom implementation of the highest-priority installed provider as the source of randomness (or a system-provided source of randomness if none of the installed providers supply a SecureRandom implementation), and one that takes just a source of randomness.

 Since no other parameters are specified when you call the above algorithm-independent`init`methods, it is up to the provider what to do about the algorithm-specific parameters (if any) to be associated with each of the keys.
- **Algorithm-Specific Initialization**

 For situations where a set of algorithm-specific parameters already exists, there are two [init](https://developer.android.com/reference/kotlin/javax/crypto/KeyGenerator#init(java.security.spec.AlgorithmParameterSpec))methods that have an`AlgorithmParameterSpec`argument. One also has a`SecureRandom`argument, while the other uses the SecureRandom implementation of the highest-priority installed provider as the source of randomness (or a system-provided source of randomness if none of the installed providers supply a SecureRandom implementation).

In case the client does not explicitly initialize the KeyGenerator (via a call to an`init`method), each provider must supply (and document) a default initialization.

Android provides the following`KeyGenerator`algorithms:

| Algorithm | Supported API Levels |
|------------|----------------------|
| AES | 1+ |
| AESWRAP | 1-8 |
| ARC4 | 14+ |
| BLOWFISH | 10+ |
| ChaCha20 | 28+ |
| DES | 1+ |
| DESede | 1+ |
| DESedeWRAP | 1-8 |
| HmacMD5 | 1+ |
| HmacSHA1 | 11+ |
| HmacSHA224 | 1-8,22+ |
| HmacSHA256 | 1+ |
| HmacSHA384 | 1+ |
| HmacSHA512 | 1+ |
| RC4 | 10-13 |

These algorithms are described in the [KeyGenerator section](https://docs.oracle.com/javase/8/docs/technotes/guides/security/StandardNames.html#KeyGenerator) of the Java Cryptography Architecture Standard Algorithm Name Documentation.

## Summary

| Protected constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [KeyGenerator](https://developer.android.com/reference/kotlin/javax/crypto/KeyGenerator#KeyGenerator(javax.crypto.KeyGeneratorSpi,%20java.security.Provider,%20kotlin.String))`(`keyGenSpi:` ` [KeyGeneratorSpi](https://developer.android.com/reference/kotlin/javax/crypto/KeyGeneratorSpi)!`, `provider:` ` [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)!`, `algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a KeyGenerator object. |

| Public methods ||
|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SecretKey](https://developer.android.com/reference/kotlin/javax/crypto/SecretKey)! | [generateKey](https://developer.android.com/reference/kotlin/javax/crypto/KeyGenerator#generateKey())`()` Generates a secret key. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAlgorithm](https://developer.android.com/reference/kotlin/javax/crypto/KeyGenerator#getAlgorithm())`()` Returns the algorithm name of this`KeyGenerator`object. |
| static [KeyGenerator](https://developer.android.com/reference/kotlin/javax/crypto/KeyGenerator#)! | [getInstance](https://developer.android.com/reference/kotlin/javax/crypto/KeyGenerator#getInstance(kotlin.String))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a`KeyGenerator`object that generates secret keys for the specified algorithm. |
| static [KeyGenerator](https://developer.android.com/reference/kotlin/javax/crypto/KeyGenerator#)! | [getInstance](https://developer.android.com/reference/kotlin/javax/crypto/KeyGenerator#getInstance(kotlin.String,%20kotlin.String))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a`KeyGenerator`object that generates secret keys for the specified algorithm. |
| static [KeyGenerator](https://developer.android.com/reference/kotlin/javax/crypto/KeyGenerator#)! | [getInstance](https://developer.android.com/reference/kotlin/javax/crypto/KeyGenerator#getInstance(kotlin.String,%20java.security.Provider))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `provider:` ` [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)!`)` Returns a`KeyGenerator`object that generates secret keys for the specified algorithm. |
| [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)! | [getProvider](https://developer.android.com/reference/kotlin/javax/crypto/KeyGenerator#getProvider())`()` Returns the provider of this`KeyGenerator`object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](https://developer.android.com/reference/kotlin/javax/crypto/KeyGenerator#init(kotlin.Int))`(`keysize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Initializes this key generator for a certain keysize. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](https://developer.android.com/reference/kotlin/javax/crypto/KeyGenerator#init(kotlin.Int,%20java.security.SecureRandom))`(`keysize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `random:` ` [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom.html#)!`)` Initializes this key generator for a certain keysize, using a user-provided source of randomness. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](https://developer.android.com/reference/kotlin/javax/crypto/KeyGenerator#init(java.security.SecureRandom))`(`random:` ` [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom.html#)!`)` Initializes this key generator. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](https://developer.android.com/reference/kotlin/javax/crypto/KeyGenerator#init(java.security.spec.AlgorithmParameterSpec))`(`params:` ` [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#)!`)` Initializes this key generator with the specified parameter set. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](https://developer.android.com/reference/kotlin/javax/crypto/KeyGenerator#init(java.security.spec.AlgorithmParameterSpec,%20java.security.SecureRandom))`(`params:` ` [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#)!`, `random:` ` [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom.html#)!`)` Initializes this key generator with the specified parameter set and a user-provided source of randomness. |

## Protected constructors

### KeyGenerator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected KeyGenerator(
    keyGenSpi: KeyGeneratorSpi!, 
    provider: Provider!, 
    algorithm: String!)
```

Creates a KeyGenerator object.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------|
| `keyGenSpi` | [KeyGeneratorSpi](https://developer.android.com/reference/kotlin/javax/crypto/KeyGeneratorSpi)!:the delegate |
| `provider` | [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)!:the provider |
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the algorithm |

## Public methods

### generateKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun generateKey(): SecretKey!
```

Generates a secret key.

| Return ||
|-------------------------------------------------------------------------------------|-------------|
| [SecretKey](https://developer.android.com/reference/kotlin/javax/crypto/SecretKey)! | the new key |

### getAlgorithm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAlgorithm(): String!
```

Returns the algorithm name of this`KeyGenerator`object.

This is the same name that was specified in one of the`getInstance`calls that created this`KeyGenerator`object.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the algorithm name of this`KeyGenerator`object. |

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(algorithm: String!): KeyGenerator!
```

Returns a`KeyGenerator`object that generates secret keys for the specified algorithm.

This method traverses the list of registered security Providers, starting with the most preferred Provider. A new KeyGenerator object encapsulating the KeyGeneratorSpi implementation from the first Provider that supports the specified algorithm is returned.

Note that the list of registered providers may be retrieved via the [Security.getProviders()](https://developer.android.com/reference/kotlin/java/security/Security.html#getProviders())method.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the standard name of the requested key algorithm. See the KeyGenerator section in the [Java Cryptography Architecture Standard Algorithm Name Documentation](https://docs.oracle.com/javase/8/docs/technotes/guides/security/StandardNames.html#KeyGenerator) for information about standard algorithm names. |

| Return ||
|--------------------------------------------------------------------------------------------|------------------------------|
| [KeyGenerator](https://developer.android.com/reference/kotlin/javax/crypto/KeyGenerator#)! | the new`KeyGenerator`object. |

| Exceptions ||
|------------------------------------------|---------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified algorithm is null. |
| `java.security.NoSuchAlgorithmException` | if no Provider supports a KeyGeneratorSpi implementation for the specified algorithm. |

**See Also**

- [java.security.Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(
    algorithm: String!, 
    provider: String!
): KeyGenerator!
```

Returns a`KeyGenerator`object that generates secret keys for the specified algorithm.

A new KeyGenerator object encapsulating the KeyGeneratorSpi implementation from the specified provider is returned. The specified provider must be registered in the security provider list.

Note that the list of registered providers may be retrieved via the [Security.getProviders()](https://developer.android.com/reference/kotlin/java/security/Security.html#getProviders())method.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the standard name of the requested key algorithm. See the KeyGenerator section in the [Java Cryptography Architecture Standard Algorithm Name Documentation](https://docs.oracle.com/javase/8/docs/technotes/guides/security/StandardNames.html#KeyGenerator) for information about standard algorithm names. |
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the provider. |

| Return ||
|--------------------------------------------------------------------------------------------|------------------------------|
| [KeyGenerator](https://developer.android.com/reference/kotlin/javax/crypto/KeyGenerator#)! | the new`KeyGenerator`object. |

| Exceptions ||
|------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified algorithm is null. |
| `java.security.NoSuchAlgorithmException` | if a KeyGeneratorSpi implementation for the specified algorithm is not available from the specified provider. |
| `java.security.NoSuchProviderException` | if the specified provider is not registered in the security provider list. |
| `java.lang.IllegalArgumentException` | if the`provider`is null or empty. |

**See Also**

- [java.security.Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(
    algorithm: String!, 
    provider: Provider!
): KeyGenerator!
```

Returns a`KeyGenerator`object that generates secret keys for the specified algorithm.

A new KeyGenerator object encapsulating the KeyGeneratorSpi implementation from the specified Provider object is returned. Note that the specified Provider object does not have to be registered in the provider list.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the standard name of the requested key algorithm. See the KeyGenerator section in the [Java Cryptography Architecture Standard Algorithm Name Documentation](https://docs.oracle.com/javase/8/docs/technotes/guides/security/StandardNames.html#KeyGenerator) for information about standard algorithm names. |
| `provider` | [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)!:the provider. |

| Return ||
|--------------------------------------------------------------------------------------------|------------------------------|
| [KeyGenerator](https://developer.android.com/reference/kotlin/javax/crypto/KeyGenerator#)! | the new`KeyGenerator`object. |

| Exceptions ||
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified algorithm is null. |
| `java.security.NoSuchAlgorithmException` | if a KeyGeneratorSpi implementation for the specified algorithm is not available from the specified Provider object. |
| `java.lang.IllegalArgumentException` | if the`provider`is null. |

**See Also**

- [java.security.Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#) 

### getProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getProvider(): Provider!
```

Returns the provider of this`KeyGenerator`object.

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------|
| [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)! | the provider of this`KeyGenerator`object |

### init

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun init(keysize: Int): Unit
```

Initializes this key generator for a certain keysize.

If this key generator requires any random bytes, it will get them using the [java.security.SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom.html#) implementation of the highest-priority installed provider as the source of randomness. (If none of the installed providers supply an implementation of SecureRandom, a system-provided source of randomness will be used.)

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `keysize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the keysize. This is an algorithm-specific metric, specified in number of bits. |

| Exceptions ||
|-------------------------------------------|-------------------------------------------|
| `java.security.InvalidParameterException` | if the keysize is wrong or not supported. |

### init

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun init(
    keysize: Int, 
    random: SecureRandom!
): Unit
```

Initializes this key generator for a certain keysize, using a user-provided source of randomness.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `keysize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the keysize. This is an algorithm-specific metric, specified in number of bits. |
| `random` | [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom.html#)!:the source of randomness for this key generator |

| Exceptions ||
|-------------------------------------------|-------------------------------------------|
| `java.security.InvalidParameterException` | if the keysize is wrong or not supported. |

### init

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun init(random: SecureRandom!): Unit
```

Initializes this key generator.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `random` | [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom.html#)!:the source of randomness for this generator |

### init

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun init(params: AlgorithmParameterSpec!): Unit
```

Initializes this key generator with the specified parameter set.

If this key generator requires any random bytes, it will get them using the [java.security.SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom.html#) implementation of the highest-priority installed provider as the source of randomness. (If none of the installed providers supply an implementation of SecureRandom, a system-provided source of randomness will be used.)

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `params` | [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#)!:the key generation parameters |

| Exceptions ||
|----------------------------------------------------|------------------------------------------------------------------|
| `java.security.InvalidAlgorithmParameterException` | if the given parameters are inappropriate for this key generator |

### init

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun init(
    params: AlgorithmParameterSpec!, 
    random: SecureRandom!
): Unit
```

Initializes this key generator with the specified parameter set and a user-provided source of randomness.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `params` | [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#)!:the key generation parameters |
| `random` | [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom.html#)!:the source of randomness for this key generator |

| Exceptions ||
|----------------------------------------------------|---------------------------------------------------|
| `java.security.InvalidAlgorithmParameterException` | if`params`is inappropriate for this key generator |
