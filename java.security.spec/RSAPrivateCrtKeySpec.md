# RSAPrivateCrtKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RSAPrivateCrtKeySpec

```
open class RSAPrivateCrtKeySpec : RSAPrivateKeySpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.security.spec.RSAPrivateKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/RSAPrivateKeySpec) ||
| | ↳ | [java.security.spec.RSAPrivateCrtKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/RSAPrivateCrtKeySpec#) |

This class specifies an RSA private key, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard, using the Chinese Remainder Theorem (CRT) information values for efficiency.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RSAPrivateCrtKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/RSAPrivateCrtKeySpec#RSAPrivateCrtKeySpec(java.math.BigInteger,%20java.math.BigInteger,%20java.math.BigInteger,%20java.math.BigInteger,%20java.math.BigInteger,%20java.math.BigInteger,%20java.math.BigInteger,%20java.math.BigInteger))`(`modulus:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `publicExponent:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `privateExponent:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `primeP:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `primeQ:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `primeExponentP:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `primeExponentQ:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `crtCoefficient:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`)` Creates a new`RSAPrivateCrtKeySpec`. |
| [RSAPrivateCrtKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/RSAPrivateCrtKeySpec#RSAPrivateCrtKeySpec(java.math.BigInteger,%20java.math.BigInteger,%20java.math.BigInteger,%20java.math.BigInteger,%20java.math.BigInteger,%20java.math.BigInteger,%20java.math.BigInteger,%20java.math.BigInteger,%20java.security.spec.AlgorithmParameterSpec))`(`modulus:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `publicExponent:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `privateExponent:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `primeP:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `primeQ:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `primeExponentP:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `primeExponentQ:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `crtCoefficient:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `keyParams:` ` [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec)!`)` Creates a new`RSAPrivateCrtKeySpec`with additional key parameters. |

| Public methods ||
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getCrtCoefficient](https://developer.android.com/reference/kotlin/java/security/spec/RSAPrivateCrtKeySpec#getCrtCoefficient())`()` Returns the crtCoefficient. |
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getPrimeExponentP](https://developer.android.com/reference/kotlin/java/security/spec/RSAPrivateCrtKeySpec#getPrimeExponentP())`()` Returns the primeExponentP. |
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getPrimeExponentQ](https://developer.android.com/reference/kotlin/java/security/spec/RSAPrivateCrtKeySpec#getPrimeExponentQ())`()` Returns the primeExponentQ. |
| --- | --- |
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getPrimeP](https://developer.android.com/reference/kotlin/java/security/spec/RSAPrivateCrtKeySpec#getPrimeP())`()` Returns the primeP. |
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getPrimeQ](https://developer.android.com/reference/kotlin/java/security/spec/RSAPrivateCrtKeySpec#getPrimeQ())`()` Returns the primeQ. |
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getPublicExponent](https://developer.android.com/reference/kotlin/java/security/spec/RSAPrivateCrtKeySpec#getPublicExponent())`()` Returns the public exponent. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [RSAPrivateKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/RSAPrivateKeySpec) |---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getModulus](https://developer.android.com/reference/kotlin/java/security/spec/RSAPrivateKeySpec#getModulus())`()` <br /> Returns the modulus. <br /> | | [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec)! | [getParams](https://developer.android.com/reference/kotlin/java/security/spec/RSAPrivateKeySpec#getParams())`()` <br /> Returns the parameters associated with this key, may be null if not present. <br /> | | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getPrivateExponent](https://developer.android.com/reference/kotlin/java/security/spec/RSAPrivateKeySpec#getPrivateExponent())`()` <br /> Returns the private exponent. <br /> | ||

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
| `modulus` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the modulus n |
| `publicExponent` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the public exponent e |
| `privateExponent` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the private exponent d |
| --- | --- |
| `primeP` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the prime factor p of n |
| `primeQ` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the prime factor q of n |
| `primeExponentP` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:this is d mod (p-1) |
| --- | --- |
| `primeExponentQ` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:this is d mod (q-1) |
| `crtCoefficient` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the Chinese Remainder Theorem coefficient q-1 mod p |

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
| `modulus` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the modulus n |
| `publicExponent` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the public exponent e |
| `privateExponent` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the private exponent d |
| --- | --- |
| `primeP` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the prime factor p of n |
| `primeQ` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the prime factor q of n |
| `primeExponentP` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:this is d mod (p-1) |
| --- | --- |
| `primeExponentQ` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:this is d mod (q-1) |
| `crtCoefficient` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the Chinese Remainder Theorem coefficient q-1 mod p |
| `keyParams` | [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec)!:the parameters associated with key |
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
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the crtCoefficient |

### getPrimeExponentP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPrimeExponentP(): BigInteger!
```

Returns the primeExponentP.

| Return ||
|------------------------------------------------------------------------------------------|--------------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the primeExponentP |

### getPrimeExponentQ

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPrimeExponentQ(): BigInteger!
```

Returns the primeExponentQ.

| Return ||
|------------------------------------------------------------------------------------------|--------------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the primeExponentQ |

### getPrimeP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPrimeP(): BigInteger!
```

Returns the primeP.

| Return ||
|------------------------------------------------------------------------------------------|------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the primeP |

### getPrimeQ

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPrimeQ(): BigInteger!
```

Returns the primeQ.

| Return ||
|------------------------------------------------------------------------------------------|------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the primeQ |

### getPublicExponent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPublicExponent(): BigInteger!
```

Returns the public exponent.

| Return ||
|------------------------------------------------------------------------------------------|---------------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the public exponent |
