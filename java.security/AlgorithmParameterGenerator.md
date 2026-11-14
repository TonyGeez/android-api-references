# AlgorithmParameterGenerator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AlgorithmParameterGenerator

```
open class AlgorithmParameterGenerator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.AlgorithmParameterGenerator](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameterGenerator#) |

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
| [AlgorithmParameterGenerator](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameterGenerator#AlgorithmParameterGenerator(java.security.AlgorithmParameterGeneratorSpi,%20java.security.Provider,%20kotlin.String))`(`paramGenSpi:` ` [AlgorithmParameterGeneratorSpi](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameterGeneratorSpi)!`, `provider:` ` [Provider](https://developer.android.com/reference/kotlin/java/security/Provider)!`, `algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates an AlgorithmParameterGenerator object. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AlgorithmParameters](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameters)! | [generateParameters](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameterGenerator#generateParameters())`()` Generates the parameters. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAlgorithm](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameterGenerator#getAlgorithm())`()` Returns the standard name of the algorithm this parameter generator is associated with. |
| openstatic [AlgorithmParameterGenerator](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameterGenerator#)! | [getInstance](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameterGenerator#getInstance(kotlin.String))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns an AlgorithmParameterGenerator object for generating a set of parameters to be used with the specified algorithm. |
| --- | --- |
| openstatic [AlgorithmParameterGenerator](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameterGenerator#)! | [getInstance](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameterGenerator#getInstance(kotlin.String,%20kotlin.String))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns an AlgorithmParameterGenerator object for generating a set of parameters to be used with the specified algorithm. |
| openstatic [AlgorithmParameterGenerator](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameterGenerator#)! | [getInstance](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameterGenerator#getInstance(kotlin.String,%20java.security.Provider))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `provider:` ` [Provider](https://developer.android.com/reference/kotlin/java/security/Provider)!`)` Returns an AlgorithmParameterGenerator object for generating a set of parameters to be used with the specified algorithm. |
| [Provider](https://developer.android.com/reference/kotlin/java/security/Provider)! | [getProvider](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameterGenerator#getProvider())`()` Returns the provider of this algorithm parameter generator object. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameterGenerator#init(kotlin.Int))`(`size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Initializes this parameter generator for a certain size. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameterGenerator#init(kotlin.Int,%20java.security.SecureRandom))`(`size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `random:` ` [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom)!`)` Initializes this parameter generator for a certain size and source of randomness. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameterGenerator#init(java.security.spec.AlgorithmParameterSpec))`(`genParamSpec:` ` [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec)!`)` Initializes this parameter generator with a set of algorithm-specific parameter generation values. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameterGenerator#init(java.security.spec.AlgorithmParameterSpec,%20java.security.SecureRandom))`(`genParamSpec:` ` [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec)!`, `random:` ` [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom)!`)` Initializes this parameter generator with a set of algorithm-specific parameter generation values. |

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
| `paramGenSpi` | [AlgorithmParameterGeneratorSpi](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameterGeneratorSpi)!:the delegate |
| `provider` | [Provider](https://developer.android.com/reference/kotlin/java/security/Provider)!:the provider |
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
| [AlgorithmParameters](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameters)! | the new AlgorithmParameters object. |

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

Note that the list of registered providers may be retrieved via the [Security.getProviders()](https://developer.android.com/reference/kotlin/java/security/Security#getProviders())method.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the algorithm this parameter generator is associated with.cc |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [AlgorithmParameterGenerator](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameterGenerator#)! | the new`AlgorithmParameterGenerator`object |

| Exceptions ||
|------------------------------------------|------------------------------------------------------------------------------------------------------|
| `java.security.NoSuchAlgorithmException` | if no`Provider`supports an`AlgorithmParameterGeneratorSpi`implementation for the specified algorithm |
| `java.lang.NullPointerException` | if`algorithm`is`null`on Android 14 or above |

**See Also**

- [java.security.Provider](https://developer.android.com/reference/kotlin/java/security/Provider) 

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

Note that the list of registered providers may be retrieved via the [Security.getProviders()](https://developer.android.com/reference/kotlin/java/security/Security#getProviders())method.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the algorithm this parameter generator is associated with. |
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the string name of the Provider. |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [AlgorithmParameterGenerator](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameterGenerator#)! | the new`AlgorithmParameterGenerator`object |

| Exceptions ||
|------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the provider name is`null`or empty |
| `java.security.NoSuchAlgorithmException` | if an`AlgorithmParameterGeneratorSpi`implementation for the specified algorithm is not available from the specified provider |
| `java.security.NoSuchProviderException` | if the specified provider is not registered in the security provider list |
| --- | --- |
| `java.lang.NullPointerException` | if`algorithm`is`null`on Android 14 or above |

**See Also**

- [java.security.Provider](https://developer.android.com/reference/kotlin/java/security/Provider) 

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
| `provider` | [Provider](https://developer.android.com/reference/kotlin/java/security/Provider)!:the`Provider`object. |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [AlgorithmParameterGenerator](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameterGenerator#)! | the new`AlgorithmParameterGenerator`object |

| Exceptions ||
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the specified provider is`null` |
| `java.security.NoSuchAlgorithmException` | if an`AlgorithmParameterGeneratorSpi`implementation for the specified algorithm is not available from the specified`Provider`object |
| `java.lang.NullPointerException` | if`algorithm`is`null`on Android 14 or above |
| --- | --- |

**See Also**

- [java.security.Provider](https://developer.android.com/reference/kotlin/java/security/Provider) 

### getProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getProvider(): Provider!
```

Returns the provider of this algorithm parameter generator object.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Provider](https://developer.android.com/reference/kotlin/java/security/Provider)! | the provider of this algorithm parameter generator object |

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
| `random` | [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom)!:the source of randomness. |

### init

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun init(genParamSpec: AlgorithmParameterSpec!): Unit
```

Initializes this parameter generator with a set of algorithm-specific parameter generation values. To generate the parameters, the`SecureRandom`implementation of the highest-priority installed provider is used as the source of randomness. (If none of the installed providers supply an implementation of`SecureRandom`, a system-provided source of randomness is used.)

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `genParamSpec` | [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec)!:the set of algorithm-specific parameter generation values. |

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
| `genParamSpec` | [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec)!:the set of algorithm-specific parameter generation values. |
| `random` | [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom)!:the source of randomness. |

| Exceptions ||
|----------------------------------------------------|------------------------------------------------------------------------------------------|
| `java.security.InvalidAlgorithmParameterException` | if the given parameter generation values are inappropriate for this parameter generator. |
