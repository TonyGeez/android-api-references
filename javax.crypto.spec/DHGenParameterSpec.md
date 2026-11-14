# DHGenParameterSpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DHGenParameterSpec

```
open class DHGenParameterSpec : AlgorithmParameterSpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.crypto.spec.DHGenParameterSpec](DHGenParameterSpec.md) |

This class specifies the set of parameters used for generating Diffie-Hellman (system) parameters for use in Diffie-Hellman key agreement. This is typically done by a central authority.

The central authority, after computing the parameters, must send this information to the parties looking to agree on a secret key.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DHGenParameterSpec](DHGenParameterSpec.md))`(`primeSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `exponentSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a parameter set for the generation of Diffie-Hellman (system) parameters. |

| Public methods ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getExponentSize](DHGenParameterSpec.md))`()` Returns the size in bits of the random exponent (private value). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPrimeSize](DHGenParameterSpec.md))`()` Returns the size in bits of the prime modulus. |

## Public constructors

### DHGenParameterSpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DHGenParameterSpec(
    primeSize: Int, 
    exponentSize: Int)
```

Constructs a parameter set for the generation of Diffie-Hellman (system) parameters. The constructed parameter set can be used to initialize an [AlgorithmParameterGenerator](../java.security/AlgorithmParameterGenerator.md) object for the generation of Diffie-Hellman parameters.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------|
| `primeSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the size (in bits) of the prime modulus. |
| `exponentSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the size (in bits) of the random exponent. |

## Public methods

### getExponentSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getExponentSize(): Int
```

Returns the size in bits of the random exponent (private value).

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the size in bits of the random exponent (private value) |

### getPrimeSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPrimeSize(): Int
```

Returns the size in bits of the prime modulus.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the size in bits of the prime modulus |
