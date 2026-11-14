# AlgorithmParameterGeneratorSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AlgorithmParameterGeneratorSpi

```
abstract class AlgorithmParameterGeneratorSpi
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.AlgorithmParameterGeneratorSpi](AlgorithmParameterGeneratorSpi.md) |

This class defines the*Service Provider Interface* (**SPI** ) for the`AlgorithmParameterGenerator`class, which is used to generate a set of parameters to be used with a certain algorithm.

All the abstract methods in this class must be implemented by each cryptographic service provider who wishes to supply the implementation of a parameter generator for a particular algorithm.

In case the client does not explicitly initialize the AlgorithmParameterGenerator (via a call to an`engineInit`method), each provider must supply (and document) a default initialization. However, note that defaults may vary across different providers. Additionally, the default value for a provider may change in a future version. Therefore, it is recommended to explicitly initialize the AlgorithmParameterGenerator instead of relying on provider-specific defaults.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AlgorithmParameterGeneratorSpi](AlgorithmParameterGeneratorSpi.md))`()` <br /> |

| Protected methods ||
|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [AlgorithmParameters](AlgorithmParameters.md)! | [engineGenerateParameters](AlgorithmParameterGeneratorSpi.md))`()` Generates the parameters. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInit](AlgorithmParameterGeneratorSpi.md))`(`size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `random:` ` [SecureRandom](SecureRandom.md)!`)` Initializes this parameter generator for a certain size and source of randomness. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInit](AlgorithmParameterGeneratorSpi.md))`(`genParamSpec:` ` [AlgorithmParameterSpec](../java.security.spec/AlgorithmParameterSpec.md)!`, `random:` ` [SecureRandom](SecureRandom.md)!`)` Initializes this parameter generator with a set of algorithm-specific parameter generation values. |
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
| [AlgorithmParameters](AlgorithmParameters.md)! | the new AlgorithmParameters object. |

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
| `random` | [SecureRandom](SecureRandom.md)!:the source of randomness. |

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
| `genParamSpec` | [AlgorithmParameterSpec](../java.security.spec/AlgorithmParameterSpec.md)!:the set of algorithm-specific parameter generation values. |
| `random` | [SecureRandom](SecureRandom.md)!:the source of randomness. |

| Exceptions ||
|----------------------------------------------------|------------------------------------------------------------------------------------------|
| `java.security.InvalidAlgorithmParameterException` | if the given parameter generation values are inappropriate for this parameter generator. |
