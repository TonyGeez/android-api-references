# RSAPrivateKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RSAPrivateKeySpec

```
open class RSAPrivateKeySpec : KeySpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.spec.RSAPrivateKeySpec](RSAPrivateKeySpec.md) |

| Known Direct Subclasses [RSAMultiPrimePrivateCrtKeySpec](RSAMultiPrimePrivateCrtKeySpec.md), [RSAPrivateCrtKeySpec](RSAPrivateCrtKeySpec.md) |------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [RSAMultiPrimePrivateCrtKeySpec](RSAMultiPrimePrivateCrtKeySpec.md) | This class specifies an RSA multi-prime private key, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard using the Chinese Remainder Theorem (CRT) information values for efficiency. | | [RSAPrivateCrtKeySpec](RSAPrivateCrtKeySpec.md) | This class specifies an RSA private key, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard, using the Chinese Remainder Theorem (CRT) information values for efficiency. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This class specifies an RSA private key.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RSAPrivateKeySpec](RSAPrivateKeySpec.md))`(`modulus:` ` [BigInteger](../java.math/BigInteger.md)!`, `privateExponent:` ` [BigInteger](../java.math/BigInteger.md)!`)` Creates a new RSAPrivateKeySpec. |
| [RSAPrivateKeySpec](RSAPrivateKeySpec.md))`(`modulus:` ` [BigInteger](../java.math/BigInteger.md)!`, `privateExponent:` ` [BigInteger](../java.math/BigInteger.md)!`, `params:` ` [AlgorithmParameterSpec](AlgorithmParameterSpec.md)!`)` Creates a new RSAPrivateKeySpec with additional key parameters. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [BigInteger](../java.math/BigInteger.md)! | [getModulus](RSAPrivateKeySpec.md))`()` Returns the modulus. |
| open [AlgorithmParameterSpec](AlgorithmParameterSpec.md)! | [getParams](RSAPrivateKeySpec.md))`()` Returns the parameters associated with this key, may be null if not present. |
| open [BigInteger](../java.math/BigInteger.md)! | [getPrivateExponent](RSAPrivateKeySpec.md))`()` Returns the private exponent. |
| --- | --- |

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
| `modulus` | [BigInteger](../java.math/BigInteger.md)!:the modulus |
| `privateExponent` | [BigInteger](../java.math/BigInteger.md)!:the private exponent |

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
| `modulus` | [BigInteger](../java.math/BigInteger.md)!:the modulus |
| `privateExponent` | [BigInteger](../java.math/BigInteger.md)!:the private exponent |
| `params` | [AlgorithmParameterSpec](AlgorithmParameterSpec.md)!:the parameters associated with this key, may be null |
| --- | --- |

## Public methods

### getModulus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getModulus(): BigInteger!
```

Returns the modulus.

| Return ||
|------------------------------------------------------------------------------------------|-------------|
| [BigInteger](../java.math/BigInteger.md)! | the modulus |

### getParams

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParams(): AlgorithmParameterSpec!
```

Returns the parameters associated with this key, may be null if not present.

| Return ||
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [AlgorithmParameterSpec](AlgorithmParameterSpec.md)! | the parameters associated with this key |

### getPrivateExponent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPrivateExponent(): BigInteger!
```

Returns the private exponent.

| Return ||
|------------------------------------------------------------------------------------------|----------------------|
| [BigInteger](../java.math/BigInteger.md)! | the private exponent |
