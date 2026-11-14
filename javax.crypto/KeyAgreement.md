# KeyAgreement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyAgreement

```
open class KeyAgreement
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.crypto.KeyAgreement](KeyAgreement.md) |

This class provides the functionality of a key agreement (or key exchange) protocol.

The keys involved in establishing a shared secret are created by one of the key generators (`KeyPairGenerator`or`KeyGenerator`), a`KeyFactory`, or as a result from an intermediate phase of the key agreement protocol.

For each of the correspondents in the key exchange,`doPhase`needs to be called. For example, if this key exchange is with one other party,`doPhase`needs to be called once, with the`lastPhase`flag set to`true`. If this key exchange is with two other parties,`doPhase`needs to be called twice, the first time setting the`lastPhase`flag to`false`, and the second time setting it to`true`. There may be any number of parties involved in a key exchange.

Android provides the following`KeyAgreement`algorithms:

| Algorithm | Supported API Levels |
|-----------|----------------------|
| DH | 1+ |
| ECDH | 11+ |
| XDH | 33+ |
| --- | --- |

This algorithm is described in the [KeyAgreement section](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#keyagreement-algorithms) of the Java Cryptography Architecture Standard Algorithm Name Documentation.

## Summary

| Protected constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [KeyAgreement](KeyAgreement.md))`(`keyAgreeSpi:` ` [KeyAgreementSpi](KeyAgreementSpi.md)!`, `provider:` ` [Provider](../java.security/Provider.md)!`, `algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a KeyAgreement object. |

| Public methods ||
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Key](../java.security/Key.md)! | [doPhase](KeyAgreement.md))`(`key:` ` [Key](../java.security/Key.md)!`, `lastPhase:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Executes the next phase of this key agreement with the given key that was received from one of the other parties involved in this key agreement. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [generateSecret](KeyAgreement.md))`()` Generates the shared secret and returns it in a new buffer. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [generateSecret](KeyAgreement.md))`(`sharedSecret:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Generates the shared secret, and places it into the buffer`sharedSecret`, beginning at`offset`inclusive. |
| --- | --- |
| [SecretKey](SecretKey.md)! | [generateSecret](KeyAgreement.md))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates the shared secret and returns it as a`SecretKey`object of the specified algorithm. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAlgorithm](KeyAgreement.md))`()` Returns the algorithm name of this`KeyAgreement`object. |
| static [KeyAgreement](KeyAgreement.md)! | [getInstance](KeyAgreement.md))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a`KeyAgreement`object that implements the specified key agreement algorithm. |
| --- | --- |
| static [KeyAgreement](KeyAgreement.md)! | [getInstance](KeyAgreement.md))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a`KeyAgreement`object that implements the specified key agreement algorithm. |
| static [KeyAgreement](KeyAgreement.md)! | [getInstance](KeyAgreement.md))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `provider:` ` [Provider](../java.security/Provider.md)!`)` Returns a`KeyAgreement`object that implements the specified key agreement algorithm. |
| [Provider](../java.security/Provider.md)! | [getProvider](KeyAgreement.md))`()` Returns the provider of this`KeyAgreement`object. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](KeyAgreement.md))`(`key:` ` [Key](../java.security/Key.md)!`)` Initializes this key agreement with the given key, which is required to contain all the algorithm parameters required for this key agreement. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](KeyAgreement.md))`(`key:` ` [Key](../java.security/Key.md)!`, `random:` ` [SecureRandom](../java.security/SecureRandom.md)!`)` Initializes this key agreement with the given key and source of randomness. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](KeyAgreement.md))`(`key:` ` [Key](../java.security/Key.md)!`, `params:` ` [AlgorithmParameterSpec](../java.security.spec/AlgorithmParameterSpec.md)!`)` Initializes this key agreement with the given key and set of algorithm parameters. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](KeyAgreement.md))`(`key:` ` [Key](../java.security/Key.md)!`, `params:` ` [AlgorithmParameterSpec](../java.security.spec/AlgorithmParameterSpec.md)!`, `random:` ` [SecureRandom](../java.security/SecureRandom.md)!`)` Initializes this key agreement with the given key, set of algorithm parameters, and source of randomness. |

## Protected constructors

### KeyAgreement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected KeyAgreement(
    keyAgreeSpi: KeyAgreementSpi!, 
    provider: Provider!, 
    algorithm: String!)
```

Creates a KeyAgreement object.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------|
| `keyAgreeSpi` | [KeyAgreementSpi](KeyAgreementSpi.md)!:the delegate |
| `provider` | [Provider](../java.security/Provider.md)!:the provider |
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the algorithm |
| --- | --- |

## Public methods

### doPhase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun doPhase(
    key: Key!, 
    lastPhase: Boolean
): Key!
```

Executes the next phase of this key agreement with the given key that was received from one of the other parties involved in this key agreement.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [Key](../java.security/Key.md)!:the key for this phase. For example, in the case of Diffie-Hellman between 2 parties, this would be the other party's Diffie-Hellman public key. |
| `lastPhase` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):flag which indicates whether or not this is the last phase of this key agreement. |

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [Key](../java.security/Key.md)! | the (intermediate) key resulting from this phase, or null if this phase does not yield a key |

| Exceptions ||
|-------------------------------------|---------------------------------------------------|
| `java.security.InvalidKeyException` | if the given key is inappropriate for this phase. |
| `java.lang.IllegalStateException` | if this key agreement has not been initialized. |

### generateSecret

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun generateSecret(): ByteArray!
```

Generates the shared secret and returns it in a new buffer.

This method resets this`KeyAgreement`object, so that it can be reused for further key agreements. Unless this key agreement is reinitialized with one of the`init`methods, the same private information and algorithm parameters will be used for subsequent key agreements.

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the new buffer with the shared secret |

| Exceptions ||
|-----------------------------------|--------------------------------------------------|
| `java.lang.IllegalStateException` | if this key agreement has not been completed yet |

### generateSecret

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun generateSecret(
    sharedSecret: ByteArray!, 
    offset: Int
): Int
```

Generates the shared secret, and places it into the buffer`sharedSecret`, beginning at`offset`inclusive.

If the`sharedSecret`buffer is too small to hold the result, a`ShortBufferException`is thrown. In this case, this call should be repeated with a larger output buffer.

This method resets this`KeyAgreement`object, so that it can be reused for further key agreements. Unless this key agreement is reinitialized with one of the`init`methods, the same private information and algorithm parameters will be used for subsequent key agreements.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `sharedSecret` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer for the shared secret |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset in`sharedSecret`where the shared secret will be stored |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of bytes placed into`sharedSecret` |

| Exceptions ||
|-------------------------------------|------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this key agreement has not been completed yet |
| `javax.crypto.ShortBufferException` | if the given output buffer is too small to hold the secret |

### generateSecret

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun generateSecret(algorithm: String!): SecretKey!
```

Creates the shared secret and returns it as a`SecretKey`object of the specified algorithm.

This method resets this`KeyAgreement`object, so that it can be reused for further key agreements. Unless this key agreement is reinitialized with one of the`init`methods, the same private information and algorithm parameters will be used for subsequent key agreements.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the requested secret-key algorithm |

| Return ||
|-------------------------------------------------------------------------------------|-----------------------|
| [SecretKey](SecretKey.md)! | the shared secret key |

| Exceptions ||
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this key agreement has not been completed yet |
| `java.security.NoSuchAlgorithmException` | if the specified secret-key algorithm is not available |
| `java.security.InvalidKeyException` | if the shared secret-key material cannot be used to generate a secret key of the specified algorithm (e.g., the key material is too short) |
| --- | --- |

### getAlgorithm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAlgorithm(): String!
```

Returns the algorithm name of this`KeyAgreement`object.

This is the same name that was specified in one of the`getInstance`calls that created this`KeyAgreement`object.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the algorithm name of this`KeyAgreement`object. |

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(algorithm: String!): KeyAgreement!
```

Returns a`KeyAgreement`object that implements the specified key agreement algorithm.

This method traverses the list of registered security Providers, starting with the most preferred Provider. A new KeyAgreement object encapsulating the KeyAgreementSpi implementation from the first Provider that supports the specified algorithm is returned.

Note that the list of registered providers may be retrieved via the [Security.getProviders()](../java.security/Security.md))method.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the standard name of the requested key agreement algorithm. See the KeyAgreement section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#keyagreement-algorithms) for information about standard algorithm names. |

| Return ||
|--------------------------------------------------------------------------------------------|-----------------------------|
| [KeyAgreement](KeyAgreement.md)! | the new`KeyAgreement`object |

| Exceptions ||
|------------------------------------------|---------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified algorithm is null. |
| `java.security.NoSuchAlgorithmException` | if no Provider supports a KeyAgreementSpi implementation for the specified algorithm. |

**See Also**

- [java.security.Provider](../java.security/Provider.md) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(
    algorithm: String!, 
    provider: String!
): KeyAgreement!
```

Returns a`KeyAgreement`object that implements the specified key agreement algorithm.

A new KeyAgreement object encapsulating the KeyAgreementSpi implementation from the specified provider is returned. The specified provider must be registered in the security provider list.

Note that the list of registered providers may be retrieved via the [Security.getProviders()](../java.security/Security.md))method.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the standard name of the requested key agreement algorithm. See the KeyAgreement section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#keyagreement-algorithms) for information about standard algorithm names. |
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the provider. |

| Return ||
|--------------------------------------------------------------------------------------------|-----------------------------|
| [KeyAgreement](KeyAgreement.md)! | the new`KeyAgreement`object |

| Exceptions ||
|------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified algorithm is null. |
| `java.security.NoSuchAlgorithmException` | if a KeyAgreementSpi implementation for the specified algorithm is not available from the specified provider. |
| `java.security.NoSuchProviderException` | if the specified provider is not registered in the security provider list. |
| --- | --- |
| `java.lang.IllegalArgumentException` | if the`provider`is null or empty. |

**See Also**

- [java.security.Provider](../java.security/Provider.md) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(
    algorithm: String!, 
    provider: Provider!
): KeyAgreement!
```

Returns a`KeyAgreement`object that implements the specified key agreement algorithm.

A new KeyAgreement object encapsulating the KeyAgreementSpi implementation from the specified Provider object is returned. Note that the specified Provider object does not have to be registered in the provider list.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the standard name of the requested key agreement algorithm. See the KeyAgreement section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#keyagreement-algorithms) for information about standard algorithm names. |
| `provider` | [Provider](../java.security/Provider.md)!:the provider. |

| Return ||
|--------------------------------------------------------------------------------------------|-----------------------------|
| [KeyAgreement](KeyAgreement.md)! | the new`KeyAgreement`object |

| Exceptions ||
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified algorithm is null. |
| `java.security.NoSuchAlgorithmException` | if a KeyAgreementSpi implementation for the specified algorithm is not available from the specified Provider object. |
| `java.lang.IllegalArgumentException` | if the`provider`is null. |
| --- | --- |

**See Also**

- [java.security.Provider](../java.security/Provider.md) 

### getProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getProvider(): Provider!
```

Returns the provider of this`KeyAgreement`object.

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------|
| [Provider](../java.security/Provider.md)! | the provider of this`KeyAgreement`object |

### init

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun init(key: Key!): Unit
```

Initializes this key agreement with the given key, which is required to contain all the algorithm parameters required for this key agreement.

If this key agreement requires any random bytes, it will get them using the [java.security.SecureRandom](../java.security/SecureRandom.md) implementation of the highest-priority installed provider as the source of randomness. (If none of the installed providers supply an implementation of SecureRandom, a system-provided source of randomness will be used.)

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [Key](../java.security/Key.md)!:the party's private information. For example, in the case of the Diffie-Hellman key agreement, this would be the party's own Diffie-Hellman private key. |

| Exceptions ||
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| `java.security.InvalidKeyException` | if the given key is inappropriate for this key agreement, e.g., is of the wrong type or has an incompatible algorithm type. |

### init

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun init(
    key: Key!, 
    random: SecureRandom!
): Unit
```

Initializes this key agreement with the given key and source of randomness. The given key is required to contain all the algorithm parameters required for this key agreement.

If the key agreement algorithm requires random bytes, it gets them from the given source of randomness,`random`. However, if the underlying algorithm implementation does not require any random bytes,`random`is ignored.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [Key](../java.security/Key.md)!:the party's private information. For example, in the case of the Diffie-Hellman key agreement, this would be the party's own Diffie-Hellman private key. |
| `random` | [SecureRandom](../java.security/SecureRandom.md)!:the source of randomness |

| Exceptions ||
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| `java.security.InvalidKeyException` | if the given key is inappropriate for this key agreement, e.g., is of the wrong type or has an incompatible algorithm type. |

### init

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun init(
    key: Key!, 
    params: AlgorithmParameterSpec!
): Unit
```

Initializes this key agreement with the given key and set of algorithm parameters.

If this key agreement requires any random bytes, it will get them using the [java.security.SecureRandom](../java.security/SecureRandom.md) implementation of the highest-priority installed provider as the source of randomness. (If none of the installed providers supply an implementation of SecureRandom, a system-provided source of randomness will be used.)

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [Key](../java.security/Key.md)!:the party's private information. For example, in the case of the Diffie-Hellman key agreement, this would be the party's own Diffie-Hellman private key. |
| `params` | [AlgorithmParameterSpec](../java.security.spec/AlgorithmParameterSpec.md)!:the key agreement parameters |

| Exceptions ||
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| `java.security.InvalidKeyException` | if the given key is inappropriate for this key agreement, e.g., is of the wrong type or has an incompatible algorithm type. |
| `java.security.InvalidAlgorithmParameterException` | if the given parameters are inappropriate for this key agreement. |

### init

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun init(
    key: Key!, 
    params: AlgorithmParameterSpec!, 
    random: SecureRandom!
): Unit
```

Initializes this key agreement with the given key, set of algorithm parameters, and source of randomness.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [Key](../java.security/Key.md)!:the party's private information. For example, in the case of the Diffie-Hellman key agreement, this would be the party's own Diffie-Hellman private key. |
| `params` | [AlgorithmParameterSpec](../java.security.spec/AlgorithmParameterSpec.md)!:the key agreement parameters |
| `random` | [SecureRandom](../java.security/SecureRandom.md)!:the source of randomness |
| --- | --- |

| Exceptions ||
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| `java.security.InvalidKeyException` | if the given key is inappropriate for this key agreement, e.g., is of the wrong type or has an incompatible algorithm type. |
| `java.security.InvalidAlgorithmParameterException` | if the given parameters are inappropriate for this key agreement. |
