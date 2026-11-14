# KeyGeneratorSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyGeneratorSpi

```
abstract class KeyGeneratorSpi
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.crypto.KeyGeneratorSpi](https://developer.android.com/reference/kotlin/javax/crypto/KeyGeneratorSpi#) |

This class defines the*Service Provider Interface* (**SPI** ) for the`KeyGenerator`class. All the abstract methods in this class must be implemented by each cryptographic service provider who wishes to supply the implementation of a key generator for a particular algorithm.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------|---|
| [KeyGeneratorSpi](https://developer.android.com/reference/kotlin/javax/crypto/KeyGeneratorSpi#KeyGeneratorSpi())`()` <br /> |

| Protected methods ||
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [SecretKey](https://developer.android.com/reference/kotlin/javax/crypto/SecretKey)! | [engineGenerateKey](https://developer.android.com/reference/kotlin/javax/crypto/KeyGeneratorSpi#engineGenerateKey())`()` Generates a secret key. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInit](https://developer.android.com/reference/kotlin/javax/crypto/KeyGeneratorSpi#engineInit(kotlin.Int,%20java.security.SecureRandom))`(`keysize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `random:` ` [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom.html#)!`)` Initializes this key generator for a certain keysize, using the given source of randomness. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInit](https://developer.android.com/reference/kotlin/javax/crypto/KeyGeneratorSpi#engineInit(java.security.SecureRandom))`(`random:` ` [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom.html#)!`)` Initializes the key generator. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInit](https://developer.android.com/reference/kotlin/javax/crypto/KeyGeneratorSpi#engineInit(java.security.spec.AlgorithmParameterSpec,%20java.security.SecureRandom))`(`params:` ` [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#)!`, `random:` ` [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom.html#)!`)` Initializes the key generator with the specified parameter set and a user-provided source of randomness. |

## Public constructors

### KeyGeneratorSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyGeneratorSpi()
```

## Protected methods

### engineGenerateKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineGenerateKey(): SecretKey!
```

Generates a secret key.

| Return ||
|-------------------------------------------------------------------------------------|-------------|
| [SecretKey](https://developer.android.com/reference/kotlin/javax/crypto/SecretKey)! | the new key |

### engineInit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineInit(
    keysize: Int, 
    random: SecureRandom!
): Unit
```

Initializes this key generator for a certain keysize, using the given source of randomness.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `keysize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the keysize. This is an algorithm-specific metric, specified in number of bits. |
| `random` | [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom.html#)!:the source of randomness for this key generator |

| Exceptions ||
|-------------------------------------------|-------------------------------------------|
| `java.security.InvalidParameterException` | if the keysize is wrong or not supported. |

### engineInit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineInit(random: SecureRandom!): Unit
```

Initializes the key generator.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `random` | [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom.html#)!:the source of randomness for this generator |

### engineInit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineInit(
    params: AlgorithmParameterSpec!, 
    random: SecureRandom!
): Unit
```

Initializes the key generator with the specified parameter set and a user-provided source of randomness.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `params` | [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#)!:the key generation parameters |
| `random` | [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom.html#)!:the source of randomness for this key generator |

| Exceptions ||
|----------------------------------------------------|---------------------------------------------------|
| `java.security.InvalidAlgorithmParameterException` | if`params`is inappropriate for this key generator |
