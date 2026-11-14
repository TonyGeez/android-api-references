# AlgorithmParameterGenerator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AlgorithmParameterGenerator

```
open class AlgorithmParameterGenerator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.AlgorithmParameterGenerator](../java/security/AlgorithmParameterGenerator.md) |

The`AlgorithmParameterGenerator`class is used to generate a set of parameters to be used with a certain algorithm. Parameter generators are constructed using the`getInstance`factory methods (static methods that return instances of a given class).

The object that will generate the parameters can be initialized in two different ways: in an algorithm-independent manner, or in an algorithm-specific manner:

- The algorithm-independent approach uses the fact that all parameter generators share the concept of a "size" and a source of randomness. The measure of size is universally shared by all algorithm parameters, though it is interpreted differently for different algorithms. For example, in the case of parameters for the*DSA*algorithm, "size" corresponds to the size of the prime modulus (in bits). When using this approach, algorithm-specific parameter generation values - if any - default to some standard values, unless they can be derived from the specified size.
- The other approach initializes a parameter generator object using algorithm-specific semantics, which are represented by a set of algorithm-specific parameter generation values. To generate Diffie-Hellman system parameters, for example, the parameter generation values usually consist of the size of the prime modulus and the size of the random exponent, both specified in number of bits.

In case the client does not explicitly initialize the AlgorithmParameterGenerator (via a call to an`init`method), each provider must supply (and document) a default initialization. However, note that defaults may vary across different providers. Additionally, the default value for a provider may change in a future version. Therefore, it is recommended to explicitly initialize the AlgorithmParameterGenerator instead of relying on provider-specific defaults.

Android provides the following`AlgorithmParameterGenerator`algorithms:

| Algorithm | Supported API Levels |
|-----------|----------------------|
| AES | 1-8 |
| DES | 1-8 |
| DESede | 1-8 |
| --- | --- |
| DH | 1+ |
| DSA | 1+ |

## Summary

| Protected constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AlgorithmParameterGenerator](../java/security/AlgorithmParameterGenerator.md))`(`paramGenSpi:` ` [AlgorithmParameterGeneratorSpi](../java/security/AlgorithmParameterGeneratorSpi.md)!`, `provider:` ` [Provider](../java/security/Provider.md)!`, `algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates an AlgorithmParameterGenerator object. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AlgorithmParameters](../java/security/AlgorithmParameters.md)! | [generateParameters](../java/security/AlgorithmParameterGenerator.md))`()` Generates the parameters. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAlgorithm](../java/security/AlgorithmParameterGenerator.md))`()` Returns the standard name of the algorithm this parameter generator is associated with. |
| openstatic [AlgorithmParameterGenerator](../java/security/AlgorithmParameterGenerator.md)! | [getInstance](../java/security/AlgorithmParameterGenerator.md))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns an AlgorithmParameterGenerator object for generating a set of parameters to be used with the specified algorithm. |
| --- | --- |
| openstatic [AlgorithmParameterGenerator](../java/security/AlgorithmParameterGenerator.md)! | [getInstance](../java/security/AlgorithmParameterGenerator.md))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns an AlgorithmParameterGenerator object for generating a set of parameters to be used with the specified algorithm. |
| openstatic [AlgorithmParameterGenerator](../java/security/AlgorithmParameterGenerator.md)! | [getInstance](../java/security/AlgorithmParameterGenerator.md))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `provider:` ` [Provider](../java/security/Provider.md)!`)` Returns an AlgorithmParameterGenerator object for generating a set of parameters to be used with the specified algorithm. |
| [Provider](../java/security/Provider.md)! | [getProvider](../java/security/AlgorithmParameterGenerator.md))`()` Returns the provider of this algorithm parameter generator object. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](../java/security/AlgorithmParameterGenerator.md))`(`size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Initializes this parameter generator for a certain size. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](../java/security/AlgorithmParameterGenerator.md))`(`size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `random:` ` [SecureRandom](../java/security/SecureRandom.md)!`)` Initializes this parameter generator for a certain size and source of randomness. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](../java/security/AlgorithmParameterGenerator.md))`(`genParamSpec:` ` [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md)!`)` Initializes this parameter generator with a set of algorithm-specific parameter generation values. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](../java/security/AlgorithmParameterGenerator.md))`(`genParamSpec:` ` [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md)!`, `random:` ` [SecureRandom](../java/security/SecureRandom.md)!`)` Initializes this parameter generator with a set of algorithm-specific parameter generation values. |

## Protected constructors

### AlgorithmParameterGenerator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected AlgorithmParameterGenerator(
    paramGenSpi: AlgorithmParameterGeneratorSpi!, 
    provider: Provider!, 
    algorithm: String!)
```

Creates an AlgorithmParameterGenerator object.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `paramGenSpi` | [AlgorithmParameterGeneratorSpi](../java/security/AlgorithmParameterGeneratorSpi.md)!:the delegate |
| `provider` | [Provider](../java/security/Provider.md)!:the provider |
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the algorithm |
| --- | --- |

## Public methods

### generateParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun generateParameters(): AlgorithmParameters!
```

Generates the parameters.

| Return ||
|----------------------------------------------------------------------------------------------------------|-------------------------------------|
| [AlgorithmParameters](../java/security/AlgorithmParameters.md)! | the new AlgorithmParameters object. |

### getAlgorithm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAlgorithm(): String!
```

Returns the standard name of the algorithm this parameter generator is associated with.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the string name of the algorithm. |

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(algorithm: String!): AlgorithmParameterGenerator!
```

Returns an AlgorithmParameterGenerator object for generating a set of parameters to be used with the specified algorithm.

This method traverses the list of registered security Providers, starting with the most preferred Provider. A new AlgorithmParameterGenerator object encapsulating the AlgorithmParameterGeneratorSpi implementation from the first Provider that supports the specified algorithm is returned.

Note that the list of registered providers may be retrieved via the [Security.getProviders()](../java/security/Security.md))method.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the algorithm this parameter generator is associated with.cc |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [AlgorithmParameterGenerator](../java/security/AlgorithmParameterGenerator.md)! | the new`AlgorithmParameterGenerator`object |

| Exceptions ||
|------------------------------------------|------------------------------------------------------------------------------------------------------|
| `java.security.NoSuchAlgorithmException` | if no`Provider`supports an`AlgorithmParameterGeneratorSpi`implementation for the specified algorithm |
| `java.lang.NullPointerException` | if`algorithm`is`null`on Android 14 or above |

**See Also**

- [java.security.Provider](../java/security/Provider.md) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    algorithm: String!, 
    provider: String!
): AlgorithmParameterGenerator!
```

Returns an AlgorithmParameterGenerator object for generating a set of parameters to be used with the specified algorithm.

A new AlgorithmParameterGenerator object encapsulating the AlgorithmParameterGeneratorSpi implementation from the specified provider is returned. The specified provider must be registered in the security provider list.

Note that the list of registered providers may be retrieved via the [Security.getProviders()](../java/security/Security.md))method.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the algorithm this parameter generator is associated with. |
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the string name of the Provider. |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [AlgorithmParameterGenerator](../java/security/AlgorithmParameterGenerator.md)! | the new`AlgorithmParameterGenerator`object |

| Exceptions ||
|------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the provider name is`null`or empty |
| `java.security.NoSuchAlgorithmException` | if an`AlgorithmParameterGeneratorSpi`implementation for the specified algorithm is not available from the specified provider |
| `java.security.NoSuchProviderException` | if the specified provider is not registered in the security provider list |
| --- | --- |
| `java.lang.NullPointerException` | if`algorithm`is`null`on Android 14 or above |

**See Also**

- [java.security.Provider](../java/security/Provider.md) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    algorithm: String!, 
    provider: Provider!
): AlgorithmParameterGenerator!
```

Returns an AlgorithmParameterGenerator object for generating a set of parameters to be used with the specified algorithm.

A new AlgorithmParameterGenerator object encapsulating the AlgorithmParameterGeneratorSpi implementation from the specified Provider object is returned. Note that the specified Provider object does not have to be registered in the provider list.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the string name of the algorithm this parameter generator is associated with. |
| `provider` | [Provider](../java/security/Provider.md)!:the`Provider`object. |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [AlgorithmParameterGenerator](../java/security/AlgorithmParameterGenerator.md)! | the new`AlgorithmParameterGenerator`object |

| Exceptions ||
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the specified provider is`null` |
| `java.security.NoSuchAlgorithmException` | if an`AlgorithmParameterGeneratorSpi`implementation for the specified algorithm is not available from the specified`Provider`object |
| `java.lang.NullPointerException` | if`algorithm`is`null`on Android 14 or above |
| --- | --- |

**See Also**

- [java.security.Provider](../java/security/Provider.md) 

### getProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getProvider(): Provider!
```

Returns the provider of this algorithm parameter generator object.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Provider](../java/security/Provider.md)! | the provider of this algorithm parameter generator object |

### init

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun init(size: Int): Unit
```

Initializes this parameter generator for a certain size. To create the parameters, the`SecureRandom`implementation of the highest-priority installed provider is used as the source of randomness. (If none of the installed providers supply an implementation of`SecureRandom`, a system-provided source of randomness is used.)

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------|
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the size (number of bits). |

### init

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun init(
    size: Int, 
    random: SecureRandom!
): Unit
```

Initializes this parameter generator for a certain size and source of randomness.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------|
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the size (number of bits). |
| `random` | [SecureRandom](../java/security/SecureRandom.md)!:the source of randomness. |

### init

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun init(genParamSpec: AlgorithmParameterSpec!): Unit
```

Initializes this parameter generator with a set of algorithm-specific parameter generation values. To generate the parameters, the`SecureRandom`implementation of the highest-priority installed provider is used as the source of randomness. (If none of the installed providers supply an implementation of`SecureRandom`, a system-provided source of randomness is used.)

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `genParamSpec` | [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md)!:the set of algorithm-specific parameter generation values. |

| Exceptions ||
|----------------------------------------------------|------------------------------------------------------------------------------------------|
| `java.security.InvalidAlgorithmParameterException` | if the given parameter generation values are inappropriate for this parameter generator. |

### init

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun init(
    genParamSpec: AlgorithmParameterSpec!, 
    random: SecureRandom!
): Unit
```

Initializes this parameter generator with a set of algorithm-specific parameter generation values.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `genParamSpec` | [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md)!:the set of algorithm-specific parameter generation values. |
| `random` | [SecureRandom](../java/security/SecureRandom.md)!:the source of randomness. |

| Exceptions ||
|----------------------------------------------------|------------------------------------------------------------------------------------------|
| `java.security.InvalidAlgorithmParameterException` | if the given parameter generation values are inappropriate for this parameter generator. |
