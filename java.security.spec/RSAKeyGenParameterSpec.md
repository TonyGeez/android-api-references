# RSAKeyGenParameterSpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RSAKeyGenParameterSpec

```
open class RSAKeyGenParameterSpec : AlgorithmParameterSpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.security.spec.RSAKeyGenParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/RSAKeyGenParameterSpec#) |

This class specifies the set of parameters used to generate an RSA key pair.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RSAKeyGenParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/RSAKeyGenParameterSpec#RSAKeyGenParameterSpec(kotlin.Int,%20java.math.BigInteger))`(`keysize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `publicExponent:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`)` Constructs a new`RSAKeyGenParameterSpec`object from the given keysize, public-exponent value, and null key parameters. |
| [RSAKeyGenParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/RSAKeyGenParameterSpec#RSAKeyGenParameterSpec(kotlin.Int,%20java.math.BigInteger,%20java.security.spec.AlgorithmParameterSpec))`(`keysize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `publicExponent:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `keyParams:` ` [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec)!`)` Constructs a new`RSAKeyGenParameterSpec`object from the given keysize, public-exponent value, and key parameters. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec)! | [getKeyParams](https://developer.android.com/reference/kotlin/java/security/spec/RSAKeyGenParameterSpec#getKeyParams())`()` Returns the parameters to be associated with key. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getKeysize](https://developer.android.com/reference/kotlin/java/security/spec/RSAKeyGenParameterSpec#getKeysize())`()` Returns the keysize. |
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getPublicExponent](https://developer.android.com/reference/kotlin/java/security/spec/RSAKeyGenParameterSpec#getPublicExponent())`()` Returns the public-exponent value. |

| Properties ||
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [F0](https://developer.android.com/reference/kotlin/java/security/spec/RSAKeyGenParameterSpec#F0:java.math.BigInteger) The public-exponent value F0 = 3. |
| static [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [F4](https://developer.android.com/reference/kotlin/java/security/spec/RSAKeyGenParameterSpec#F4:java.math.BigInteger) The public exponent-value F4 = 65537. |

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
| `publicExponent` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the public exponent |

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
| `publicExponent` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the public exponent |
| `keyParams` | [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec)!:the key parameters, may be null |

## Public methods

### getKeyParams

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKeyParams(): AlgorithmParameterSpec!
```

Returns the parameters to be associated with key.

| Return ||
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec)! | the associated parameters, may be null if not present |

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
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the public-exponent value. |

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
