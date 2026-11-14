# KeyPairGenerator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyPairGenerator

```
abstract class KeyPairGenerator : KeyPairGeneratorSpi
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.security.KeyPairGeneratorSpi](https://developer.android.com/reference/kotlin/java/security/KeyPairGeneratorSpi) ||
| | ↳ | [java.security.KeyPairGenerator](https://developer.android.com/reference/kotlin/java/security/KeyPairGenerator#) |

The KeyPairGenerator class is used to generate pairs of public and private keys. Key pair generators are constructed using the`getInstance`factory methods (static methods that return instances of a given class).

A Key pair generator for a particular algorithm creates a public/private key pair that can be used with this algorithm. It also associates algorithm-specific parameters with each of the generated keys.

There are two ways to generate a key pair: in an algorithm-independent manner, and in an algorithm-specific manner. The only difference between the two is the initialization of the object:

- **Algorithm-Independent Initialization**

 All key pair generators share the concepts of a keysize and a source of randomness. The keysize is interpreted differently for different algorithms (e.g., in the case of the*DSA* algorithm, the keysize corresponds to the length of the modulus). There is an [initialize](https://developer.android.com/reference/kotlin/java/security/KeyPairGenerator#initialize(kotlin.Int,%20java.security.SecureRandom))method in this KeyPairGenerator class that takes these two universally shared types of arguments. There is also one that takes just a`keysize`argument, and uses the`SecureRandom`implementation of the highest-priority installed provider as the source of randomness. (If none of the installed providers supply an implementation of`SecureRandom`, a system-provided source of randomness is used.)

 Since no other parameters are specified when you call the above algorithm-independent`initialize`methods, it is up to the provider what to do about the algorithm-specific parameters (if any) to be associated with each of the keys.

 If the algorithm is the*DSA* algorithm, and the keysize (modulus size) is 512, 768, 1024, or 2048, then the*Sun* provider uses a set of precomputed values for the`p`,`q`, and`g`parameters. If the modulus size is not one of the above values, the*Sun*provider creates a new set of parameters. Other providers might have precomputed parameter sets for more than just the modulus sizes mentioned above. Still others might not have a list of precomputed parameters at all and instead always create new parameter sets.
- **Algorithm-Specific Initialization**

 For situations where a set of algorithm-specific parameters already exists (e.g., so-called*community parameters* in DSA), there are two [initialize](https://developer.android.com/reference/kotlin/java/security/KeyPairGenerator#initialize(java.security.spec.AlgorithmParameterSpec))methods that have an`AlgorithmParameterSpec`argument. One also has a`SecureRandom`argument, while the other uses the`SecureRandom`implementation of the highest-priority installed provider as the source of randomness. (If none of the installed providers supply an implementation of`SecureRandom`, a system-provided source of randomness is used.)

In case the client does not explicitly initialize the KeyPairGenerator (via a call to an`initialize`method), each provider must supply (and document) a default initialization. For example, the*Sun*provider uses a default modulus size (keysize) of 1024 bits.

Note that this class is abstract and extends from`KeyPairGeneratorSpi`for historical reasons. Application developers should only take notice of the methods defined in this`KeyPairGenerator`class; all the methods in the superclass are intended for cryptographic service providers who wish to supply their own implementations of key pair generators.

Android provides the following`KeyPairGenerator`algorithms:

| Algorithm | Supported API Levels |
|-----------|----------------------|
| DH | 1+ |
| DSA | 1+ |
| EC | 11+ |
| --- | --- |
| RSA | 1+ |
| XDH | 33+ |

These algorithms are described in the [KeyPairGenerator section](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#keypairgenerator-algorithms) of the Java Cryptography Architecture Standard Algorithm Name Documentation.

## Summary

| Protected constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [KeyPairGenerator](https://developer.android.com/reference/kotlin/java/security/KeyPairGenerator#KeyPairGenerator(kotlin.String))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a KeyPairGenerator object for the specified algorithm. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [KeyPair](https://developer.android.com/reference/kotlin/java/security/KeyPair)! | [genKeyPair](https://developer.android.com/reference/kotlin/java/security/KeyPairGenerator#genKeyPair())`()` Generates a key pair. |
| open [KeyPair](https://developer.android.com/reference/kotlin/java/security/KeyPair)! | [generateKeyPair](https://developer.android.com/reference/kotlin/java/security/KeyPairGenerator#generateKeyPair())`()` Generates a key pair. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAlgorithm](https://developer.android.com/reference/kotlin/java/security/KeyPairGenerator#getAlgorithm())`()` Returns the standard name of the algorithm for this key pair generator. |
| --- | --- |
| openstatic [KeyPairGenerator](https://developer.android.com/reference/kotlin/java/security/KeyPairGenerator#)! | [getInstance](https://developer.android.com/reference/kotlin/java/security/KeyPairGenerator#getInstance(kotlin.String))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a KeyPairGenerator object that generates public/private key pairs for the specified algorithm. |
| openstatic [KeyPairGenerator](https://developer.android.com/reference/kotlin/java/security/KeyPairGenerator#)! | [getInstance](https://developer.android.com/reference/kotlin/java/security/KeyPairGenerator#getInstance(kotlin.String,%20kotlin.String))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a KeyPairGenerator object that generates public/private key pairs for the specified algorithm. |
| openstatic [KeyPairGenerator](https://developer.android.com/reference/kotlin/java/security/KeyPairGenerator#)! | [getInstance](https://developer.android.com/reference/kotlin/java/security/KeyPairGenerator#getInstance(kotlin.String,%20java.security.Provider))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `provider:` ` [Provider](https://developer.android.com/reference/kotlin/java/security/Provider)!`)` Returns a KeyPairGenerator object that generates public/private key pairs for the specified algorithm. |
| --- | --- |
| [Provider](https://developer.android.com/reference/kotlin/java/security/Provider)! | [getProvider](https://developer.android.com/reference/kotlin/java/security/KeyPairGenerator#getProvider())`()` Returns the provider of this key pair generator object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [initialize](https://developer.android.com/reference/kotlin/java/security/KeyPairGenerator#initialize(kotlin.Int))`(`keysize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Initializes the key pair generator for a certain keysize using a default parameter set and the`SecureRandom`implementation of the highest-priority installed provider as the source of randomness. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [initialize](https://developer.android.com/reference/kotlin/java/security/KeyPairGenerator#initialize(kotlin.Int,%20java.security.SecureRandom))`(`keysize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `random:` ` [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom)!`)` Initializes the key pair generator for a certain keysize with the given source of randomness (and a default parameter set). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [initialize](https://developer.android.com/reference/kotlin/java/security/KeyPairGenerator#initialize(java.security.spec.AlgorithmParameterSpec))`(`params:` ` [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec)!`)` Initializes the key pair generator using the specified parameter set and the`SecureRandom`implementation of the highest-priority installed provider as the source of randomness. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [initialize](https://developer.android.com/reference/kotlin/java/security/KeyPairGenerator#initialize(java.security.spec.AlgorithmParameterSpec,%20java.security.SecureRandom))`(`params:` ` [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec)!`, `random:` ` [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom)!`)` Initializes the key pair generator with the given parameter set and source of randomness. |

## Protected constructors

### KeyPairGenerator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected KeyPairGenerator(algorithm: String!)
```

Creates a KeyPairGenerator object for the specified algorithm.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the standard string name of the algorithm. See the KeyPairGenerator section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#keypairgenerator-algorithms) for information about standard algorithm names. |

## Public methods

### genKeyPair

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun genKeyPair(): KeyPair!
```

Generates a key pair.

If this KeyPairGenerator has not been initialized explicitly, provider-specific defaults will be used for the size and other (algorithm-specific) values of the generated keys.

This will generate a new key pair every time it is called.

This method is functionally equivalent to [generateKeyPair](https://developer.android.com/reference/kotlin/java/security/KeyPairGenerator#generateKeyPair()).

| Return ||
|----------------------------------------------------------------------------------|------------------------|
| [KeyPair](https://developer.android.com/reference/kotlin/java/security/KeyPair)! | the generated key pair |

### generateKeyPair

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun generateKeyPair(): KeyPair!
```

Generates a key pair.

If this KeyPairGenerator has not been initialized explicitly, provider-specific defaults will be used for the size and other (algorithm-specific) values of the generated keys.

This will generate a new key pair every time it is called.

This method is functionally equivalent to [genKeyPair](https://developer.android.com/reference/kotlin/java/security/KeyPairGenerator#genKeyPair()).

| Return ||
|----------------------------------------------------------------------------------|------------------------|
| [KeyPair](https://developer.android.com/reference/kotlin/java/security/KeyPair)! | the generated key pair |

### getAlgorithm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAlgorithm(): String!
```

Returns the standard name of the algorithm for this key pair generator. See the KeyPairGenerator section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#keypairgenerator-algorithms) for information about standard algorithm names.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the standard string name of the algorithm. |

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(algorithm: String!): KeyPairGenerator!
```

Returns a KeyPairGenerator object that generates public/private key pairs for the specified algorithm.

This method traverses the list of registered security Providers, starting with the most preferred Provider. A new KeyPairGenerator object encapsulating the KeyPairGeneratorSpi implementation from the first Provider that supports the specified algorithm is returned.

Note that the list of registered providers may be retrieved via the [Security.getProviders()](https://developer.android.com/reference/kotlin/java/security/Security#getProviders())method.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the standard string name of the algorithm. See the KeyPairGenerator section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#keypairgenerator-algorithms) for information about standard algorithm names. |

| Return ||
|-----------------------------------------------------------------------------------------------------|---------------------------------|
| [KeyPairGenerator](https://developer.android.com/reference/kotlin/java/security/KeyPairGenerator#)! | the new`KeyPairGenerator`object |

| Exceptions ||
|------------------------------------------|------------------------------------------------------------------------------------------|
| `java.security.NoSuchAlgorithmException` | if no`Provider`supports a`KeyPairGeneratorSpi`implementation for the specified algorithm |
| `java.lang.NullPointerException` | if`algorithm`is`null` |

**See Also**

- [java.security.Provider](https://developer.android.com/reference/kotlin/java/security/Provider) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    algorithm: String!, 
    provider: String!
): KeyPairGenerator!
```

Returns a KeyPairGenerator object that generates public/private key pairs for the specified algorithm.

A new KeyPairGenerator object encapsulating the KeyPairGeneratorSpi implementation from the specified provider is returned. The specified provider must be registered in the security provider list.

Note that the list of registered providers may be retrieved via the [Security.getProviders()](https://developer.android.com/reference/kotlin/java/security/Security#getProviders())method.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the standard string name of the algorithm. See the KeyPairGenerator section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#keypairgenerator-algorithms) for information about standard algorithm names. |
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the string name of the provider. |

| Return ||
|-----------------------------------------------------------------------------------------------------|---------------------------------|
| [KeyPairGenerator](https://developer.android.com/reference/kotlin/java/security/KeyPairGenerator#)! | the new`KeyPairGenerator`object |

| Exceptions ||
|------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the provider name is`null`or empty |
| `java.security.NoSuchAlgorithmException` | if a`KeyPairGeneratorSpi`implementation for the specified algorithm is not available from the specified provider |
| `java.security.NoSuchProviderException` | if the specified provider is not registered in the security provider list |
| --- | --- |
| `java.lang.NullPointerException` | if`algorithm`is`null` |

**See Also**

- [java.security.Provider](https://developer.android.com/reference/kotlin/java/security/Provider) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    algorithm: String!, 
    provider: Provider!
): KeyPairGenerator!
```

Returns a KeyPairGenerator object that generates public/private key pairs for the specified algorithm.

A new KeyPairGenerator object encapsulating the KeyPairGeneratorSpi implementation from the specified Provider object is returned. Note that the specified Provider object does not have to be registered in the provider list.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the standard string name of the algorithm. See the KeyPairGenerator section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#keypairgenerator-algorithms) for information about standard algorithm names. |
| `provider` | [Provider](https://developer.android.com/reference/kotlin/java/security/Provider)!:the provider. |

| Return ||
|-----------------------------------------------------------------------------------------------------|---------------------------------|
| [KeyPairGenerator](https://developer.android.com/reference/kotlin/java/security/KeyPairGenerator#)! | the new`KeyPairGenerator`object |

| Exceptions ||
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the specified provider is`null` |
| `java.security.NoSuchAlgorithmException` | if a`KeyPairGeneratorSpi`implementation for the specified algorithm is not available from the specified`Provider`object |
| `java.lang.NullPointerException` | if`algorithm`is`null` |
| --- | --- |

**See Also**

- [java.security.Provider](https://developer.android.com/reference/kotlin/java/security/Provider) 

### getProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getProvider(): Provider!
```

Returns the provider of this key pair generator object.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------|
| [Provider](https://developer.android.com/reference/kotlin/java/security/Provider)! | the provider of this key pair generator object |

### initialize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun initialize(keysize: Int): Unit
```

Initializes the key pair generator for a certain keysize using a default parameter set and the`SecureRandom`implementation of the highest-priority installed provider as the source of randomness. (If none of the installed providers supply an implementation of`SecureRandom`, a system-provided source of randomness is used.)

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `keysize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the keysize. This is an algorithm-specific metric, such as modulus length, specified in number of bits. |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------|
| `java.security.InvalidParameterException` | if the`keysize`is not supported by this KeyPairGenerator object. |

### initialize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun initialize(
    keysize: Int, 
    random: SecureRandom!
): Unit
```

Initializes the key pair generator for a certain keysize with the given source of randomness (and a default parameter set).

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `keysize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the keysize. This is an algorithm-specific metric, such as modulus length, specified in number of bits. |
| `random` | [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom)!:the source of randomness. |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------|
| `java.security.InvalidParameterException` | if the`keysize`is not supported by this KeyPairGenerator object. |

### initialize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun initialize(params: AlgorithmParameterSpec!): Unit
```

Initializes the key pair generator using the specified parameter set and the`SecureRandom`implementation of the highest-priority installed provider as the source of randomness. (If none of the installed providers supply an implementation of`SecureRandom`, a system-provided source of randomness is used.)

This concrete method has been added to this previously-defined abstract class. This method calls the KeyPairGeneratorSpi [initialize](https://developer.android.com/reference/kotlin/java/security/KeyPairGeneratorSpi#initialize(java.security.spec.AlgorithmParameterSpec,%20java.security.SecureRandom))method, passing it`params`and a source of randomness (obtained from the highest-priority installed provider or system-provided if none of the installed providers supply one). That`initialize`method always throws an UnsupportedOperationException if it is not overridden by the provider.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `params` | [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec)!:the parameter set used to generate the keys. |

| Exceptions ||
|----------------------------------------------------|------------------------------------------------------------------------|
| `java.security.InvalidAlgorithmParameterException` | if the given parameters are inappropriate for this key pair generator. |

### initialize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun initialize(
    params: AlgorithmParameterSpec!, 
    random: SecureRandom!
): Unit
```

Initializes the key pair generator with the given parameter set and source of randomness.

This concrete method has been added to this previously-defined abstract class. This method calls the KeyPairGeneratorSpi [initialize](https://developer.android.com/reference/kotlin/java/security/KeyPairGeneratorSpi#initialize(java.security.spec.AlgorithmParameterSpec,%20java.security.SecureRandom))method, passing it`params`and`random`. That`initialize`method always throws an UnsupportedOperationException if it is not overridden by the provider.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `params` | [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec)!:the parameter set used to generate the keys. |
| `random` | [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom)!:the source of randomness. |

| Exceptions ||
|----------------------------------------------------|------------------------------------------------------------------------|
| `java.security.InvalidAlgorithmParameterException` | if the given parameters are inappropriate for this key pair generator. |
