# AlgorithmParameterGeneratorSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AlgorithmParameterGeneratorSpi

```
abstract class AlgorithmParameterGeneratorSpi
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.AlgorithmParameterGeneratorSpi](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameterGeneratorSpi#) |

This class defines the*Service Provider Interface* (**SPI** ) for the`AlgorithmParameterGenerator`class, which is used to generate a set of parameters to be used with a certain algorithm.

All the abstract methods in this class must be implemented by each cryptographic service provider who wishes to supply the implementation of a parameter generator for a particular algorithm.

In case the client does not explicitly initialize the AlgorithmParameterGenerator (via a call to an`engineInit`method), each provider must supply (and document) a default initialization. However, note that defaults may vary across different providers. Additionally, the default value for a provider may change in a future version. Therefore, it is recommended to explicitly initialize the AlgorithmParameterGenerator instead of relying on provider-specific defaults.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AlgorithmParameterGeneratorSpi](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameterGeneratorSpi#AlgorithmParameterGeneratorSpi())`()` <br /> |

| Protected methods ||
|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [AlgorithmParameters](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameters)! | [engineGenerateParameters](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameterGeneratorSpi#engineGenerateParameters())`()` Generates the parameters. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInit](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameterGeneratorSpi#engineInit(kotlin.Int,%20java.security.SecureRandom))`(`size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `random:` ` [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom)!`)` Initializes this parameter generator for a certain size and source of randomness. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInit](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameterGeneratorSpi#engineInit(java.security.spec.AlgorithmParameterSpec,%20java.security.SecureRandom))`(`genParamSpec:` ` [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec)!`, `random:` ` [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom)!`)` Initializes this parameter generator with a set of algorithm-specific parameter generation values. |
| --- | --- |

## Public constructors

### AlgorithmParameterGeneratorSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AlgorithmParameterGeneratorSpi()
```

## Protected methods

### engineGenerateParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineGenerateParameters(): AlgorithmParameters!
```

Generates the parameters.

| Return ||
|----------------------------------------------------------------------------------------------------------|-------------------------------------|
| [AlgorithmParameters](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameters)! | the new AlgorithmParameters object. |

### engineInit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineInit(
    size: Int, 
    random: SecureRandom!
): Unit
```

Initializes this parameter generator for a certain size and source of randomness.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------|
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the size (number of bits). |
| `random` | [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom)!:the source of randomness. |

### engineInit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineInit(
    genParamSpec: AlgorithmParameterSpec!, 
    random: SecureRandom!
): Unit
```

Initializes this parameter generator with a set of algorithm-specific parameter generation values.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `genParamSpec` | [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec)!:the set of algorithm-specific parameter generation values. |
| `random` | [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom)!:the source of randomness. |

| Exceptions ||
|----------------------------------------------------|------------------------------------------------------------------------------------------|
| `java.security.InvalidAlgorithmParameterException` | if the given parameter generation values are inappropriate for this parameter generator. |
