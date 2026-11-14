# RSAPublicKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RSAPublicKeySpec

```
open class RSAPublicKeySpec : KeySpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.security.spec.RSAPublicKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/RSAPublicKeySpec#) |

This class specifies an RSA public key.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RSAPublicKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/RSAPublicKeySpec#RSAPublicKeySpec(java.math.BigInteger,%20java.math.BigInteger))`(`modulus:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `publicExponent:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`)` Creates a new RSAPublicKeySpec. |
| [RSAPublicKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/RSAPublicKeySpec#RSAPublicKeySpec(java.math.BigInteger,%20java.math.BigInteger,%20java.security.spec.AlgorithmParameterSpec))`(`modulus:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `publicExponent:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `params:` ` [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec)!`)` Creates a new RSAPublicKeySpec with additional key parameters. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getModulus](https://developer.android.com/reference/kotlin/java/security/spec/RSAPublicKeySpec#getModulus())`()` Returns the modulus. |
| open [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec)! | [getParams](https://developer.android.com/reference/kotlin/java/security/spec/RSAPublicKeySpec#getParams())`()` Returns the parameters associated with this key, may be null if not present. |
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getPublicExponent](https://developer.android.com/reference/kotlin/java/security/spec/RSAPublicKeySpec#getPublicExponent())`()` Returns the public exponent. |

## Public constructors

### RSAPublicKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RSAPublicKeySpec(
    modulus: BigInteger!, 
    publicExponent: BigInteger!)
```

Creates a new RSAPublicKeySpec.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------|
| `modulus` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the modulus |
| `publicExponent` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the public exponent |

### RSAPublicKeySpec

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RSAPublicKeySpec(
    modulus: BigInteger!, 
    publicExponent: BigInteger!, 
    params: AlgorithmParameterSpec!)
```

Creates a new RSAPublicKeySpec with additional key parameters.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `modulus` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the modulus |
| `publicExponent` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the public exponent |
| `params` | [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec)!:the parameters associated with this key, may be null |

## Public methods

### getModulus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getModulus(): BigInteger!
```

Returns the modulus.

| Return ||
|------------------------------------------------------------------------------------------|-------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the modulus |

### getParams

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParams(): AlgorithmParameterSpec!
```

Returns the parameters associated with this key, may be null if not present.

| Return ||
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec)! | the parameters associated with this key |

### getPublicExponent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPublicExponent(): BigInteger!
```

Returns the public exponent.

| Return ||
|------------------------------------------------------------------------------------------|---------------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the public exponent |
