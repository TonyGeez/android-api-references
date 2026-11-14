# KeyGeneratorSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyGeneratorSpi

```
abstract class KeyGeneratorSpi
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.crypto.KeyGeneratorSpi](../javax/crypto/KeyGeneratorSpi.md) |

This class defines the*Service Provider Interface* (**SPI** ) for the`KeyGenerator`class. All the abstract methods in this class must be implemented by each cryptographic service provider who wishes to supply the implementation of a key generator for a particular algorithm.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------|---|
| [KeyGeneratorSpi](../javax/crypto/KeyGeneratorSpi.md))`()` <br /> |

| Protected methods ||
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [SecretKey](../javax/crypto/SecretKey.md)! | [engineGenerateKey](../javax/crypto/KeyGeneratorSpi.md))`()` Generates a secret key. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInit](../javax/crypto/KeyGeneratorSpi.md))`(`keysize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `random:` ` [SecureRandom](../java/security/SecureRandom.md)!`)` Initializes this key generator for a certain keysize, using the given source of randomness. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInit](../javax/crypto/KeyGeneratorSpi.md))`(`random:` ` [SecureRandom](../java/security/SecureRandom.md)!`)` Initializes the key generator. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInit](../javax/crypto/KeyGeneratorSpi.md))`(`params:` ` [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md)!`, `random:` ` [SecureRandom](../java/security/SecureRandom.md)!`)` Initializes the key generator with the specified parameter set and a user-provided source of randomness. |

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
| [SecretKey](../javax/crypto/SecretKey.md)! | the new key |

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
| `random` | [SecureRandom](../java/security/SecureRandom.md)!:the source of randomness for this key generator |

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
| `random` | [SecureRandom](../java/security/SecureRandom.md)!:the source of randomness for this generator |

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
| `params` | [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md)!:the key generation parameters |
| `random` | [SecureRandom](../java/security/SecureRandom.md)!:the source of randomness for this key generator |

| Exceptions ||
|----------------------------------------------------|---------------------------------------------------|
| `java.security.InvalidAlgorithmParameterException` | if`params`is inappropriate for this key generator |
