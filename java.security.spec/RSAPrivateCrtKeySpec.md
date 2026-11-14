# RSAPrivateCrtKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RSAPrivateCrtKeySpec

```
open class RSAPrivateCrtKeySpec : RSAPrivateKeySpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.security.spec.RSAPrivateKeySpec](RSAPrivateKeySpec.md) ||
| | ↳ | [java.security.spec.RSAPrivateCrtKeySpec](RSAPrivateCrtKeySpec.md) |

This class specifies an RSA private key, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard, using the Chinese Remainder Theorem (CRT) information values for efficiency.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RSAPrivateCrtKeySpec](RSAPrivateCrtKeySpec.md))`(`modulus:` ` [BigInteger](../java.math/BigInteger.md)!`, `publicExponent:` ` [BigInteger](../java.math/BigInteger.md)!`, `privateExponent:` ` [BigInteger](../java.math/BigInteger.md)!`, `primeP:` ` [BigInteger](../java.math/BigInteger.md)!`, `primeQ:` ` [BigInteger](../java.math/BigInteger.md)!`, `primeExponentP:` ` [BigInteger](../java.math/BigInteger.md)!`, `primeExponentQ:` ` [BigInteger](../java.math/BigInteger.md)!`, `crtCoefficient:` ` [BigInteger](../java.math/BigInteger.md)!`)` Creates a new`RSAPrivateCrtKeySpec`. |
| [RSAPrivateCrtKeySpec](RSAPrivateCrtKeySpec.md))`(`modulus:` ` [BigInteger](../java.math/BigInteger.md)!`, `publicExponent:` ` [BigInteger](../java.math/BigInteger.md)!`, `privateExponent:` ` [BigInteger](../java.math/BigInteger.md)!`, `primeP:` ` [BigInteger](../java.math/BigInteger.md)!`, `primeQ:` ` [BigInteger](../java.math/BigInteger.md)!`, `primeExponentP:` ` [BigInteger](../java.math/BigInteger.md)!`, `primeExponentQ:` ` [BigInteger](../java.math/BigInteger.md)!`, `crtCoefficient:` ` [BigInteger](../java.math/BigInteger.md)!`, `keyParams:` ` [AlgorithmParameterSpec](AlgorithmParameterSpec.md)!`)` Creates a new`RSAPrivateCrtKeySpec`with additional key parameters. |

| Public methods ||
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [BigInteger](../java.math/BigInteger.md)! | [getCrtCoefficient](RSAPrivateCrtKeySpec.md))`()` Returns the crtCoefficient. |
| open [BigInteger](../java.math/BigInteger.md)! | [getPrimeExponentP](RSAPrivateCrtKeySpec.md))`()` Returns the primeExponentP. |
| open [BigInteger](../java.math/BigInteger.md)! | [getPrimeExponentQ](RSAPrivateCrtKeySpec.md))`()` Returns the primeExponentQ. |
| --- | --- |
| open [BigInteger](../java.math/BigInteger.md)! | [getPrimeP](RSAPrivateCrtKeySpec.md))`()` Returns the primeP. |
| open [BigInteger](../java.math/BigInteger.md)! | [getPrimeQ](RSAPrivateCrtKeySpec.md))`()` Returns the primeQ. |
| open [BigInteger](../java.math/BigInteger.md)! | [getPublicExponent](RSAPrivateCrtKeySpec.md))`()` Returns the public exponent. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [RSAPrivateKeySpec](RSAPrivateKeySpec.md) |---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [BigInteger](../java.math/BigInteger.md)! | [getModulus](RSAPrivateKeySpec.md))`()` <br /> Returns the modulus. <br /> | | [AlgorithmParameterSpec](AlgorithmParameterSpec.md)! | [getParams](RSAPrivateKeySpec.md))`()` <br /> Returns the parameters associated with this key, may be null if not present. <br /> | | [BigInteger](../java.math/BigInteger.md)! | [getPrivateExponent](RSAPrivateKeySpec.md))`()` <br /> Returns the private exponent. <br /> | ||

## Public constructors

### RSAPrivateCrtKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RSAPrivateCrtKeySpec(
    modulus: BigInteger!, 
    publicExponent: BigInteger!, 
    privateExponent: BigInteger!, 
    primeP: BigInteger!, 
    primeQ: BigInteger!, 
    primeExponentP: BigInteger!, 
    primeExponentQ: BigInteger!, 
    crtCoefficient: BigInteger!)
```

Creates a new`RSAPrivateCrtKeySpec`.

| Parameters ||
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `modulus` | [BigInteger](../java.math/BigInteger.md)!:the modulus n |
| `publicExponent` | [BigInteger](../java.math/BigInteger.md)!:the public exponent e |
| `privateExponent` | [BigInteger](../java.math/BigInteger.md)!:the private exponent d |
| --- | --- |
| `primeP` | [BigInteger](../java.math/BigInteger.md)!:the prime factor p of n |
| `primeQ` | [BigInteger](../java.math/BigInteger.md)!:the prime factor q of n |
| `primeExponentP` | [BigInteger](../java.math/BigInteger.md)!:this is d mod (p-1) |
| --- | --- |
| `primeExponentQ` | [BigInteger](../java.math/BigInteger.md)!:this is d mod (q-1) |
| `crtCoefficient` | [BigInteger](../java.math/BigInteger.md)!:the Chinese Remainder Theorem coefficient q-1 mod p |

### RSAPrivateCrtKeySpec

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RSAPrivateCrtKeySpec(
    modulus: BigInteger!, 
    publicExponent: BigInteger!, 
    privateExponent: BigInteger!, 
    primeP: BigInteger!, 
    primeQ: BigInteger!, 
    primeExponentP: BigInteger!, 
    primeExponentQ: BigInteger!, 
    crtCoefficient: BigInteger!, 
    keyParams: AlgorithmParameterSpec!)
```

Creates a new`RSAPrivateCrtKeySpec`with additional key parameters.

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `modulus` | [BigInteger](../java.math/BigInteger.md)!:the modulus n |
| `publicExponent` | [BigInteger](../java.math/BigInteger.md)!:the public exponent e |
| `privateExponent` | [BigInteger](../java.math/BigInteger.md)!:the private exponent d |
| --- | --- |
| `primeP` | [BigInteger](../java.math/BigInteger.md)!:the prime factor p of n |
| `primeQ` | [BigInteger](../java.math/BigInteger.md)!:the prime factor q of n |
| `primeExponentP` | [BigInteger](../java.math/BigInteger.md)!:this is d mod (p-1) |
| --- | --- |
| `primeExponentQ` | [BigInteger](../java.math/BigInteger.md)!:this is d mod (q-1) |
| `crtCoefficient` | [BigInteger](../java.math/BigInteger.md)!:the Chinese Remainder Theorem coefficient q-1 mod p |
| `keyParams` | [AlgorithmParameterSpec](AlgorithmParameterSpec.md)!:the parameters associated with key |
| --- | --- |

## Public methods

### getCrtCoefficient

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCrtCoefficient(): BigInteger!
```

Returns the crtCoefficient.

| Return ||
|------------------------------------------------------------------------------------------|--------------------|
| [BigInteger](../java.math/BigInteger.md)! | the crtCoefficient |

### getPrimeExponentP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPrimeExponentP(): BigInteger!
```

Returns the primeExponentP.

| Return ||
|------------------------------------------------------------------------------------------|--------------------|
| [BigInteger](../java.math/BigInteger.md)! | the primeExponentP |

### getPrimeExponentQ

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPrimeExponentQ(): BigInteger!
```

Returns the primeExponentQ.

| Return ||
|------------------------------------------------------------------------------------------|--------------------|
| [BigInteger](../java.math/BigInteger.md)! | the primeExponentQ |

### getPrimeP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPrimeP(): BigInteger!
```

Returns the primeP.

| Return ||
|------------------------------------------------------------------------------------------|------------|
| [BigInteger](../java.math/BigInteger.md)! | the primeP |

### getPrimeQ

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPrimeQ(): BigInteger!
```

Returns the primeQ.

| Return ||
|------------------------------------------------------------------------------------------|------------|
| [BigInteger](../java.math/BigInteger.md)! | the primeQ |

### getPublicExponent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPublicExponent(): BigInteger!
```

Returns the public exponent.

| Return ||
|------------------------------------------------------------------------------------------|---------------------|
| [BigInteger](../java.math/BigInteger.md)! | the public exponent |
