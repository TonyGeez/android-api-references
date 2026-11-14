# KeyAgreementSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyAgreementSpi

```
abstract class KeyAgreementSpi
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [javax.crypto.KeyAgreementSpi](https://developer.android.com/reference/kotlin/javax/crypto/KeyAgreementSpi#) |

This class defines the*Service Provider Interface* (**SPI** ) for the`KeyAgreement`class. All the abstract methods in this class must be implemented by each cryptographic service provider who wishes to supply the implementation of a particular key agreement algorithm.

The keys involved in establishing a shared secret are created by one of the key generators (`KeyPairGenerator`or`KeyGenerator`), a`KeyFactory`, or as a result from an intermediate phase of the key agreement protocol ([engineDoPhase](https://developer.android.com/reference/kotlin/javax/crypto/KeyAgreementSpi#engineDoPhase(java.security.Key,%20kotlin.Boolean))).

For each of the correspondents in the key exchange,`engineDoPhase`needs to be called. For example, if the key exchange is with one other party,`engineDoPhase`needs to be called once, with the`lastPhase`flag set to`true`. If the key exchange is with two other parties,`engineDoPhase`needs to be called twice, the first time setting the`lastPhase`flag to`false`, and the second time setting it to`true`. There may be any number of parties involved in a key exchange.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------|---|
| [KeyAgreementSpi](https://developer.android.com/reference/kotlin/javax/crypto/KeyAgreementSpi#KeyAgreementSpi())`()` <br /> |

| Protected methods ||
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#)! | [engineDoPhase](https://developer.android.com/reference/kotlin/javax/crypto/KeyAgreementSpi#engineDoPhase(java.security.Key,%20kotlin.Boolean))`(`key:` ` [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#)!`, `lastPhase:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Executes the next phase of this key agreement with the given key that was received from one of the other parties involved in this key agreement. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [engineGenerateSecret](https://developer.android.com/reference/kotlin/javax/crypto/KeyAgreementSpi#engineGenerateSecret())`()` Generates the shared secret and returns it in a new buffer. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [engineGenerateSecret](https://developer.android.com/reference/kotlin/javax/crypto/KeyAgreementSpi#engineGenerateSecret(kotlin.ByteArray,%20kotlin.Int))`(`sharedSecret:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Generates the shared secret, and places it into the buffer`sharedSecret`, beginning at`offset`inclusive. |
| abstract [SecretKey](https://developer.android.com/reference/kotlin/javax/crypto/SecretKey)! | [engineGenerateSecret](https://developer.android.com/reference/kotlin/javax/crypto/KeyAgreementSpi#engineGenerateSecret(kotlin.String))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates the shared secret and returns it as a secret key object of the requested algorithm type. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInit](https://developer.android.com/reference/kotlin/javax/crypto/KeyAgreementSpi#engineInit(java.security.Key,%20java.security.SecureRandom))`(`key:` ` [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#)!`, `random:` ` [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom.html#)!`)` Initializes this key agreement with the given key and source of randomness. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInit](https://developer.android.com/reference/kotlin/javax/crypto/KeyAgreementSpi#engineInit(java.security.Key,%20java.security.spec.AlgorithmParameterSpec,%20java.security.SecureRandom))`(`key:` ` [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#)!`, `params:` ` [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#)!`, `random:` ` [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom.html#)!`)` Initializes this key agreement with the given key, set of algorithm parameters, and source of randomness. |

## Public constructors

### KeyAgreementSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyAgreementSpi()
```

## Protected methods

### engineDoPhase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineDoPhase(
    key: Key!, 
    lastPhase: Boolean
): Key!
```

Executes the next phase of this key agreement with the given key that was received from one of the other parties involved in this key agreement.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#)!:the key for this phase. For example, in the case of Diffie-Hellman between 2 parties, this would be the other party's Diffie-Hellman public key. |
| `lastPhase` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):flag which indicates whether or not this is the last phase of this key agreement. |

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#)! | the (intermediate) key resulting from this phase, or null if this phase does not yield a key |

| Exceptions ||
|-------------------------------------|---------------------------------------------------|
| `java.security.InvalidKeyException` | if the given key is inappropriate for this phase. |
| `java.lang.IllegalStateException` | if this key agreement has not been initialized. |

### engineGenerateSecret

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineGenerateSecret(): ByteArray!
```

Generates the shared secret and returns it in a new buffer.

This method resets this`KeyAgreementSpi`object, so that it can be reused for further key agreements. Unless this key agreement is reinitialized with one of the`engineInit`methods, the same private information and algorithm parameters will be used for subsequent key agreements.

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the new buffer with the shared secret |

| Exceptions ||
|-----------------------------------|--------------------------------------------------|
| `java.lang.IllegalStateException` | if this key agreement has not been completed yet |

### engineGenerateSecret

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineGenerateSecret(
    sharedSecret: ByteArray!, 
    offset: Int
): Int
```

Generates the shared secret, and places it into the buffer`sharedSecret`, beginning at`offset`inclusive.

If the`sharedSecret`buffer is too small to hold the result, a`ShortBufferException`is thrown. In this case, this call should be repeated with a larger output buffer.

This method resets this`KeyAgreementSpi`object, so that it can be reused for further key agreements. Unless this key agreement is reinitialized with one of the`engineInit`methods, the same private information and algorithm parameters will be used for subsequent key agreements.

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

### engineGenerateSecret

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineGenerateSecret(algorithm: String!): SecretKey!
```

Creates the shared secret and returns it as a secret key object of the requested algorithm type.

This method resets this`KeyAgreementSpi`object, so that it can be reused for further key agreements. Unless this key agreement is reinitialized with one of the`engineInit`methods, the same private information and algorithm parameters will be used for subsequent key agreements.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the requested secret key algorithm |

| Return ||
|-------------------------------------------------------------------------------------|-----------------------|
| [SecretKey](https://developer.android.com/reference/kotlin/javax/crypto/SecretKey)! | the shared secret key |

| Exceptions ||
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this key agreement has not been completed yet |
| `java.security.NoSuchAlgorithmException` | if the requested secret key algorithm is not available |
| `java.security.InvalidKeyException` | if the shared secret key material cannot be used to generate a secret key of the requested algorithm type (e.g., the key material is too short) |

### engineInit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineInit(
    key: Key!, 
    random: SecureRandom!
): Unit
```

Initializes this key agreement with the given key and source of randomness. The given key is required to contain all the algorithm parameters required for this key agreement.

If the key agreement algorithm requires random bytes, it gets them from the given source of randomness,`random`. However, if the underlying algorithm implementation does not require any random bytes,`random`is ignored.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#)!:the party's private information. For example, in the case of the Diffie-Hellman key agreement, this would be the party's own Diffie-Hellman private key. |
| `random` | [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom.html#)!:the source of randomness |

| Exceptions ||
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| `java.security.InvalidKeyException` | if the given key is inappropriate for this key agreement, e.g., is of the wrong type or has an incompatible algorithm type. |

### engineInit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineInit(
    key: Key!, 
    params: AlgorithmParameterSpec!, 
    random: SecureRandom!
): Unit
```

Initializes this key agreement with the given key, set of algorithm parameters, and source of randomness.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#)!:the party's private information. For example, in the case of the Diffie-Hellman key agreement, this would be the party's own Diffie-Hellman private key. |
| `params` | [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#)!:the key agreement parameters |
| `random` | [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom.html#)!:the source of randomness |

| Exceptions ||
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| `java.security.InvalidKeyException` | if the given key is inappropriate for this key agreement, e.g., is of the wrong type or has an incompatible algorithm type. |
| `java.security.InvalidAlgorithmParameterException` | if the given parameters are inappropriate for this key agreement. |
