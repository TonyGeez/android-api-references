# ExemptionMechanismSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ExemptionMechanismSpi

```
abstract class ExemptionMechanismSpi
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.crypto.ExemptionMechanismSpi](ExemptionMechanismSpi.md) |

This class defines the*Service Provider Interface* (**SPI** ) for the`ExemptionMechanism`class. All the abstract methods in this class must be implemented by each cryptographic service provider who wishes to supply the implementation of a particular exemption mechanism.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ExemptionMechanismSpi](ExemptionMechanismSpi.md))`()` <br /> |

| Protected methods ||
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [engineGenExemptionBlob](ExemptionMechanismSpi.md))`()` Generates the exemption mechanism key blob. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [engineGenExemptionBlob](ExemptionMechanismSpi.md))`(`output:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `outputOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Generates the exemption mechanism key blob, and stores the result in the`output`buffer, starting at`outputOffset`inclusive. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [engineGetOutputSize](ExemptionMechanismSpi.md))`(`inputLen:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the length in bytes that an output buffer would need to be in order to hold the result of the next [engineGenExemptionBlob](ExemptionMechanismSpi.md))operation, given the input length`inputLen`(in bytes). |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInit](ExemptionMechanismSpi.md))`(`key:` ` [Key](../java.security/Key.md)!`)` Initializes this exemption mechanism with a key. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInit](ExemptionMechanismSpi.md))`(`key:` ` [Key](../java.security/Key.md)!`, `params:` ` [AlgorithmParameters](../java.security/AlgorithmParameters.md)!`)` Initializes this exemption mechanism with a key and a set of algorithm parameters. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInit](ExemptionMechanismSpi.md))`(`key:` ` [Key](../java.security/Key.md)!`, `params:` ` [AlgorithmParameterSpec](../java.security.spec/AlgorithmParameterSpec.md)!`)` Initializes this exemption mechanism with a key and a set of algorithm parameters. |
| --- | --- |

## Public constructors

### ExemptionMechanismSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ExemptionMechanismSpi()
```

## Protected methods

### engineGenExemptionBlob

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineGenExemptionBlob(): ByteArray!
```

Generates the exemption mechanism key blob.

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the new buffer with the result key blob. |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------|
| `javax.crypto.ExemptionMechanismException` | if problem(s) encountered in the process of generating. |

### engineGenExemptionBlob

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineGenExemptionBlob(
    output: ByteArray!, 
    outputOffset: Int
): Int
```

Generates the exemption mechanism key blob, and stores the result in the`output`buffer, starting at`outputOffset`inclusive.

If the`output`buffer is too small to hold the result, a`ShortBufferException`is thrown. In this case, repeat this call with a larger output buffer. Use [engineGetOutputSize](ExemptionMechanismSpi.md))to determine how big the output buffer should be.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------|
| `output` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer for the result |
| `outputOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset in`output`where the result is stored |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of bytes stored in`output` |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------|
| `javax.crypto.ShortBufferException` | if the given output buffer is too small to hold the result. |
| `javax.crypto.ExemptionMechanismException` | if problem(s) encountered in the process of generating. |

### engineGetOutputSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineGetOutputSize(inputLen: Int): Int
```

Returns the length in bytes that an output buffer would need to be in order to hold the result of the next [engineGenExemptionBlob](ExemptionMechanismSpi.md))operation, given the input length`inputLen`(in bytes).

The actual output length of the next [engineGenExemptionBlob](ExemptionMechanismSpi.md))call may be smaller than the length returned by this method.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------|
| `inputLen` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the input length (in bytes) |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the required output buffer size (in bytes) |

### engineInit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineInit(key: Key!): Unit
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

### engineInit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineInit(
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

### engineInit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineInit(
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
