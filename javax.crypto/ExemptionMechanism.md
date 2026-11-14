# ExemptionMechanism

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ExemptionMechanism

```
open class ExemptionMechanism
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.crypto.ExemptionMechanism](ExemptionMechanism.md) |

This class provides the functionality of an exemption mechanism, examples of which are*key recovery* ,*key weakening* , and*key escrow*.

Applications or applets that use an exemption mechanism may be granted stronger encryption capabilities than those which don't.

## Summary

| Protected constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ExemptionMechanism](ExemptionMechanism.md))`(`exmechSpi:` ` [ExemptionMechanismSpi](ExemptionMechanismSpi.md)!`, `provider:` ` [Provider](../java.security/Provider.md)!`, `mechanism:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a ExemptionMechanism object. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [genExemptionBlob](ExemptionMechanism.md))`()` Generates the exemption mechanism key blob. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [genExemptionBlob](ExemptionMechanism.md))`(`output:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Generates the exemption mechanism key blob, and stores the result in the`output`buffer. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [genExemptionBlob](ExemptionMechanism.md))`(`output:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `outputOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Generates the exemption mechanism key blob, and stores the result in the`output`buffer, starting at`outputOffset`inclusive. |
| --- | --- |
| static [ExemptionMechanism](ExemptionMechanism.md)! | [getInstance](ExemptionMechanism.md))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns an`ExemptionMechanism`object that implements the specified exemption mechanism algorithm. |
| static [ExemptionMechanism](ExemptionMechanism.md)! | [getInstance](ExemptionMechanism.md))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns an`ExemptionMechanism`object that implements the specified exemption mechanism algorithm. |
| static [ExemptionMechanism](ExemptionMechanism.md)! | [getInstance](ExemptionMechanism.md))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `provider:` ` [Provider](../java.security/Provider.md)!`)` Returns an`ExemptionMechanism`object that implements the specified exemption mechanism algorithm. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](ExemptionMechanism.md))`()` Returns the exemption mechanism name of this`ExemptionMechanism`object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOutputSize](ExemptionMechanism.md))`(`inputLen:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the length in bytes that an output buffer would need to be in order to hold the result of the next [genExemptionBlob](ExemptionMechanism.md))operation, given the input length`inputLen`(in bytes). |
| [Provider](../java.security/Provider.md)! | [getProvider](ExemptionMechanism.md))`()` Returns the provider of this`ExemptionMechanism`object. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](ExemptionMechanism.md))`(`key:` ` [Key](../java.security/Key.md)!`)` Initializes this exemption mechanism with a key. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](ExemptionMechanism.md))`(`key:` ` [Key](../java.security/Key.md)!`, `params:` ` [AlgorithmParameters](../java.security/AlgorithmParameters.md)!`)` Initializes this exemption mechanism with a key and a set of algorithm parameters. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](ExemptionMechanism.md))`(`key:` ` [Key](../java.security/Key.md)!`, `params:` ` [AlgorithmParameterSpec](../java.security.spec/AlgorithmParameterSpec.md)!`)` Initializes this exemption mechanism with a key and a set of algorithm parameters. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCryptoAllowed](ExemptionMechanism.md))`(`key:` ` [Key](../java.security/Key.md)!`)` Returns whether the result blob has been generated successfully by this exemption mechanism. |

## Protected constructors

### ExemptionMechanism

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected ExemptionMechanism(
    exmechSpi: ExemptionMechanismSpi!, 
    provider: Provider!, 
    mechanism: String!)
```

Creates a ExemptionMechanism object.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------|
| `exmechSpi` | [ExemptionMechanismSpi](ExemptionMechanismSpi.md)!:the delegate |
| `provider` | [Provider](../java.security/Provider.md)!:the provider |
| `mechanism` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the exemption mechanism |
| --- | --- |

## Public methods

### genExemptionBlob

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun genExemptionBlob(): ByteArray!
```

Generates the exemption mechanism key blob.

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the new buffer with the result key blob. |

| Exceptions ||
|--------------------------------------------|-----------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this exemption mechanism is in a wrong state (e.g., has not been initialized). |
| `javax.crypto.ExemptionMechanismException` | if problem(s) encountered in the process of generating. |

### genExemptionBlob

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun genExemptionBlob(output: ByteArray!): Int
```

Generates the exemption mechanism key blob, and stores the result in the`output`buffer.

If the`output`buffer is too small to hold the result, a`ShortBufferException`is thrown. In this case, repeat this call with a larger output buffer. Use [getOutputSize](ExemptionMechanism.md))to determine how big the output buffer should be.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------|
| `output` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer for the result |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of bytes stored in`output` |

| Exceptions ||
|--------------------------------------------|-----------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this exemption mechanism is in a wrong state (e.g., has not been initialized). |
| `javax.crypto.ShortBufferException` | if the given output buffer is too small to hold the result. |
| `javax.crypto.ExemptionMechanismException` | if problem(s) encountered in the process of generating. |
| --- | --- |

### genExemptionBlob

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun genExemptionBlob(
    output: ByteArray!, 
    outputOffset: Int
): Int
```

Generates the exemption mechanism key blob, and stores the result in the`output`buffer, starting at`outputOffset`inclusive.

If the`output`buffer is too small to hold the result, a`ShortBufferException`is thrown. In this case, repeat this call with a larger output buffer. Use [getOutputSize](ExemptionMechanism.md))to determine how big the output buffer should be.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------|
| `output` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer for the result |
| `outputOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset in`output`where the result is stored |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of bytes stored in`output` |

| Exceptions ||
|--------------------------------------------|-----------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this exemption mechanism is in a wrong state (e.g., has not been initialized). |
| `javax.crypto.ShortBufferException` | if the given output buffer is too small to hold the result. |
| `javax.crypto.ExemptionMechanismException` | if problem(s) encountered in the process of generating. |
| --- | --- |

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(algorithm: String!): ExemptionMechanism!
```

Returns an`ExemptionMechanism`object that implements the specified exemption mechanism algorithm.

This method traverses the list of registered security Providers, starting with the most preferred Provider. A new ExemptionMechanism object encapsulating the ExemptionMechanismSpi implementation from the first Provider that supports the specified algorithm is returned.

Note that the list of registered providers may be retrieved via the [Security.getProviders()](../java.security/Security.md))method.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the standard name of the requested exemption mechanism. See the ExemptionMechanism section in the [Java Cryptography Architecture Standard Algorithm Name Documentation](https://docs.oracle.com/javase/8/docs/technotes/guides/security/StandardNames.html#Exemption) for information about standard exemption mechanism names. |

| Return ||
|--------------------------------------------------------------------------------------------------------|------------------------------------|
| [ExemptionMechanism](ExemptionMechanism.md)! | the new`ExemptionMechanism`object. |

| Exceptions ||
|------------------------------------------|----------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`algorithm`is null. |
| `java.security.NoSuchAlgorithmException` | if no Provider supports an ExemptionMechanismSpi implementation for the specified algorithm. |

**See Also**

- [java.security.Provider](../java.security/Provider.md) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(
    algorithm: String!, 
    provider: String!
): ExemptionMechanism!
```

Returns an`ExemptionMechanism`object that implements the specified exemption mechanism algorithm.

A new ExemptionMechanism object encapsulating the ExemptionMechanismSpi implementation from the specified provider is returned. The specified provider must be registered in the security provider list.

Note that the list of registered providers may be retrieved via the [Security.getProviders()](../java.security/Security.md))method.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the standard name of the requested exemption mechanism. See the ExemptionMechanism section in the [Java Cryptography Architecture Standard Algorithm Name Documentation](https://docs.oracle.com/javase/8/docs/technotes/guides/security/StandardNames.html#Exemption) for information about standard exemption mechanism names. |
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the provider. |

| Return ||
|--------------------------------------------------------------------------------------------------------|------------------------------------|
| [ExemptionMechanism](ExemptionMechanism.md)! | the new`ExemptionMechanism`object. |

| Exceptions ||
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`algorithm`is null. |
| `java.security.NoSuchAlgorithmException` | if an ExemptionMechanismSpi implementation for the specified algorithm is not available from the specified provider. |
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
): ExemptionMechanism!
```

Returns an`ExemptionMechanism`object that implements the specified exemption mechanism algorithm.

A new ExemptionMechanism object encapsulating the ExemptionMechanismSpi implementation from the specified Provider object is returned. Note that the specified Provider object does not have to be registered in the provider list.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the standard name of the requested exemption mechanism. See the ExemptionMechanism section in the [Java Cryptography Architecture Standard Algorithm Name Documentation](https://docs.oracle.com/javase/8/docs/technotes/guides/security/StandardNames.html#Exemption) for information about standard exemption mechanism names. |
| `provider` | [Provider](../java.security/Provider.md)!:the provider. |

| Return ||
|--------------------------------------------------------------------------------------------------------|------------------------------------|
| [ExemptionMechanism](ExemptionMechanism.md)! | the new`ExemptionMechanism`object. |

| Exceptions ||
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`algorithm`is null. |
| `java.security.NoSuchAlgorithmException` | if an ExemptionMechanismSpi implementation for the specified algorithm is not available from the specified Provider object. |
| `java.lang.IllegalArgumentException` | if the`provider`is null. |
| --- | --- |

**See Also**

- [java.security.Provider](../java.security/Provider.md) 

### getName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getName(): String!
```

Returns the exemption mechanism name of this`ExemptionMechanism`object.

This is the same name that was specified in one of the`getInstance`calls that created this`ExemptionMechanism`object.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the exemption mechanism name of this`ExemptionMechanism`object. |

### getOutputSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOutputSize(inputLen: Int): Int
```

Returns the length in bytes that an output buffer would need to be in order to hold the result of the next [genExemptionBlob](ExemptionMechanism.md))operation, given the input length`inputLen`(in bytes).

The actual output length of the next [genExemptionBlob](ExemptionMechanism.md))call may be smaller than the length returned by this method.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------|
| `inputLen` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the input length (in bytes) |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the required output buffer size (in bytes) |

| Exceptions ||
|-----------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this exemption mechanism is in a wrong state (e.g., has not yet been initialized) |

### getProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getProvider(): Provider!
```

Returns the provider of this`ExemptionMechanism`object.

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------|
| [Provider](../java.security/Provider.md)! | the provider of this`ExemptionMechanism`object. |

### init

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun init(key: Key!): Unit
```

Initializes this exemption mechanism with a key.

If this exemption mechanism requires any algorithm parameters that cannot be derived from the given`key`, the underlying exemption mechanism implementation is supposed to generate the required parameters itself (using provider-specific default values); in the case that algorithm parameters must be specified by the caller, an`InvalidKeyException`is raised.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------|
| `key` | [Key](../java.security/Key.md)!:the key for this exemption mechanism |

| Exceptions ||
|--------------------------------------------|-----------------------------------------------------------------|
| `java.security.InvalidKeyException` | if the given key is inappropriate for this exemption mechanism. |
| `javax.crypto.ExemptionMechanismException` | if problem(s) encountered in the process of initializing. |

### init

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun init(
    key: Key!, 
    params: AlgorithmParameters!
): Unit
```

Initializes this exemption mechanism with a key and a set of algorithm parameters.

If this exemption mechanism requires any algorithm parameters and`params`is null, the underlying exemption mechanism implementation is supposed to generate the required parameters itself (using provider-specific default values); in the case that algorithm parameters must be specified by the caller, an`InvalidAlgorithmParameterException`is raised.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [Key](../java.security/Key.md)!:the key for this exemption mechanism |
| `params` | [AlgorithmParameters](../java.security/AlgorithmParameters.md)!:the algorithm parameters |

| Exceptions ||
|----------------------------------------------------|-----------------------------------------------------------------------------------|
| `java.security.InvalidKeyException` | if the given key is inappropriate for this exemption mechanism. |
| `java.security.InvalidAlgorithmParameterException` | if the given algorithm parameters are inappropriate for this exemption mechanism. |
| `javax.crypto.ExemptionMechanismException` | if problem(s) encountered in the process of initializing. |
| --- | --- |

### init

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun init(
    key: Key!, 
    params: AlgorithmParameterSpec!
): Unit
```

Initializes this exemption mechanism with a key and a set of algorithm parameters.

If this exemption mechanism requires any algorithm parameters and`params`is null, the underlying exemption mechanism implementation is supposed to generate the required parameters itself (using provider-specific default values); in the case that algorithm parameters must be specified by the caller, an`InvalidAlgorithmParameterException`is raised.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [Key](../java.security/Key.md)!:the key for this exemption mechanism |
| `params` | [AlgorithmParameterSpec](../java.security.spec/AlgorithmParameterSpec.md)!:the algorithm parameters |

| Exceptions ||
|----------------------------------------------------|-----------------------------------------------------------------------------------|
| `java.security.InvalidKeyException` | if the given key is inappropriate for this exemption mechanism. |
| `java.security.InvalidAlgorithmParameterException` | if the given algorithm parameters are inappropriate for this exemption mechanism. |
| `javax.crypto.ExemptionMechanismException` | if problem(s) encountered in the process of initializing. |
| --- | --- |

### isCryptoAllowed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isCryptoAllowed(key: Key!): Boolean
```

Returns whether the result blob has been generated successfully by this exemption mechanism.

The method also makes sure that the key passed in is the same as the one this exemption mechanism used in initializing and generating phases.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------|
| `key` | [Key](../java.security/Key.md)!:the key the crypto is going to use. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the result blob of the same key has been generated successfully by this exemption mechanism; false if`key`is null. |

| Exceptions ||
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `javax.crypto.ExemptionMechanismException` | if problem(s) encountered while determining whether the result blob has been generated successfully by this exemption mechanism object. |
