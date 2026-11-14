# RSAPrivateKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RSAPrivateKeySpec

```
open class RSAPrivateKeySpec : KeySpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.security.spec.RSAPrivateKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/RSAPrivateKeySpec#) |

| Known Direct Subclasses [RSAMultiPrimePrivateCrtKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/RSAMultiPrimePrivateCrtKeySpec), [RSAPrivateCrtKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/RSAPrivateCrtKeySpec) |------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [RSAMultiPrimePrivateCrtKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/RSAMultiPrimePrivateCrtKeySpec) | This class specifies an RSA multi-prime private key, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard using the Chinese Remainder Theorem (CRT) information values for efficiency. | | [RSAPrivateCrtKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/RSAPrivateCrtKeySpec) | This class specifies an RSA private key, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard, using the Chinese Remainder Theorem (CRT) information values for efficiency. | |

This class specifies an RSA private key.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RSAPrivateKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/RSAPrivateKeySpec#RSAPrivateKeySpec(java.math.BigInteger,%20java.math.BigInteger))`(`modulus:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `privateExponent:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`)` Creates a new RSAPrivateKeySpec. |
| [RSAPrivateKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/RSAPrivateKeySpec#RSAPrivateKeySpec(java.math.BigInteger,%20java.math.BigInteger,%20java.security.spec.AlgorithmParameterSpec))`(`modulus:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `privateExponent:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `params:` ` [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec)!`)` Creates a new RSAPrivateKeySpec with additional key parameters. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getModulus](https://developer.android.com/reference/kotlin/java/security/spec/RSAPrivateKeySpec#getModulus())`()` Returns the modulus. |
| open [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec)! | [getParams](https://developer.android.com/reference/kotlin/java/security/spec/RSAPrivateKeySpec#getParams())`()` Returns the parameters associated with this key, may be null if not present. |
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getPrivateExponent](https://developer.android.com/reference/kotlin/java/security/spec/RSAPrivateKeySpec#getPrivateExponent())`()` Returns the private exponent. |

## Public constructors

### RSAPrivateKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RSAPrivateKeySpec(
    modulus: BigInteger!, 
    privateExponent: BigInteger!)
```

Creates a new RSAPrivateKeySpec.

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------------------------|
| `modulus` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the modulus |
| `privateExponent` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the private exponent |

### RSAPrivateKeySpec

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RSAPrivateKeySpec(
    modulus: BigInteger!, 
    privateExponent: BigInteger!, 
    params: AlgorithmParameterSpec!)
```

Creates a new RSAPrivateKeySpec with additional key parameters.

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `modulus` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the modulus |
| `privateExponent` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the private exponent |
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

### getPrivateExponent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPrivateExponent(): BigInteger!
```

Returns the private exponent.

| Return ||
|------------------------------------------------------------------------------------------|----------------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the private exponent |
