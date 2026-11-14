# RSAKeyGenParameterSpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RSAKeyGenParameterSpec

```
open class RSAKeyGenParameterSpec : AlgorithmParameterSpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.spec.RSAKeyGenParameterSpec](RSAKeyGenParameterSpec.md) |

This class specifies the set of parameters used to generate an RSA key pair.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RSAKeyGenParameterSpec](RSAKeyGenParameterSpec.md))`(`keysize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `publicExponent:` ` [BigInteger](../java.math/BigInteger.md)!`)` Constructs a new`RSAKeyGenParameterSpec`object from the given keysize, public-exponent value, and null key parameters. |
| [RSAKeyGenParameterSpec](RSAKeyGenParameterSpec.md))`(`keysize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `publicExponent:` ` [BigInteger](../java.math/BigInteger.md)!`, `keyParams:` ` [AlgorithmParameterSpec](AlgorithmParameterSpec.md)!`)` Constructs a new`RSAKeyGenParameterSpec`object from the given keysize, public-exponent value, and key parameters. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [AlgorithmParameterSpec](AlgorithmParameterSpec.md)! | [getKeyParams](RSAKeyGenParameterSpec.md))`()` Returns the parameters to be associated with key. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getKeysize](RSAKeyGenParameterSpec.md))`()` Returns the keysize. |
| open [BigInteger](../java.math/BigInteger.md)! | [getPublicExponent](RSAKeyGenParameterSpec.md))`()` Returns the public-exponent value. |
| --- | --- |

| Properties ||
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [BigInteger](../java.math/BigInteger.md)! | [F0](RSAKeyGenParameterSpec.md) The public-exponent value F0 = 3. |
| static [BigInteger](../java.math/BigInteger.md)! | [F4](RSAKeyGenParameterSpec.md) The public exponent-value F4 = 65537. |

## Public constructors

### RSAKeyGenParameterSpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RSAKeyGenParameterSpec(
    keysize: Int, 
    publicExponent: BigInteger!)
```

Constructs a new`RSAKeyGenParameterSpec`object from the given keysize, public-exponent value, and null key parameters.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `keysize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the modulus size (specified in number of bits) |
| `publicExponent` | [BigInteger](../java.math/BigInteger.md)!:the public exponent |

### RSAKeyGenParameterSpec

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RSAKeyGenParameterSpec(
    keysize: Int, 
    publicExponent: BigInteger!, 
    keyParams: AlgorithmParameterSpec!)
```

Constructs a new`RSAKeyGenParameterSpec`object from the given keysize, public-exponent value, and key parameters.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `keysize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the modulus size (specified in number of bits) |
| `publicExponent` | [BigInteger](../java.math/BigInteger.md)!:the public exponent |
| `keyParams` | [AlgorithmParameterSpec](AlgorithmParameterSpec.md)!:the key parameters, may be null |
| --- | --- |

## Public methods

### getKeyParams

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKeyParams(): AlgorithmParameterSpec!
```

Returns the parameters to be associated with key.

| Return ||
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| [AlgorithmParameterSpec](AlgorithmParameterSpec.md)! | the associated parameters, may be null if not present |

### getKeysize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKeysize(): Int
```

Returns the keysize.

| Return ||
|----------------------------------------------------------------------------|--------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the keysize. |

### getPublicExponent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPublicExponent(): BigInteger!
```

Returns the public-exponent value.

| Return ||
|------------------------------------------------------------------------------------------|----------------------------|
| [BigInteger](../java.math/BigInteger.md)! | the public-exponent value. |

## Properties

### F0

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val F0: BigInteger!
```

The public-exponent value F0 = 3. 

### F4

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val F4: BigInteger!
```

The public exponent-value F4 = 65537.
